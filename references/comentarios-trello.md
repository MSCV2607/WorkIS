# Modos de comentarios de Trello

Los comentarios son funcionales y no técnicos. No describas archivos, funciones, componentes ni diffs. Las ramas, PR, commits, migraciones y configuraciones se incluyen únicamente como enlaces o referencias operativas.

## Fuentes permitidas

| Modo | Fuente principal |
|---|---|
| `comentario-rama` | Diff acumulado de la rama frente a su base, commits propios y evidencia disponible. |
| `comentario-commit` | Solo el commit indicado y su diff. |
| `comentario-atf` | AF, ATF aprobado y cambios implementados. |
| `comentario-sesion` | Decisiones y validaciones de la conversación, contrastadas con los cambios reales. |

Al analizar una rama o commit, trabajá exclusivamente en solo lectura. No crees, elimines ni modifiques archivos, ramas, configuraciones ni el estado del repositorio.

## Plantilla obligatoria

Trello es el registro principal. Copiá estos campos a la tarjeta y mantenelos actualizados. Enlazá el AF y el ATF aprobados, sin repetir sus definiciones.

```markdown
- Proyecto, ID de tarjeta, responsable y versión prevista: [ ]
- AF y ATF aprobados, accesibles y acordes con lo publicado: [Enlaces o pendiente]
- Qué se hizo y por qué: [Función nueva, mejora o corrección concreta]
- Cómo se usa y qué resultado se espera: [Ubicación y pasos; o «sin impacto visible»]
- Impacto: [Usuarios, procesos, permisos, datos, integraciones y funciones relacionadas; o no aplica]
- Diferencia respecto del AF o cambio de alcance: [No aplica o decisión enlazada]
- Rama, PR, commit, migraciones y configuración: [Enlaces; o no aplica]
- Validaciones, resultado y evidencias: [ ]
- Permisos o tareas posteriores: [No aplica o detalle]
- Limitaciones, riesgos, documentos y tarjetas relacionadas: [No aplica o enlaces]
```

No documentes como realizado algo solo propuesto, investigado o pendiente. Si no hay evidencia para una validación, impacto o diferencia de alcance, dejá el pendiente visible o indicá `No aplica` únicamente cuando corresponda. Diferenciá explícitamente incidencia reportada, validación realizada, decisión acordada y limitación pendiente. Si el resultado contradice AF o ATF, informalo como diferencia de alcance o incumplimiento; no lo resuelvas en el comentario.

Si el usuario solicita una copia local, proponé crear `Sistema_IDTarjeta_CambioImplementado.md` en la carpeta configurada para comentarios y esperá confirmación antes de escribirla.
