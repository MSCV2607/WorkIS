# Modo estimación frontend

Usá este modo a partir de un ATF aprobado. La salida contiene únicamente el checklist listo para pegar en Trello: no agregues explicación, tabla ni resumen del ATF.

## Criterios

- Considerá exclusivamente trabajo de frontend.
- Agrupá una misma unidad de implementación en una sola tarea. No fragmentes por funciones, tipos, variables o revisiones normales del código.
- Considerá la reutilización de componentes o lógica existente. No estimes como desarrollo desde cero si el ATF indica un ajuste sobre algo existente.
- No incluyas backend, base de datos, infraestructura, DevOps ni cambios de contrato que correspondan a otro equipo; mencioná una dependencia solo cuando sea necesaria.
- No agregues tiempo por riesgos hipotéticos, análisis duplicado ni trabajo no respaldado por el ATF.
- Incluí pruebas o verificación frontend cuando correspondan.

## Formato obligatorio

Estas tareas siempre deben aparecer con exactamente estos tiempos:

```text
Análisis Técnico Funcional de la Incidencia +2hs
Completado de Tarjeta +30min
PR +20min
```

Entre ellas, agregá las tareas concretas de implementación y, cuando aplique, de pruebas/verificación:

```text
Análisis Técnico Funcional de la Incidencia +2hs
[Implementación frontend concreta] +Xhs
[Pruebas / verificación] +Xhs
Completado de Tarjeta +30min
PR +20min
```
