# 📰 Proyecto de Investigación Web — Revista Científica Digital

> Curso de Programación Web I · Ingeniería en Sistemas
> Coordinación del proyecto: Auxiliar de clase
> Supervisión académica: Ingeniero a cargo del curso

---

## 1. ¿Qué vamos a construir?

Cada grupo va a producir **una edición de revista de investigación en formato web (HTML + CSS)**. La revista es el formato general — el diseño, la tipografía y el estilo son los mismos para todos los grupos — pero cada grupo elige **cómo contar su investigación**:

- **Formato entrevista** — cada integrante es "entrevistado" sobre su aporte a la investigación, y en conjunto sus respuestas cuentan el proceso completo. Ideal si el tema se presta a distintas perspectivas dentro del grupo.
- **Formato artículo científico** — un artículo clásico de revista de investigación (resumen, introducción, objetivos, metodología, resultados, conclusión, referencias), firmado por todos los integrantes como autores. Ideal si el tema es más técnico y se explica mejor de forma directa.

Ambos formatos usan la misma plantilla visual (`template/css/estilos.css`), así que la revista se ve unificada aunque cada grupo haya elegido un camino distinto.

## 2. Tema de investigación

Cada grupo elige **uno** de estos dos caminos:

- **Tecnología o tema innovador actual** — una tecnología emergente, tendencia o innovación relevante hoy en día (IA, ciberseguridad, cómputo en la nube, hardware, sostenibilidad tecnológica, etc.)
- **Propuesta de solución a un problema actual de la carrera** — un problema real o vigente relacionado con Ingeniería en Sistemas, y una propuesta de solución fundamentada.

## 3. Metodología: el método científico como columna vertebral

Sin importar qué formato elijan, el contenido **debe** seguir el método científico. Así se traduce en cada formato:

| Etapa del método científico | En formato entrevista... | En formato artículo... |
|---|---|---|
| Planteamiento del problema | "¿Qué problema o pregunta los llevó a esta investigación?" | Sección 1. Introducción |
| Hipótesis | "¿Qué esperaban encontrar antes de investigar?" | Sección 2. Objetivos e hipótesis |
| Metodología | "¿Cómo investigaron esto? ¿Qué fuentes o métodos usaron?" | Sección 3. Metodología |
| Resultados / hallazgos | "¿Qué encontraron? ¿Qué los sorprendió?" | Sección 4. Resultados |
| Conclusión / propuesta | "¿A qué conclusión llegaron? / ¿Qué proponen?" | Sección 5. Discusión y conclusión |

En el formato entrevista, cada integrante responde estas etapas **desde su propio aporte o enfoque** dentro de la investigación. En el formato artículo, el grupo redacta cada sección de forma conjunta, firmando todos como autores.

## 4. Estructura del repositorio

```
proyecto-investigacion-web/
├── README.md                     ← este documento
├── docs/
│   ├── guia-html-css.md          ← especificación técnica: etiquetas, clases y CSS a usar
│   └── rubrica-evaluacion.md     ← cómo se evalúa cada entrega
├── template/
│   ├── formato-entrevista/
│   │   └── index.html            ← plantilla si el grupo elige formato entrevista
│   ├── formato-articulo/
│   │   └── index.html            ← plantilla si el grupo elige formato artículo científico
│   ├── css/estilos.css           ← hoja de estilos base compartida por ambos formatos
│   └── assets/                   ← aquí van imágenes/fotos que use su grupo
└── grupos/
    └── grupo-XX-nombre-del-tema/ ← cada grupo trabaja únicamente dentro de su propia carpeta
        ├── index.html
        ├── css/estilos.css
        └── assets/
```

## 5. Cómo entregar

1. Hagan **fork** de este repositorio (o clónenlo si trabajan todos en el mismo equipo de GitHub).
2. Decidan como grupo qué formato usar y copien la carpeta correspondiente (`template/formato-entrevista/` o `template/formato-articulo/`) junto con `template/css/` dentro de `grupos/`, renombrando la carpeta según la convención:
   `grupo-XX-tema-corto` (ejemplo: `grupo-03-inteligencia-artificial`)
3. Editen **únicamente** dentro de su carpeta. No modifiquen `template/` ni el contenido de otros grupos.
4. Suban su avance mediante **commits individuales** — cada integrante debe tener al menos un commit visible con su parte de la entrevista. Esto es parte de la evaluación de trabajo en equipo.
5. Al finalizar, abran un **Pull Request** hacia la rama principal con el nombre: `Entrega Grupo XX - Nombre del tema`.

## 6. Reglas generales

- Todo el sitio debe construirse **solo con HTML y CSS** (ver `docs/guia-html-css.md` para el detalle exacto de qué está permitido en esta etapa del curso).
- Deben usar las clases y estructura del `template/`. Pueden ampliar el CSS, pero no eliminar ni romper la estructura base.
- El texto de la entrevista debe sonar natural y fluido, no como una lista de respuestas cortadas. Redacten como si un periodista realmente les hubiera hecho estas preguntas.
- Cada integrante debe tener su sección claramente identificada dentro de la página (foto o ilustración, nombre, y sus respuestas).

## 7. Documentos relacionados

- 📐 [`docs/guia-html-css.md`](docs/guia-html-css.md) — qué etiquetas, clases y estilos deben usar
- ✅ [`docs/rubrica-evaluacion.md`](docs/rubrica-evaluacion.md) — cómo se califica la entrega

## 8. Checklist antes de entregar

- [ ] Mi grupo usó la plantilla de `template/` sin romper su estructura
- [ ] Cada integrante tiene su propia sección con las 5 etapas del método científico respondidas como entrevista
- [ ] El texto suena fluido y profesional, no como una lista técnica
- [ ] Cada integrante tiene al menos un commit propio
- [ ] Revisé `docs/guia-html-css.md` y no usé etiquetas o técnicas fuera de lo permitido
- [ ] El Pull Request está abierto con el nombre correcto

