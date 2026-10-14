# Spec de desarrollo — Studio Ash

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.
Construye el sitio siguiendo exactamente docs/10-spec-desarrollo.md:
solo HTML y CSS, la estructura de archivos y la navegación definidas,
las variables de :root con los valores de DESIGN.md y la estructura
semántica de cada página. Usa el código de Stitch solo como referencia
visual. Al terminar, revisa cada criterio de aceptación y dime cuáles
se cumplen y cuáles no.
```

---

## 1. Estructura de archivos

```text
mi-emprendimiento/
├── index.html                  # Pantalla 1: Home / Landing
├── servicios.html              # Pantalla 2: Catálogo de Servicios
├── servicio-detalle.html       # Pantalla 3: Ficha de Servicio & Test Morfológico
├── confirmacion.html           # Pantalla 4: Confirmación de Cita / Agendamiento
├── blog.html                   # Pantalla 5: Blog & Guías de Cuidado (Q&A)
├── articulo.html               # Pantalla 6: Artículo de Cuidado y Bioseguridad
├── DESIGN.md                   # Design system con tokens y reglas del proyecto
├── css/
│   └── styles.css              # Hoja de estilos global con variables :root y componentes
├── img/                        # Carpeta de imágenes del proyecto
│   ├── servicios/              # Fotografías de catálogo y tratamientos
│   └── blog/                   # Portadas e ilustraciones de artículos
├── stitch/                     # Código exportado de Stitch (referencia visual)
└── docs/                       # Especificaciones y documentación del proyecto
```

---

## 2. Páginas y navegación

- **Navbar global en todas las páginas:** Logotipo de Studio Ash, enlaces principales (Inicio, Servicios, FAQ / Blog, Contacto) y botón CTA button-primary "Agendar Cita".
- **Footer global en todas las páginas:** Calificaciones y opiniones (5 estrellas), redes sociales (@studioash), dirección del estudio (Edificio Angamos #667, Valparaíso), botón de WhatsApp y derechos reservados.

| Desde | Elemento | Lleva a |
|---|---|---|
| `index.html` | Botón "Agendar Cita" (Navbar y Hero) | `servicios.html` |
| `index.html` | Botón "Ver detalles" de cada tarjeta de servicio | `servicio-detalle.html` |
| `index.html` | Enlace "Preguntas Frecuentes / Blog" | `blog.html` |
| `servicios.html` | Botón "Agendar / Añadir" de cualquier servicio | `servicio-detalle.html` |
| `servicios.html` | Chips de filtro ("Todos", "Pestañas", "Cejas", "Kits") | Filtrado dinámico en la misma página |
| `servicio-detalle.html` | Botón "Seleccionar Fecha y Hora" | `confirmacion.html` |
| `servicio-detalle.html` | Botón "Consultar por WhatsApp" | Enlace externo directo a WhatsApp (`https://wa.me/569XXXXXXXX`) |
| `confirmacion.html` | Botón "Pagar Abono y Confirmar Cita" | Mensaje/modal de confirmación de cita agendada |
| `blog.html` | Tarjeta de artículo destacado | `articulo.html` |
| `articulo.html` | Banner CTA al final de la lectura | `servicios.html` |
| Todas las páginas | Logotipo de Studio Ash en la barra de navegación | `index.html` |

---

## 3. Estructura semántica

### `index.html` (Landing)
```html
<header>              <!-- Navbar con logo, navegación y CTA Agendar -->
<main>
  <section class="hero">        <!-- Titular h1, propuesta de valor, imagen y CTA principal -->
  <section class="badges">      <!-- Indicadores de confianza: Sin irritación, Alta gama, Diseño personalizado -->
  <section class="services">    <!-- h2 "Nuestros Servicios" y grilla de tarjetas de servicio -->
  <section class="artist">      <!-- Bloque "Conoce a tu Lash Artist" con biografía y credenciales -->
  <section class="reviews">     <!-- Reseñas reales y testimonios de clientas (5 estrellas) -->
  <section class="faq">         <!-- Acordeón interactivo de preguntas frecuentes -->
</main>
<footer>              <!-- Datos de contacto, redes sociales, dirección y créditos -->
```

### `servicios.html` (Catálogo de Servicios)
```html
<header>              <!-- Navbar global -->
<main>
  <section class="catalog-header"> <!-- h1 "Catálogo de Servicios", descripción y chips de filtro -->
  <section class="services-grid">  <!-- Grilla de 3 columnas con <article class="card-service"> -->
</main>
<footer>              <!-- Footer global -->
```

### `servicio-detalle.html` (Ficha de Servicio & Test)
```html
<header>              <!-- Navbar global -->
<main>
  <section class="service-layout"> <!-- Layout 2 columnas: galería izquierda + panel derecho -->
    <div class="gallery">          <!-- Imagen principal y miniaturas antes/después -->
    <div class="details">          <!-- h1 nombre, precio, duración, selector de variante y CTA -->
  </section>
  <section class="artist-mini">    <!-- Resumen de credenciales de la especialista asignada -->
  <section class="morphology-test"><!-- Test interactivo de morfología y tipo de ojo -->
  <section class="tabs-info">      <!-- Pestañas: Cuidados posteriores, Contraindicaciones y FAQ -->
</main>
<footer>              <!-- Footer global -->
```

### `confirmacion.html` (Confirmación de Cita / Agendamiento)
```html
<header>              <!-- Navbar simplificado con indicador de pasos -->
<main>
  <section class="checkout-grid">  <!-- Layout 2 columnas: resumen reserva + formulario -->
    <aside class="booking-summary"><!-- Resumen: servicio, fecha, hora, desglose total y abono 50% -->
    <section class="client-form">  <!-- Formulario: Nombre, WhatsApp, Email, notas y botón de pago -->
  </section>
  <section class="policies-notice"><!-- Indicaciones: tolerancia 15 min, asistir sin maquillaje -->
</main>
<footer>              <!-- Footer global -->
```

---

## 4. Organización del CSS

```css
:root {
  /* Paleta cromática — Studio Ash */
  --color-primary: #D8B4A6;          /* Truffle Blush: botones principales y bordes */
  --color-primary-hover: #C9A091;    /* Truffle Blush oscuro para hover */
  --color-secondary: #C48B9F;        /* Dusty Rose: detalles secundarios e interactivos */
  --color-accent: #3A2321;           /* Espresso Brown: títulos y textos de máximo contraste */
  --color-bg: #FAF8F5;               /* Ivory: fondo principal suave y pulcro */
  --color-surface: #FFFFFF;          /* Blanco puro para tarjetas y contenedores */
  --color-text: #2B2B2B;             /* Dark Neutral: cuerpo de texto y párrafos */
  --color-text-muted: #6B6563;       /* Texto secundario y leyendas */
  --color-success: #82A67D;          /* Soft Green: confirmaciones y abonos exitosos */
  --color-error: #C86D6D;            /* Muted Red: validación y errores de formulario */

  /* Tipografía */
  --font-title: 'Playfair Display', serif;
  --font-body: 'Plus Jakarta Sans', sans-serif;

  /* Escala de espaciados */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Radios de borde */
  --radius-sm: 6px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-full: 9999px;

  /* Sombras y elevación */
  --shadow-sm: 0 2px 4px rgba(58, 35, 33, 0.04);
  --shadow-md: 0 4px 12px rgba(58, 35, 33, 0.08);
  --shadow-hover: 0 8px 24px rgba(58, 35, 33, 0.12);
}
```

- **Convención de clases:** Nombres en inglés con guiones (kebab-case): `.navbar`, `.hero`, `.card-service`, `.button-primary`, `.button-secondary`, `.chip-filter`, `.summary-box`.
- **Breakpoints:**
  - **Mobile:** hasta 767px (layout a 1 columna vertical, menú colapsable, botón CTA sticky al pie).
  - **Tablet:** de 768px a 1023px (grillas de 2 columnas).
  - **Desktop:** desde 1024px (grillas de 3 columnas, ancho máximo contenedor 1200px centrado).
- **Enfoque de diseño:** *Mobile first*, garantizando legibilidad en pantallas táctiles de 375px.

---

## 5. Criterios de aceptación

### Navegación
- [ ] La barra de navegación (Navbar) y el pie de página (Footer) son consistentes y funcionales en todas las pantallas.
- [ ] Se puede completar el flujo de compra y reserva: `index.html` → `servicios.html` → `servicio-detalle.html` → `confirmacion.html`.
- [ ] El enlace directo a WhatsApp funciona correctamente con el mensaje preconfigurado.
- [ ] No existen enlaces rotos ni botones sin destino asignado.

### Funcionalidades
- [ ] La landing presenta los servicios destacados con precios claros y tiempo de aplicación.
- [ ] El catálogo de servicios permite filtrar por categoría de tratamiento.
- [ ] La ficha de servicio muestra la duración, precio, contraindicaciones y selector de variantes de efecto.
- [ ] La pantalla de confirmación calcula y muestra claramente el desglose del total y el abono requerido del 50%.

### Diseño y estilos
- [ ] Todos los colores provienen estrictamente de las variables `:root` definidas según la paleta de Studio Ash.
- [ ] El contraste entre el texto y el fondo cumple la norma WCAG AA (texto `#2B2B2B` o `#3A2321` sobre fondo Ivory `#FAF8F5`).
- [ ] Los botones tienen estados interactivos claros (`hover`, `active`, `disabled`).
- [ ] La tipografía respeta la jerarquía visual: *Playfair Display* para encabezados y *Plus Jakarta Sans* para lectura fluida.

### Responsive
- [ ] El sitio es 100% navegable en teléfonos móviles (ancho 375px) sin desplazamiento horizontal (scroll horizontal).
- [ ] Las grillas colapsan de 3 columnas en desktop a 1 sola columna en dispositivos móviles.
- [ ] Los botones táctiles en versión móvil tienen un tamaño mínimo accesible (44px de alto).

### Accesibilidad y publicación
- [ ] Cada página cuenta con un único encabezado principal `<h1>`.
- [ ] Todas las imágenes incorporan atributos `alt` descriptivos para lectores de pantalla.
- [ ] La estructura utiliza etiquetas semánticas de HTML5 (`<header>`, `<main>`, `<section>`, `<article>`, `<footer>`).
