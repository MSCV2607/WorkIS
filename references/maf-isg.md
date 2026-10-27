# Marco operativo MAF-ISG

## Principios obligatorios

- AF define qué debe hacer el sistema y por qué; ATF define cómo se implementará un AF aprobado.
- No inventar datos, responsables, APIs, tablas, prioridades, estimaciones, reglas, decisiones o resultados.
- No convertir una propuesta técnica en una regla funcional ni un incidente reportado en defecto reproducido.
- Las ambigüedades se registran como pendientes concretos, con responsable, impacto y condición de bloqueo.
- Si una sección no aplica, indicarlo y justificarlo.
- Cada regla confirmada usa un código único y se vincula con casos de prueba; en ATF, además, con implementación y prueba técnica.

## Estados de evidencia

Usar de forma consistente: `Confirmado`, `Pendiente`, `Resuelto`, `Incidente reportado`, `Reproducido`, `Propuesta funcional`, `Propuesta técnica`, `Aprobado` y `No aplica`.

Usar los prefijos: `RN` (regla), `EX` (excepción), `CP` (caso funcional), `RF` (riesgo funcional), `P` (pendiente), `DT` (decisión técnica), `ET` (excepción técnica), `PT` (prueba técnica) y `RT` (riesgo técnico).

## Control de versiones y aprobación

- `0.1` es el borrador inicial; `0.2`, `0.3` y siguientes son revisiones previas a la primera aprobación.
- La primera versión aprobada es `1.0`; las versiones previas se conservan sin sobrescribir.
- Una aprobación registra rol, persona, fecha, observación y versión exacta.
- Una modificación posterior de alcance, reglas, excepciones o pruebas requiere nueva versión y revisión; no modificar silenciosamente una versión aprobada.

## Revisión antes de entregar

Confirmar alcance y exclusiones, actores, flujo, reglas, excepciones, parámetros, impacto, pruebas, riesgos, contradicciones, pendientes, fuentes, historial y trazabilidad. En un ATF, evaluar además datos, APIs, seguridad, auditoría, errores, regresión, instalación, reversión y estimación.
