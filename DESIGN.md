---
version: alpha
name: Studio Ash
description: Design system de Studio Ash — pestañas, cejas y estética facial personalizada
colors:
  primary: "#e88ca8"
  primary-hover: "#d77794"
  on-primary: "#ffffff"
  secondary: "#f3d1dc"
  on-secondary: "#2b2b2b"
  tertiary: "#3a2321"
  on-tertiary: "#ffffff"
  neutral: "#fdfbfb"
  surface: "#ffffff"
  on-surface: "#2b2b2b"
  on-surface-variant: "#6c757d"
  border: "#e0e0e0"
  disabled: "#e0e0e0"
  on-disabled: "#8a8a8a"
  error: "#c86d6d"
  success: "#82a67d"
typography:
  headline-display:
    fontFamily: Playfair Display
    fontSize: 48px
    fontWeight: 700
    lineHeight: 1.15
  headline-lg:
    fontFamily: Playfair Display
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.2
  headline-md:
    fontFamily: Playfair Display
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  body-md:
    fontFamily: Poppins
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-md:
    fontFamily: Poppins
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1
rounded:
  sm: 6px
  md: 12px
  lg: 16px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 14px 28px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  card-product:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-service:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
  tag-offer:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    rounded: "{rounded.full}"
    padding: 4px 12px
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.sm}"
    padding: 12px 16px
  message-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
    typography: "{typography.body-md}"
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
  text-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
---

# Studio Ash — Design System

## Overview

Studio Ash es un estudio especializado en diseño de mirada, extensiones de pestañas personalizadas según morfología facial y tratamientos de belleza no invasivos (Lash Lifting, nutrición con keratina y depilación con hilo orgánico).

Nuestra usuaria principal es **Maura Salinas**, una profesional de 29 años que busca ahorrar tiempo en su rutina matutina, valora la pulcritud y el cuidado de su piel sensible, y necesita total confianza en los estándares de higiene y bioseguridad del servicio.

El estilo visual es femenino, sofisticado, cálido y minimalista: refleja delicadeza mediante tonos nude y rosas suaves (`#e88ca8`), contrastados con un fondo claro y luminoso (`#fdfbfb`) y una tipografía elegante con serif (*Playfair Display*) en conjunto con una sans-serif geométrica moderna (*Poppins*).

## Colors

- **Primary (`#e88ca8`):** Rosa destacado de la marca. Se utiliza en el botón principal de llamada a la acción (CTA "Agendar Cita", "Pagar Abono"), elementos interactivos activos y badges de destaque. No se usa como fondo de secciones completas ni en textos extensos.
- **Primary Hover (`#d77794`):** Rosa de tono más profundo para feedback visual al pasar el cursor o pulsar botones primarios.
- **Secondary (`#f3d1dc`):** Rosa pastel suave para fondos de chips de categoría, badges secundarios y etiquetas de oferta o tiempo estimado.
- **Tertiary / Accent (`#3a2321`):** Espresso oscuro para titulares de alto impacto, logo tipográfico y textos que requieran máxima jerarquía.
- **Neutral (`#fdfbfb`):** Fondo general de todas las páginas (nude casi blanco), transmitiendo luz, calma y asepsia clínica.
- **Surface (`#ffffff`):** Fondo de tarjetas de servicio (`card-service`), contenedor del resumen de compra y modales de confirmación.
- **On-Surface (`#2b2b2b`):** Color del cuerpo de texto general, párrafos y descripciones, garantizando contraste accesible WCAG AA.
- **On-Surface-Variant (`#6c757d`):** Gris suave para textos secundarios, tiempos de sesión (ej. "90 min") y notas al pie.
- **Border (`#e0e0e0`):** Líneas divisorias sutiles, bordes de inputs de formulario y contornos de tarjetas.
- **Success (`#82a67d`):** Verde suave para confirmaciones de citas exitosas y validaciones de reserva.
- **Error (`#c86d6d`):** Rojo moderado para alertas de campos obligatorios en el agendamiento y contraindicaciones de salud.

## Typography

- **Títulos y encabezados:** *Playfair Display* (Serif). Aporta distinción editorial, lujo y calidez artesanal.
  - `headline-display` (48px, bold, line-height 1.15): Título del Hero de la Landing.
  - `headline-lg` (32px, semi-bold, line-height 1.2): Encabezados principales `h1` de catálogo y títulos de sección `h2`.
  - `headline-md` (24px, semi-bold, line-height 1.25): Títulos de tarjetas de servicios y subtítulos `h3`.
- **Textos de lectura y componentes:** *Poppins* (Sans-serif). Aporta legibilidad instantánea, geometría limpia y modernidad en pantallas digitales.
  - `body-md` (16px, regular 400, line-height 1.6): Descripciones de servicios, párrafos de blog y campos de formulario.
  - `label-md` (16px, semi-bold 600, line-height 1): Botones de acción, enlaces de navegación, chips de filtro y precios destacados.

## Layout

- **Ancho máximo del contenedor:** 1200px centrado horizontalmente con márgenes laterales automáticos.
- **Márgenes de seguridad:**
  - Desktop: 32px a los lados.
  - Mobile: 16px a los lados.
- **Breakpoints:**
  - **Mobile:** hasta 767px (layout a 1 columna vertical, menú hamburguesa desplegable en navbar, botones principales en modo sticky fijo al pie).
  - **Tablet:** 768px a 1023px (grilla de 2 columnas para catálogo y testimonios).
  - **Desktop:** desde 1024px (grilla de 3 columnas para servicios y blog, layout de 2 columnas para ficha de servicio y reserva).
- **Escala de espaciados:** Uso estricto de múltiplos de 8px (`sm: 8px`, `md: 16px`, `lg: 24px`, `xl: 32px`, `2xl: 48px`).

## Elevation & Depth

- La jerarquía se expresa mediante fondos limpios y sombras suaves difusas en lugar de bordes pesados:
  - **Nivel 0 (Base):** Fondo general Ivory (`#fdfbfb`).
  - **Nivel 1 (Superficie):** Tarjetas `card-service` sobre fondo blanco con sombra sutil `0 2px 4px rgba(43, 43, 43, 0.04)` y borde `1px solid #e0e0e0`.
  - **Nivel 2 (Hover / Interacción):** Elevación al pasar el mouse con sombra `0 8px 24px rgba(232, 140, 168, 0.25)` y leve traslación vertical de -3px.
  - **Nivel 3 (Fijo / Modales):** Navbar y botón sticky mobile con sombra `0 4px 12px rgba(43, 43, 43, 0.08)`.

## Shapes

- **Botones (`button-primary`, `button-secondary`):** Completamente redondeados con estilo píldora (`rounded.full: 9999px`) para un aspecto orgánico, amable y sofisticado.
- **Tarjetas (`card-service`, `card-product`):** Esquinas redondeadas suaves (`rounded.md: 12px`).
- **Campos de formulario (`input-field`):** Bordes con radio sutil (`rounded.sm: 6px`).
- **Chips de categoría y etiquetas (`tag-offer`):** Estilo píldora (`rounded.full: 9999px`).

## Components

### Botón Primario (`button-primary`)
- **Propósito:** Llamada a la acción principal del sitio ("Agendar Cita", "Pagar Abono y Confirmar").
- **Estados:**
  - *Normal:* Fondo `#e88ca8`, texto `#ffffff`, padding 14px 28px, bordes redondeados.
  - *Hover:* Fondo oscurecido a `#d77794` con sombra rosada difusa.
  - *Disabled:* Fondo gris `#e0e0e0`, texto `#8a8a8a`, cursor `not-allowed`.
- **Regla:** Solo puede existir un botón primario visible al mismo tiempo en el viewport principal de la pantalla.

### Botón Secundario (`button-secondary`)
- **Propósito:** Acciones secundarias de exploración ("Ver detalles", "Más información").
- **Estados:** Fondo blanco, contorno sutil o texto en color primario `#e88ca8`, hover con fondo pastel suave `#f3d1dc`.

### Tarjeta de Servicio (`card-service`)
- **Propósito:** Mostrar los tratamientos del catálogo.
- **Contenido obligatorio:** Imagen con ratio 4:3, badge de categoría, nombre en *Playfair Display* (máximo 2 líneas), duración estimada (ej. "90 min"), precio destacado en pesos chilenos y botón secundario "Ver detalles".
- **Regla:** El precio y el tiempo siempre deben ser visibles sin necesidad de interacción previa.

### Campo de Texto (`input-field`)
- **Propósito:** Captura de datos de la clienta en el formulario de confirmación de cita (Nombre, WhatsApp, Email, notas).
- **Regla:** Al hacer foco (`focus`), el borde cambia a `#e88ca8` con un halo suave y accesible.

## Do's and Don'ts

### Do's (Lo que siempre se hace)
- Usar siempre las fuentes oficiales *Playfair Display* para títulos y *Poppins* para el cuerpo de texto.
- Mantener espacios en blanco generosos (mínimo 24px entre bloques) para transmitir pulcritud, calma y exclusividad.
- Incluir siempre la duración y el valor del abono (50%) en las reservas para evitar sorpresas a la clienta.
- Mostrar micro-interacciones suaves (transiciones de 0.2s) en hover de tarjetas y botones.

### Don'ts (Lo que nunca se hace)
- Nunca usar negros puros (`#000000`) para fondos ni para textos; usar `#2b2b2b` o `#3a2321` para mantener la suavidad visual.
- Nunca usar tipografías manuscritas o de fantasía ilegibles en descripciones o textos de botones.
- Nunca saturar las pantallas con colores fluorescentes o rojos estridentes; los avisos de error deben mantenerse en el tono `#c86d6d`.
- Nunca omitir el estado mobile ni permitir que elementos provoquen desplazamiento horizontal en pantallas estrechas.
