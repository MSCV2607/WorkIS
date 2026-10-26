---
name: workis
description: "Gestiona el ciclo documental de tarjetas de cambio: ATF iterativos, estimaciones frontend y comentarios funcionales de Trello. Usar cuando se solicite analizar una tarjeta, preparar un ATF, estimar desarrollo frontend o documentar una implementación para Trello."
---

# WorkIS

**Versión:** `v0.1.0`

WorkIS gestiona el análisis y la documentación de cambios para uno o varios sistemas. Identifica primero el proyecto y el modo de trabajo; solicita únicamente los datos mínimos que falten.

## Perfiles de proyecto

Los perfiles guardan la configuración estable de cada sistema: nombre, rutas del repositorio, frontend y backend opcionales, AF/ATF/recursos, rama base y carpetas de entregables. Si no hay perfiles, pedí al usuario esa información antes de analizar. Si hay varios perfiles y no se indicó uno, pedí cuál usar.

Guardá los perfiles localmente, fuera del repositorio de WorkIS y sin incluir rutas personales en Git. En Windows, usá `%USERPROFILE%\.workis\projects.local.json`; en otros sistemas, `~/.workis/projects.local.json`.

## Elegir modo

| Pedido | Modo | Referencia |
|---|---|---|
| Crear, revisar o versionar un ATF | `atf` | [ATF](references/atf.md) |
| Estimar horas y checklist de frontend | `estimar` | [Estimación](references/estimacion-frontend.md) |
| Comentario de Trello desde una rama | `comentario-rama` | [Comentarios](references/comentarios-trello.md) |
| Comentario de Trello desde un commit | `comentario-commit` | [Comentarios](references/comentarios-trello.md) |
| Comentario de Trello desde ATF y cambios | `comentario-atf` | [Comentarios](references/comentarios-trello.md) |
| Comentario de Trello desde la sesión | `comentario-sesion` | [Comentarios](references/comentarios-trello.md) |

Si el modo no es claro, preguntá si necesita ATF, estimación o comentario de Trello. Para un comentario, pedí una única aclaración sobre la fuente: rama, commit, ATF aprobado o sesión.

## Reglas comunes

- Separá hechos confirmados, evidencia, propuestas y dudas. No inventes requisitos, impactos, validaciones, enlaces, decisiones ni resultados.
- Si AF, ATF, recursos, código o conversación se contradicen, documentá la contradicción y pedí definición; no la resuelvas por cuenta propia.
- Al inspeccionar repositorios, ramas, commits, código o documentación, trabajá en solo lectura. No modifiques el proyecto analizado.
- Antes de crear o actualizar un entregable, indicá ruta, nombre y versión. Solo escribí el archivo después de la confirmación del usuario.
- Respetá las convenciones del perfil del proyecto y preguntá ante cualquier valor ausente o ambiguo.
- El ATF es técnico, completo y estructurado; la estimación es únicamente un checklist; el comentario Trello es funcional y no técnico.
- Referenciá las fuentes relevantes: AF y evidencias en ATF; ATF/AF aprobados y referencias operativas en Trello; ATF aprobado en estimaciones.

## Entregables

Usá estos nombres, sin sobrescribir versiones existentes:

```text
Sistema_IDTarjeta_ATF_v0.1.md
Sistema_IDTarjeta_ATF_v0.2.md
Sistema_IDTarjeta_ATF_V1.md
Sistema_IDTarjeta_CambioImplementado.md
```

`Sistema` es el identificador del perfil y `IDTarjeta` el código real de la tarjeta. Los ATF van a la carpeta configurada para ATF. Las copias de comentarios solo se crean a pedido explícito. Las estimaciones se entregan en el chat, salvo que el usuario solicite guardarlas.
