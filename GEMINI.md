# Contexto del Repositorio para Gemini

## Metadatos del Proyecto

| Campo                    | Valor                                                              |
| ------------------------ | ------------------------------------------------------------------ |
| **Nombre**               | FÓRMULAS DEL MUNDO                                                 |
| **Repositorio**          | `NeruDev/FORMULAS-DEL-MUNDO`                                      |
| **Fecha de creación**    | 2026-02-12T22:22:25-06:00                                         |
| **Última actualización** | 2026-02-14T17:33:42-06:00                                         |
| **Autor**                | NeruDev                                                            |
| **Lenguaje principal**   | Markdown (contenido), Python (scripts auxiliares)                  |
| **Motor de renderizado** | KaTeX / MathJax (LaTeX embebido en Markdown)                      |
| **Entorno virtual**      | `.venv/` (Python, gestionado con `venv`)                           |
| **Licencia**             | Sin definir                                                        |
| **Idioma del contenido** | Español                                                            |

---

## Naturaleza y Propósito

Este repositorio recopila **modelos matemáticos heurísticos** diseñados para explicar fenómenos sociales, demográficos y cognitivos a través de formulaciones cuantitativas. Cada modelo nace de **conversaciones exploratorias con inteligencia artificial**, donde se proponen, debaten y refinan hipótesis hasta alcanzar una formulación formal con notación LaTeX.

El objetivo no es producir modelos predictivos validados empíricamente, sino construir **marcos conceptuales estructurados** que permitan razonar cuantitativamente sobre la realidad social. Son herramientas de pensamiento, no de predicción industrial.

---

## Estructura del Repositorio

```
FORMULAS-DEL-MUNDO/
├── .gemini/                          # Configuración de contexto para Gemini
│   └── settings.json
├── .github/
│   └── copilot-instructions.md       # Instrucciones de contexto para Copilot
├── .gitignore
├── .venv/                            # Entorno virtual Python (ignorado por git)
├── GEMINI.md                         # ← Este archivo
├── README.md                         # Documentación técnica y registro de scripts
├── Complejidad cognitiva/
│   ├── Contexto completo.md          # Conversación completa con la IA
│   ├── Formula completa explicada.md # Formulación formal del modelo IPCC-100
│   └── image/                        # Recursos gráficos
│       └── Contextocompleto/
│           └── 1771103119032.png
└── Invierno demografico/
    ├── Contexto completo.md          # Conversación completa con la IA
    └── Formula completa.md           # Formulación formal del modelo Ψ₃
```

### Convención de carpetas temáticas

Cada carpeta temática representa un **dominio de investigación** y contiene:

| Archivo                        | Función                                                                                                  |
| ------------------------------ | -------------------------------------------------------------------------------------------------------- |
| `Contexto completo.md`         | Transcripción íntegra de la conversación con la IA. Incluye prompts, respuestas, iteraciones y análisis. |
| `Formula completa.md` / `Formula completa explicada.md` | Formulación matemática formal extraída y refinada a partir de la conversación.                            |
| `image/`                       | Recursos visuales referenciados desde los documentos Markdown.                                           |

---

## Cronología del Repositorio

| Fecha (UTC-6)             | Evento                                                                  |
| ------------------------- | ----------------------------------------------------------------------- |
| 2026-02-12 22:22:25       | Commit inicial: creación del repositorio y `README.md`                  |
| 2026-02-12 22:53:43       | Modelo $\Psi_3$ (Invierno demográfico): formulación formal agregada     |
| 2026-02-14 15:52:32       | Módulo Complejidad cognitiva: contexto, fórmula IPCC-100, `.gitignore`, `.venv` |
| 2026-02-14 17:00:36       | Corrección de formato LaTeX y eliminación de duplicados en Invierno demográfico |
| 2026-02-14 17:08:09       | Actualización de análisis demográfico con tasas de fertilidad específicas |
| 2026-02-14 17:08:34       | Mejoras de experiencia y corrección de errores en módulos               |
| 2026-02-14 17:33:42       | Contexto completo de Invierno demográfico actualizado correctamente     |

---

## Modelos Contenidos

### 1. Índice Psicosocial de Complejidad Cognitiva (IPCC-100)

- **Carpeta:** `Complejidad cognitiva/`
- **Símbolo principal:** $\Phi_{100}$
- **Dominio:** Psicología cognitiva, sociología del conocimiento
- **Descripción:** Cuantifica la complejidad cognitiva de un individuo o grupo en una escala de 0 a 100, ponderando factores de resiliencia cognitiva frente a factores de simplificación.
- **Fecha de formulación:** 2026-02-14

### 2. Índice Estructural de Potencial Reproductivo (Modelo $\Psi_3$)

- **Carpeta:** `Invierno demografico/`
- **Símbolo principal:** $\Psi_3$
- **Dominio:** Demografía, economía del comportamiento reproductivo
- **Descripción:** Modela la voluntad de reproducción como razón entre fuerzas biológicas/culturales (numerador) y resistencias económicas/tecnológicas (denominador). Incluye análisis por país y fórmula cualitativa de la "Ecuación House de la Atrofia Reproductiva" ($\Psi$).
- **Fecha de formulación:** 2026-02-12

---

## Directivas de Estilo y Lenguaje

### Para el contenido general

- Utilizar un **registro formal y técnico**. El texto debe leerse como documentación científica divulgativa, no como un blog casual.
- Las explicaciones de modelos y sus aplicaciones deben emplear **terminología precisa** del dominio correspondiente (demografía, psicología cognitiva, estadística, etc.).
- Las fórmulas se escriben en **LaTeX embebido en Markdown**: `$...$` para expresiones inline y `$$...$$` para bloques display.

### Para la explicación de parámetros

- Cada variable, subíndice y operador debe explicarse con un **lenguaje didáctico y accesible**, asumiendo que el lector tiene formación básica pero no es especialista.
- Usar analogías solo cuando clarifiquen sin distorsionar el concepto matemático.
- Indicar siempre: **símbolo**, **nombre completo**, **rango de valores**, **unidad conceptual** e **interpretación práctica**.

### LaTeX

- Escapar `%` como `\%` dentro de expresiones matemáticas.
- Usar `\text{}` para texto descriptivo dentro de fórmulas.
- Los subíndices de más de un carácter requieren llaves: `_{eff}`, no `_eff`.
- No mezclar delimitadores `$` con paréntesis `()` como delimitadores matemáticos.

---

## Stack Técnico

| Componente         | Tecnología                          | Propósito                                          |
| ------------------ | ----------------------------------- | -------------------------------------------------- |
| Contenido          | Markdown `.md`                      | Documentación, conversaciones, formulaciones       |
| Fórmulas           | LaTeX (KaTeX/MathJax)               | Renderizado de expresiones matemáticas             |
| Scripts auxiliares  | Python 3.x                          | Corrección de errores de sintaxis LaTeX en lote    |
| Entorno virtual    | `.venv/` (módulo `venv` de Python)  | Aislamiento de dependencias para scripts           |
| Control de versiones | Git + GitHub                      | Historial, colaboración, trazabilidad de cambios   |

---

## Instrucciones para la IA

1. **Contexto temático:** Cada carpeta es un dominio independiente. No mezclar variables ni notación entre modelos distintos salvo que se solicite explícitamente una comparación.
2. **Formato de salida:** Siempre que se genere o modifique contenido, mantener la estructura Markdown existente con encabezados `###`, listas con `*` o `-`, y tablas con `|`.
3. **Fórmulas:** Validar que toda expresión LaTeX renderice correctamente con KaTeX. Evitar los errores documentados en el `README.md` (sección "Errores detectados post-conversión").
4. **Idioma:** Todo el contenido se produce en **español**. La notación matemática sigue convenciones internacionales estándar (caracteres griegos, subíndices en inglés cuando es convención del campo, e.g., `_{eff}`).
5. **Nuevos modelos:** Al crear un nuevo dominio temático, seguir la convención de carpetas: `Nombre del tema/Contexto completo.md` + `Nombre del tema/Formula completa.md`.
6. **Scripts Python:** Documentar en el `README.md` cualquier script ejecutado, incluyendo: propósito, transformaciones realizadas, errores detectados y correcciones aplicadas.
7. **Tono de las conversaciones:** Los archivos `Contexto completo.md` preservan el tono original de la conversación con la IA (que puede incluir humor, sarcasmo o analogías médicas). No sanear ni censurar el contenido conversacional; es parte del registro intelectual.
