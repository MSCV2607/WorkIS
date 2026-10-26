# Modo ATF

Usá este modo para crear o revisar un Análisis Técnico-Funcional iterativo. El AF aprobado es obligatorio como fuente de referencia. Si no está aprobado o accesible, podés preparar un borrador, pero marcá el pendiente y no lo presentes como listo para aprobación.

## Fuentes y prioridad

1. AF aprobado.
2. Guía de trabajo del proyecto.
3. Recursos de la tarjeta.
4. Código fuente y configuración como evidencia del funcionamiento actual.
5. Plantilla ATF: [plantilla-atf.md](../templates/plantilla-atf.md).
6. Aclaraciones explícitas del usuario.

Cada afirmación técnica relevante debe indicar su evidencia: archivo, componente, prueba, recurso o conversación.

## Flujo de versiones

1. Revisá las fuentes disponibles en solo lectura.
2. Elaborá el análisis inicial y las dudas o contradicciones.
3. Proponé crear `Sistema_IDTarjeta_ATF_v0.1.md` en la carpeta configurada y esperá confirmación antes de escribirlo.
4. Después de la revisión del usuario, creá una nueva versión independiente (`v0.2`, `v0.3`, etc.). Nunca sobrescribas una anterior.
5. Creá `Sistema_IDTarjeta_ATF_V1.md` únicamente con la aprobación explícita del usuario.

## Estructura obligatoria

Usá la plantilla completa. No elimines secciones. Cuando algo no aplique, escribí `No aplica` y justificá por qué. Conservá el historial y las aprobaciones en la sección 17.

El ATF debe diferenciar el funcionamiento actual, cambio solicitado, comportamiento esperado e implementación técnica propuesta. Las dudas funcionales o técnicas deben quedar visibles, sin asumir una respuesta.
