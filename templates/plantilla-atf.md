# Plantilla de Análisis Técnico Funcional

> El ATF debe referenciar un AF aprobado. No eliminar secciones. Si no corresponde, indicar `No aplica` y justificar.

## Identificación y trazabilidad

| Campo | Valor |
|---|---|
| Código | `[REQ-0000]` |
| Título | `[Nombre]` |
| AF de referencia | `[Archivo, versión, fecha y estado]` |
| Producto / módulo | `[Completar]` |
| Responsable del ATF | `[Completar]` |
| Revisores | `[Líder / DBA / Integraciones / otros]` |
| Versión objetivo | `[Completar]` |
| Repositorio / rama | `[Completar]` |
| Versión / fecha | `[0.1 / AAAA-MM-DD]` |
| Estado | `[Borrador / En revisión / Aprobado]` |

## 1. Resumen técnico

`[Enfoque general para cumplir el AF. No redefinir el negocio.]`

## 2. Funcionamiento actual relevado

| Componente / proceso | Funcionamiento actual | Evidencia | Debe conservarse |
|---|---|---|---|
| `[Nombre]` | `[Descripción]` | `[Archivo, SP, pantalla, prueba]` | `[Sí / No]` |

## 3. Impacto técnico

Evaluar expresamente:

- proyectos y módulos;
- archivos y componentes;
- pantallas;
- tablas, campos e índices;
- procedimientos y consultas;
- APIs e integraciones;
- reportes y dashboards;
- procesos automáticos;
- replicación;
- configuración;
- permisos y auditoría;
- rendimiento;
- instalación.

| Área | Componente | Impacto | Cambio previsto | Responsable |
|---|---|---|---|---|
| `[Código / BD / UI / API / Reporte]` | `[Nombre]` | `[Directo / Indirecto / Sin impacto]` | `[Detalle]` | `[Nombre]` |

## 4. Diseño de la solución

### 4.1 Flujo técnico

| Paso | Componente | Acción técnica | Entrada | Salida / error |
|---:|---|---|---|---|
| 1 | `[Componente]` | `[Acción]` | `[Datos]` | `[Resultado]` |

### 4.2 Componentes nuevos o modificados

| Tipo | Nombre | Acción | Descripción |
|---|---|---|---|
| `[Archivo / Clase / SP / Tabla / API / Pantalla]` | `[Nombre]` | `[Nuevo / Modifica]` | `[Cambio]` |

### 4.3 Decisiones técnicas

| Código | Decisión | Alternativas | Fundamento | Estado |
|---|---|---|---|---|
| `DT-001` | `[Decisión]` | `[Opciones]` | `[Motivo]` | `[Propuesta / Aprobada]` |

## 5. Trazabilidad de reglas

| Regla AF | Implementación | Componente | Caso funcional | Prueba técnica |
|---|---|---|---|---|
| `RN-001` | `[Cómo se cumple]` | `[Nombre]` | `CP-001` | `PT-001` |

Ninguna regla confirmada puede quedar sin implementación y prueba.

## 6. Datos y base de datos

| Objeto | Cambio | Datos existentes | Migración / inicialización | Reversión |
|---|---|---|---|---|
| `[Tabla / Campo / SP / Índice / No aplica]` | `[Detalle]` | `[Impacto]` | `[Acción]` | `[Rollback]` |

Documentar:

- nulabilidad y valores iniciales;
- claves e integridad;
- transacciones;
- compatibilidad;
- migración;
- volumen;
- índices;
- auditoría;
- replicación.

## 7. Interfaces, mensajes y permisos

| Interfaz | Cambio | Validaciones / mensajes | Permiso | Estados |
|---|---|---|---|---|
| `[Pantalla / API / No aplica]` | `[Detalle]` | `[Comportamiento]` | `[Rol]` | `[Estados]` |

## 8. Integraciones, APIs y replicación

| Componente | Impacto | Contrato / datos | Errores y reintentos | Compatibilidad |
|---|---|---|---|---|
| `[Nombre / No aplica]` | `[Detalle]` | `[Contrato]` | `[Tratamiento]` | `[Versiones]` |

## 9. Seguridad, auditoría y privacidad

| Aspecto | Requisito | Implementación | Evidencia |
|---|---|---|---|
| `[Permiso / Auditoría / Dato sensible]` | `[Necesidad]` | `[Solución]` | `[Prueba]` |

## 10. Excepciones y errores

| Código | Situación | Detección | Respuesta técnica | Resultado funcional |
|---|---|---|---|---|
| `ET-001` | `[Error]` | `[Cómo se detecta]` | `[Tratamiento]` | `[Resultado]` |

## 11. Pruebas técnicas

| Código | Tipo | Preparación | Ejecución | Resultado esperado | Reglas |
|---|---|---|---|---|---|
| `PT-001` | `[Unitaria / Integración / Datos]` | `[Datos]` | `[Pasos]` | `[Resultado]` | `[RN-001]` |

## 12. Pruebas de regresión

| Proceso relacionado | Motivo | Prueba | Resultado esperado |
|---|---|---|---|
| `[Proceso]` | `[Componente compartido]` | `[Escenario]` | `[Resultado]` |

## 13. Riesgos técnicos

| Código | Riesgo | Consecuencia | Probabilidad | Mitigación |
|---|---|---|---|---|
| `RT-001` | `[Evento]` | `[Impacto]` | `[Alta / Media / Baja]` | `[Prevención]` |

## 14. Instalación, actualización y reversión

| Orden | Acción | Responsable | Validación | Reversión |
|---:|---|---|---|---|
| 1 | `[Script / Archivo / Configuración]` | `[Nombre]` | `[Control]` | `[Acción]` |

## 15. Estimación y dependencias

| Actividad | Responsable | Estimación | Dependencia | Observaciones |
|---|---|---|---|---|
| `[Análisis / Desarrollo / Prueba / Script / Documentación]` | `[Nombre]` | `[Horas / días]` | `[Dependencia]` | `[Detalle]` |

La estimación se realiza después de completar el impacto y el diseño.

## 16. Condiciones para iniciar desarrollo

- AF aprobado.
- Pendientes críticos resueltos.
- Funcionamiento actual relevado.
- Objetos y dependencias identificados.
- Impacto en datos, replicación, reportes y seguridad evaluado.
- Casos de prueba definidos.
- Estimación aprobada.
- Instalación y reversión preparadas.

## 17. Historial y aprobaciones

| Versión | Fecha | Autor | Cambio | Estado |
|---|---|---|---|---|
| `0.1` | `[Fecha]` | `[Autor]` | `Documento inicial` | `Borrador` |

