# Protocolo de aplicación real en Central

## Propósito

Este protocolo define cómo ejecutar la primera aplicación real del marco en Central sin contaminar la evaluación. Su función es guiar la captura de `E-GH-INT-01`, `E-GH-INT-02`, `E-GH-INT-03`, `E-TEST-INT-01` y `E-FORM-01`, manteniendo separadas la construcción documental, la intervención, la evaluación formativa y la evaluación sumativa.

## Condición de entrada

Antes de iniciar la aplicación, debe existir una tarea real de Central que sea pequeña, verificable y no ficticia. No se debe crear una solicitud de integración artificial solo para producir evidencia de tesis, porque eso debilitaría la validez ecológica de la evaluación.

La tarea seleccionada debe cumplir estos criterios mínimos:

| Criterio | Regla |
|:--|:--|
| Proyecto | Debe pertenecer a Central. |
| Componente | Central Odoo Backend, Central API o Central Frontend. |
| Responsable | Debe registrarse con código `DEV-001`, `DEV-002` o `DEV-003`. |
| Tamaño | Debe poder resolverse con una rama corta y una solicitud de integración. |
| Verificación | Debe permitir prueba, construcción, prueba de API o verificación manual documentada. |
| Evidencia | Debe permitir capturas o registros privados sin exponer datos sensibles. |

## Flujo obligatorio de aplicación

1. Registrar la tarea en Odoo o mecanismo equivalente, con código, responsable, componente y criterio mínimo de aceptación.
2. Crear la rama con el formato vigente: `<tipo>/<codigo-tarea>-<descripcion-corta>`.
3. Realizar commits con el formato vigente: `<tipo>(<codigo-tarea>): <descripcion-breve>`.
4. Crear solicitud de integración con título: `<tipo>(<codigo-tarea>): <descripcion breve>`.
5. Completar la plantilla de solicitud de integración.
6. Registrar evidencia de verificación técnica.
7. Registrar validación, revisión por tercero o excepción documentada.
8. Registrar fricciones de uso y decisión de rediseño.

## Evidencias a capturar

| Código | Momento | Qué debe mostrar | Archivo o soporte esperado |
|:--|:--|:--|:--|
| `E-GH-INT-01` | Al crear la solicitud de integración. | Rama, título de solicitud, repositorio, componente y vínculo con tarea. | Captura privada o registro anonimizado. |
| `E-GH-INT-02` | Antes de fusionar. | Plantilla completada: tarea, resumen, riesgo, verificación y validación. | Captura privada de la solicitud. |
| `E-GH-INT-03` | Antes o después de fusionar. | Commits con formato conforme y código de tarea. | Captura o exportación de historial. |
| `E-TEST-INT-01` | Antes de aprobar o fusionar. | Resultado de prueba, construcción, prueba de API o verificación manual documentada. | Captura de consola, registro, evidencia de herramienta o acta breve. |
| `E-FORM-01` | Al terminar el primer uso. | Fricciones, desviaciones, dudas y ajustes propuestos. | Bitácora formativa. |

## Bitácora mínima de fricción formativa

Cada fricción debe registrarse con esta estructura:

| Campo | Contenido requerido |
|:--|:--|
| Código de fricción | `F-001`, `F-002`, etc. |
| Evidencia relacionada | `E-GH-INT-01`, `E-TEST-INT-01` u otra. |
| Regla afectada | Rama, commit, solicitud, plantilla, verificación o validación. |
| Qué ocurrió | Descripción breve y factual. |
| Por qué importa | Riesgo para trazabilidad, aplicabilidad o verificación. |
| Rediseño propuesto | Ajuste a estándar, plantilla, ejemplo o comunicación. |
| Decisión | Aceptado, rechazado o pendiente. |

## Criterio para declarar evaluación formativa ejecutada

La evaluación formativa podrá declararse ejecutada solo si existe, como mínimo:

1. una solicitud de integración real posterior al marco en Central;
2. evidencia de rama, commits, título y plantilla;
3. evidencia técnica de verificación;
4. registro de al menos una fricción o confirmación explícita de ausencia de fricciones;
5. decisión de rediseño V1.1-Central o justificación de no rediseñar.

Si falta cualquiera de estos elementos, E8 seguirá siendo plan de evaluación, no evaluación ejecutada.

## Reglas de confidencialidad

Las capturas deben mantenerse en la carpeta privada de evidencias. En documentos públicos de tesis se deben usar códigos de participante, nombres genéricos de componente y descripciones técnicas no sensibles. No se deben exponer nombres completos de desarrolladores, enlaces privados, credenciales, código fuente sensible ni datos de clientes.

## Estado del protocolo

Este protocolo queda listo para usar en la primera tarea real de Central. No sustituye la evaluación; solo define cómo capturar evidencia válida para cerrar E8 formativa y alimentar E9 y E10.

## Tarea seleccionada para primera aplicación

El 2026-10-13 se seleccionó la tarea `CCC-7336`: validar pruebas unitarias en la API de CCC. Esta tarea es metodológicamente adecuada para la primera aplicación porque pertenece a Central, se ubica en el componente API, permite observar trazabilidad desde tarea hasta solicitud de integración y puede producir evidencia técnica directa para `E-TEST-INT-01`.

| Campo | Valor |
|:--|:--|
| Código de tarea | `CCC-7336` |
| Descripción operativa | Validar pruebas unitarias en API de CCC. |
| Proyecto | Central |
| Componente | Central API |
| Responsable codificado | `DEV-002` si ejecuta el responsable de API; `DEV-003` si ejecuta el tesista. Debe confirmarse antes de registrar la evidencia. |
| Evidencia principal esperada | `E-GH-INT-01`, `E-GH-INT-02`, `E-GH-INT-03`, `E-TEST-INT-01`, `E-FORM-01`. |
| Relevancia para indicadores | I3, I4, I5, I6, I7 e I9. |

### Nombres recomendados para esta tarea

Para mantener conformidad con `STD-GIT-001`, `STD-GIT-002` y `STD-GIT-003`, se recomienda usar:

```text
Rama: test/CCC-7336-validar-tests-unitarios-api
Commit: test(CCC-7336): validar tests unitarios en API de CCC
Solicitud de integración: test(CCC-7336): validar tests unitarios en API de CCC
```

Si durante la ejecución se corrige configuración de pruebas, dependencias o canalización de construcción, puede usarse un commit adicional de tipo `config`, por ejemplo:

```text
config(CCC-7336): ajustar configuración de pruebas unitarias
```

La evidencia técnica mínima para `E-TEST-INT-01` deberá incluir el comando ejecutado, el resultado obtenido y la fecha de ejecución. Si las pruebas fallan, el fallo no invalida la evidencia; al contrario, puede ser hallazgo formativo si se registra qué regla, configuración o instrucción del marco debe ajustarse.
