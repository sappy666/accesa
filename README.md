# acces.a — Diseño sin barreras

> Una guía visual e interactiva para diseñar experiencias digitales más accesibles.

![HTML](https://img.shields.io/badge/HTML5-Accessible-black?style=flat-square)
![CSS](https://img.shields.io/badge/CSS3-Responsive-black?style=flat-square)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-black?style=flat-square)
![WCAG](https://img.shields.io/badge/WCAG-2.2-blue?style=flat-square)
![Responsive](https://img.shields.io/badge/Responsive-Mobile%20First-blue?style=flat-square)

---

## 01 — Sobre el proyecto

**acces.a** es una landing page experimental y educativa creada para explorar cómo pequeñas decisiones de diseño pueden hacer que una interfaz sea más fácil de percibir, comprender y utilizar.

El proyecto no busca únicamente **hablar sobre accesibilidad**.

La propia interfaz funciona como demostración.

Contraste, tipografía, navegación por teclado, estados de foco, áreas táctiles, movimiento reducido y diferentes preferencias visuales pueden explorarse directamente desde el sitio.

**Diseñar para más personas no significa diseñar menos.**

---

## 02 — ¿Qué puedes explorar?

La experiencia incluye ejemplos y recomendaciones sobre:

- Contraste de color
- Jerarquía tipográfica
- Tamaños de texto
- Áreas táctiles
- Estados `:focus-visible`
- Navegación mediante teclado
- Formularios accesibles
- Texto alternativo
- Uso correcto del color
- HTML semántico
- Preferencias de movimiento
- Componentes accesibles
- Escalas y especificaciones UI
- Fragmentos de código listos para copiar
- Prompts para auditar proyectos con IA

---

## 03 — Accessibility Menu

El sitio incorpora su propio panel de accesibilidad.

Desde él puedes modificar la experiencia y observar en tiempo real cómo diferentes necesidades afectan una interfaz.

### Contenido

`Aumentar texto`  
`Cursor grande`  
`Ayudas visuales`  
`Ocultar imágenes`  
`Fuente legible`

### Apariencia

`Modo oscuro`  
`Alto contraste`  
`Invertir colores`  
`Escala de grises`  
`Brillo`  
`Saturación`

### Navegación y lectura

`Guía de lectura`  
`Resaltar enlaces`  
`Reducir movimiento`

Las preferencias seleccionadas se conservan localmente en el navegador.

---

## 04 — UI Specs

El proyecto también funciona como una pequeña referencia para diseñadores.

### Tipografía

| Uso | Tamaño recomendado |
| --- | ---: |
| Texto pequeño | 14 px |
| Texto base | 16 px |
| Texto destacado | 18–20 px |
| Subtítulos | 24–32 px |
| Display | 48–96 px |

El tamaño por sí solo no garantiza legibilidad. Interlineado, longitud de línea, contraste, peso y contexto también importan.

### Contraste

Para WCAG AA, como referencia general:

**Texto normal** → `4.5:1`

**Texto grande** → `3:1`

**Componentes y elementos gráficos relevantes** → `3:1`

### Touch targets

Los elementos interactivos deben disponer de un área cómoda para interacción táctil.

En este proyecto se utiliza **44 × 44 px** como referencia de diseño confortable.

---

## 05 — Código listo para usar

Algunos patrones incluidos en la guía pueden reutilizarse directamente.

### Focus visible

```css
:focus-visible {
  outline: 3px solid #2563eb;
  outline-offset: 4px;
}
