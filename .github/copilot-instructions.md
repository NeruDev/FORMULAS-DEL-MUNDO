# Instrucciones de Contexto para GitHub Copilot

## Metadatos del Proyecto

- **Repositorio:** `NeruDev/FORMULAS-DEL-MUNDO`
- **Creado:** 2026-02-12T22:22:25-06:00
- **Última actualización:** 2026-02-14T17:33:42-06:00
- **Idioma del contenido:** Español
- **Stack:** Markdown (contenido) + LaTeX (fórmulas) + Python (scripts auxiliares)
- **Entorno virtual:** `.venv/` (Python `venv`)

---

## Descripción del Proyecto

Repositorio de **modelos matemáticos heurísticos** que buscan explicar fenómenos sociales, demográficos y cognitivos. Los modelos se originan en **conversaciones exploratorias con inteligencia artificial** y se formalizan con notación LaTeX.

El propósito es construir **marcos conceptuales cuantitativos** para razonar sobre la realidad social: herramientas de pensamiento y seguimiento de ideas para modelar aspectos del mundo real a través de la IA.

---

## Estructura del Repositorio

Cada carpeta temática es un **dominio de investigación independiente** con la siguiente convención:

| Archivo                          | Función                                                                |
| -------------------------------- | ---------------------------------------------------------------------- |
| `Contexto completo.md`           | Transcripción íntegra de la conversación con la IA (prompts + respuestas) |
| `Formula completa.md` / `Formula completa explicada.md` | Formulación matemática formal del modelo                              |
| `image/`                         | Recursos gráficos referenciados en los documentos                     |

### Dominios actuales

1. **Complejidad cognitiva** — Modelo IPCC-100 ($\Phi_{100}$): índice psicosocial de complejidad cognitiva (escala 0–100). Creado: 2026-02-14.
2. **Invierno demográfico** — Modelo $\Psi_3$: índice estructural de potencial reproductivo. Incluye la "Ecuación House de la Atrofia Reproductiva" ($\Psi$). Creado: 2026-02-12.

---

## Directivas de Estilo

### Contenido general
- **Registro formal y técnico.** El texto debe leerse como documentación científica divulgativa.
- Usar **terminología precisa** del dominio correspondiente (demografía, psicología cognitiva, estadística, etc.).
- Todo el contenido se produce en **español**.

### Explicación de parámetros
- **Lenguaje didáctico y accesible.** Asumir formación básica pero no especialista.
- Para cada variable indicar: **símbolo**, **nombre completo**, **rango de valores**, **unidad conceptual** e **interpretación práctica**.
- Las analogías son bienvenidas solo cuando clarifiquen sin distorsionar.

### LaTeX en Markdown
- Inline: `$...$`. Display: `$$...$$`.
- Escapar `%` como `\%` dentro de expresiones matemáticas.
- Texto descriptivo dentro de fórmulas: `\text{}`.
- Subíndices multi-carácter: `_{eff}`, nunca `_eff`.
- No mezclar `$` con `()` como delimitadores matemáticos.
- Validar renderizado con KaTeX.

---

## Directivas de Código Python

- Los scripts Python son **auxiliares de corrección**: procesan archivos `.md` para arreglar errores de sintaxis LaTeX en lote.
- Ejecutar siempre dentro del entorno virtual `.venv/`.
- Documentar cada script en el `README.md` con: propósito, transformaciones, errores encontrados y correcciones.
- Patrones comunes de errores ya documentados en `README.md`:
  - `%` como comentario LaTeX dentro de `\frac{}{}`
  - Artefactos Markdown (`===`) dentro de bloques `$$`
  - Variables con subíndice en texto plano sin `$...$`
  - Subíndices sin llaves (`_eff` → `_{eff}`)
  - Superposición de regex entre scripts sucesivos

---

## Convenciones para Nuevos Dominios

Al agregar un nuevo tema:

1. Crear carpeta: `Nombre del tema/`
2. Incluir `Contexto completo.md` (conversación con la IA)
3. Incluir `Formula completa.md` (formulación formal)
4. Opcional: carpeta `image/` para recursos gráficos
5. Actualizar el `README.md` y los archivos de contexto de IA

---

## Notas para Copilot

- **No mezclar** variables ni notación entre modelos de distintos dominios salvo comparación explícita.
- **Preservar el tono original** de los archivos `Contexto completo.md` (pueden incluir humor, sarcasmo o analogías narrativas). Es parte del registro intelectual.
- Al generar fórmulas, **verificar** que no se incurra en los errores de renderizado LaTeX documentados.
- Preferir **ediciones incrementales** sobre reescrituras completas.
- Los archivos `.md` son el producto principal. Los scripts `.py` son herramientas desechables de mantenimiento.
