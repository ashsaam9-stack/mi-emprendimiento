# Arquitectura de la información — STUDIO ASH

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

```text
Inicio (landing)
├── Hero / Propuesta de Valor (Inicio)
├── Servicios & Morfología
│   ├── Ficha: Extensiones de pestañas según morfología
│   ├── Ficha: Lash Lifting & nutrición (keratina / botox)
│   └── Ficha: Depilación facial hindú (hilo)
├── Galería Antes / Después (por tipo de ojo y rostro)
├── Beneficios & Garantía de Higiene y Bioseguridad
├── Tienda / Post-Cuidado
│   ├── Categoría: Limpieza y desmaquillantes hipoalergénicos
│   ├── Categoría: Nutrición y sueros fortalecedores
│   ├── Categoría: Accesorios y cepillos
│   ├── Ficha de producto
│   └── Carrito de compras
├── Blog (Contenido Educativo)
│   ├── Categoría: Cuidado e higiene
│   ├── Categoría: Morfología & estilo
│   ├── Categoría: Durabilidad & mantenimiento
│   └── Artículo individual (con comentarios y compartir)
├── Preguntas Frecuentes (FAQ)
├── Contacto & Reserva (CTA / Formulario / WhatsApp)
├── Términos y Condiciones
├── Política de Privacidad
└── 404 (Página no encontrada con enlace de retorno)
```

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: Reserva / Consulta (Agendamiento)

```text
Instagram / TikTok (link en bio o anuncio de mirada natural)
→ Inicio (landing)
→ [Revisa la propuesta de valor en el Hero y hace scroll a "Servicios"]
→ Sección: Servicios & Morfología
→ [Identifica su servicio de interés: extensiones según morfología o depilación con hilo]
→ Sección: Galería Antes / Después
→ [Consulta resultados reales y verifica garantías de higiene y materiales]
◇ ¿Prefiere resolver dudas antes o agendar de inmediato?
   ├── Resolver dudas → [Clic en botón flotante de WhatsApp] → Chat de WhatsApp
   └── Agendar directo → [Clic en botón principal "Reservar Cita"]
→ Formulario de Reserva / Agenda
→ [Selecciona servicio, fecha y hora disponible]
→ Fin: Reserva confirmada / Notificación de cita lista
```

### Flujo 2: Educación y Resolución de Dudas (Contenido)

```text
Google / Redes ("depilación sin irritación piel sensible")
→ Artículo del Blog: "¿Piel sensible o alergias? Por qué la depilación con hilo es tu mejor opción"
→ [Lee sobre la técnica hindú sin cera ni químicos y baja a la sección de cuidados]
→ Sección: Preguntas Frecuentes (FAQ)
→ [Resuelve dudas sobre rojeces, duración y contraindicaciones]
◇ ¿Qué decide hacer la usuaria?
   ├── Comprar insumo de mantenimiento → [Clic en producto recomendado: Espuma limpiadora libre de aceites] → Ficha de producto → Carrito
   └── Agendar cita en el studio → [Clic en "Solicitar evaluación personalizada"] → Contacto / WhatsApp
→ Fin: Cita agendada o producto seleccionado
```

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de servicios y productos

| Categoría | Servicios / Productos |
|---|---|
| **Pestañas Personalizadas** | Extensiones de pestañas con diseño según morfología facial (Clásico, Efecto Rímel, Volumen Suave, Volumen Intenso, Variedad de efectos adaptados a cada tipo de ojo). |
| **Lifting & Tratamientos** | Lash Lifting con nutrición profunda de keratina, botox de pestañas, serum multivitaminas y tinte de pestañas. |
| **Depilación Facial Hindú** | Depilación con hilo 100% orgánico para cejas, bozo y rostro completo (sin químicos, sin cera, ideal para piel sensible). |
| **Post-Cuidado Facial y Pestañas** *(Tienda)* | Lash shampoo hipoalergénico, espumas de limpieza libres de aceites, suero fortalecedor y cepillos especiales para pestañas. |

### Categorías del blog / Contenido Educativo

| Categoría | Idea de artículo / Sección | Necesidad o motivación de la proto-persona | Servicio / Producto relacionado |
|---|---|---|---|
| **Cuidado e Higiene** | "¿Piel sensible o alergias? Por qué la depilación con hilo es tu mejor opción" | Evitar rojeces, ardor e irritaciones causadas por la cera tradicional o químicos. | Depilación facial hindú (con hilo) / Espuma limpiadora calmante |
| **Morfología & Estilo** | "Cómo elegir el diseño de pestañas según la forma de tus ojos" | Encontrar un diseño natural y armónico que realce sus facciones sin verse recargado. | Extensiones de pestañas personalizadas según morfología |
| **Durabilidad & Mantenimiento** | "Guía de cuidados posteriores para un Lash Lifting y extensiones duraderas" | Ahorrar tiempo en las mañanas y mantener los resultados impecables por semanas sin dañar la pestaña natural. | Lash Lifting & nutrición / Lash shampoo y cepillo |
