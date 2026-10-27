# Modo ATF

Usá este modo para crear o revisar un Análisis Técnico-Funcional iterativo. El AF aprobado es obligatorio como fuente de referencia. Si no está aprobado o accesible, podés preparar un borrador, pero marcá el pendiente y no lo presentes como listo para aprobación.

## Carga de fuentes y prioridad

1. `AGENTS.md` o reglas del proyecto.
2. Metodología del proyecto.
3. Plantilla ATF: [plantilla-atf.md](../templates/plantilla-atf.md).
4. Criterios de validación y estados de trazabilidad.
5. AF aprobado.
6. Recursos de la tarjeta y aclaraciones explícitas del usuario.
7. Código fuente y configuración como evidencia del funcionamiento actual.

Si hay impacto de datos, completar además el relevamiento de objetos, integridad, migración, reversión, auditoría, replicación y volumen. Si no hay impacto, indicar `No aplica` con justificación; no inventar tablas, campos ni procedimientos.

Cada afirmación técnica relevante debe indicar su evidencia: archivo, componente, prueba, recurso o conversación. Separá siempre hechos confirmados, incidente reportado, pendiente, propuesta técnica y decisión aprobada. No presentes un incidente como reproducido sin evidencia ni resuelvas una ambigüedad mediante una suposición.

## Flujo de versiones

1. Revisá las fuentes disponibles en solo lectura y auditá el AF: reglas, excepciones, pruebas, contradicciones y términos no verificables.
2. Si el AF no está aprobado, sólo prepará un borrador técnico claramente identificado; no lo presentes como listo para implementar o aprobar.
3. Elaborá el análisis inicial, los riesgos y las dudas o contradicciones. Reportá primero hallazgos críticos, luego importantes, menores, ambigüedades, riesgos y preguntas.
4. Proponé crear `Sistema_IDTarjeta_ATF_v0.1.md` en la carpeta configurada y esperá confirmación antes de escribirlo.
5. Después de cada revisión, creá una nueva versión independiente (`v0.2`, `v0.3`, etc.). Nunca sobrescribas una versión anterior ni una aprobada.
6. Creá `Sistema_IDTarjeta_ATF_V1.md` únicamente con aprobación explícita que identifique la versión. Ante un cambio posterior, generá una versión nueva, actualizá trazabilidad e historial y solicitá nueva aprobación si cambia alcance, reglas o pruebas.

## Estructura obligatoria

Usá la plantilla completa. No elimines secciones. Cuando algo no aplique, escribí `No aplica` y justificá por qué. Conservá el historial y las aprobaciones en la sección 17.

El ATF debe diferenciar funcionamiento actual, cambio solicitado, comportamiento esperado e implementación técnica propuesta. Las dudas funcionales o técnicas deben quedar visibles, sin asumir una respuesta. Cada regla AF confirmada debe relacionarse con su implementación, al menos un caso funcional y una prueba técnica. Antes de presentar una versión, verificar alcance, datos, APIs, seguridad, errores, regresión, riesgos, instalación, reversión y estimación.
