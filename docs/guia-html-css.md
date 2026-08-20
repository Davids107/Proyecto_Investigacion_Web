# 📐 Guía técnica: HTML y CSS permitidos en este proyecto

Esta guía establece las convenciones técnicas del proyecto. El objetivo es que todos los grupos construyan sobre las mismas bases, garantizando un resultado consistente, semántico y fácil de revisar.

---

## 1. Qué SÍ deben usar

### Etiquetas semánticas obligatorias

En lugar de armar todo con `<div>`, la estructura del `template/index.html` ya usa estas etiquetas — respétenlas:

| Etiqueta | Para qué se usa aquí |
|---|---|
| `<header>` | Encabezado de la revista (título, número de edición, nombre del grupo) |
| `<main>` | Contenedor de todo el contenido de la entrevista |
| `<article>` | Cada bloque de entrevista (una por integrante) |
| `<section>` | Cada etapa del método científico dentro de una entrevista |
| `<figure>` / `<figcaption>` | Foto o ilustración del integrante con su descripción |
| `<footer>` | Créditos, fecha, curso |
| `<h1>`, `<h2>`, `<h3>` | Jerarquía de títulos — no salten niveles (no usar `h3` sin haber usado `h2` antes) |
| `<blockquote>` | Para resaltar una frase textual destacada de la entrevista |
| `<nav>` | Solo si su revista tiene más de una página/sección navegable |

### Buenas prácticas de HTML

- Un solo `<h1>` por página.
- Atributo `alt` obligatorio en **todas** las imágenes.
- Indentación consistente (2 espacios).
- Nombres de archivo en minúsculas, sin espacios ni tildes (`grupo-03-ia.html`, no `Grupo 03 IA.html`).
- Comentarios `<!-- -->` para separar las secciones de cada integrante.

### Clases CSS ya definidas (usar tal cual)

El archivo `template/css/estilos.css` ya trae estas clases listas — su trabajo es **aplicarlas correctamente en el HTML**, no reinventarlas:

| Clase | Uso |
|---|---|
| `.revista__header` | Contenedor del encabezado principal |
| `.revista__titulo` | Título principal de la edición |
| `.revista__meta` | Línea de metadatos (edición, fecha, grupo) |
| `.entrevista` | Contenedor de cada `<article>` de integrante |
| `.entrevista__foto` | Imagen/figura del integrante |
| `.entrevista__nombre` | Nombre del integrante entrevistado |
| `.entrevista__rol` | Su rol o enfoque dentro de la investigación |
| `.entrevista__cuerpo` | Envuelve todas las `.etapa` (y el `.destacado`) de un integrante. **No lo eliminen** — activa el maquetado a dos columnas en pantallas grandes y la letra capital de la primera respuesta. |
| `.etapa` | Cada `<section>` de una etapa del método científico |
| `.etapa__pregunta` | La pregunta que "hace" el entrevistador |
| `.etapa__respuesta` | La respuesta del integrante |
| `.destacado` | Para usar junto con `<blockquote>` en una frase relevante |

> ⚠️ **`.entrevista__cuerpo` es obligatorio.** Si lo eliminan, pierden las columnas, la letra capital y que el `.destacado` rompa el layout correctamente. No necesitan configurar nada — el CSS ya lo hace por ustedes, solo tienen que mantener la estructura del `template/index.html`.

### Clases del formato artículo científico (alternativa)

Si su grupo eligió `template/formato-articulo/`, usan este set de clases en vez de las de entrevista:

| Clase | Uso |
|---|---|
| `.articulo` | Contenedor del artículo completo (un solo `<article>` por grupo, no uno por integrante) |
| `.articulo__titulo` | Título del artículo |
| `.articulo__autores` | Línea con los nombres de todos los integrantes como autores |
| `.articulo__resumen` | Caja de resumen/abstract al inicio |
| `.articulo__cuerpo` | Envuelve las `.seccion` — activa columnas y letra capital, igual que `.entrevista__cuerpo` |
| `.seccion` | Cada sección numerada (Introducción, Metodología, Resultados, etc.) |
| `.seccion__titulo` | Título de la sección |
| `.seccion__texto` | Texto de la sección |
| `.referencias` | Lista numerada de fuentes citadas |
| `.destacado` | Misma cita destacada que en el formato entrevista — también disponible aquí |

**No mezclen los dos formatos en la misma página.** Elijan uno solo por grupo y usen únicamente las clases de ese formato.

### Efectos editoriales automáticos (no hay que programarlos)

- **Columnas tipo revista:** en pantallas de escritorio, el cuerpo de cada entrevista se acomoda en dos columnas automáticamente.
- **Letra capital:** la primera respuesta de cada integrante (etapa "Planteamiento") lleva una letra grande al estilo revista impresa.
- **Cita destacada de ancho completo:** el `.destacado` rompe las dos columnas para resaltar la frase, como en una revista real.
- **Impresión / exportar a PDF:** el diseño ya tiene una versión optimizada para imprimir (`Ctrl+P` o `Cmd+P` desde el navegador da un resultado limpio, sin sombras ni colores de fondo).

## 2. Qué NO deben usar todavía

Las siguientes tecnologías están fuera del alcance de esta etapa del proyecto. Su uso no suma puntos y rompe la consistencia de la entrega:

- ❌ JavaScript (ningún `<script>` con lógica propia)
- ❌ Frameworks o librerías CSS (Bootstrap, Tailwind, etc.)
- ❌ CSS Grid o Flexbox avanzado que no venga ya en `estilos.css`
- ❌ Animaciones o transiciones CSS propias
- ❌ Frameworks de HTML generado por builders (Wix, Canva, etc.) — el código se escribe a mano

## 3. Pueden extender (con criterio)

- Colores dentro de la paleta ya definida en `:root` del CSS (ver variables `--color-*`)
- Tamaños de fuente adicionales para casos puntuales, siempre usando `rem`
- Agregar imágenes propias en `assets/` (optimizadas, peso razonable)

## 4. Estructura de carpetas por grupo

```
grupos/grupo-XX-tema/
├── index.html
├── css/
│   └── estilos.css     ← copia del template, pueden extenderla
└── assets/
    └── (fotos, logos, etc.)
```

## 5. Validación antes de entregar

- Abran su `index.html` en el navegador y revisen que no haya elementos rotos.
- Verifiquen que el HTML sea válido (pueden usar [validator.w3.org](https://validator.w3.org)).
- Confirmen que todas las imágenes tengan `alt` y que los enlaces (si hay) funcionen.

