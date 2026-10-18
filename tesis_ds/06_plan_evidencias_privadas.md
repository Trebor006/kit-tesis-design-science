# Plan de evidencias privadas

## Propósito

Este documento organiza las capturas, enlaces internos y registros privados que respaldarán la línea base, la intervención y la evaluación del marco. No debe publicarse con datos sensibles, nombres completos de desarrolladores, enlaces privados ni código de la empresa. En la tesis pública se usarán códigos de evidencia y participantes anonimizados.

## Regla metodológica

Las evidencias deben separarse en tres momentos:

1. **Línea base:** evidencia observada antes de aplicar el marco.
2. **Intervención:** evidencia de construcción o aplicación inicial del artefacto.
3. **Evaluación:** evidencia generada después de aplicar el marco.

Mezclar estos momentos debilita la evaluación. Si una captura se toma después, pero muestra un hecho histórico anterior, debe anotarse la fecha de captura y la fecha real del evento observado.

## Categorías de evidencia

| Código | Categoría | Uso |
|:--|:--|:--|
| `E-GH` | GitHub y repositorios | Repositorios, ramas, commits, solicitudes de integración y configuración organizacional. |
| `E-ODOO` | Tareas Odoo | Tareas, responsables codificados, estados, criterios y granularidad. |
| `E-TEST` | Pruebas y verificación | Salidas de pruebas, construcción, pruebas manuales documentadas o evidencia técnica equivalente. |
| `E-DELIV` | Entrega y despliegue | Ambientes, ramas desplegadas, versiones, fechas y responsables. |
| `E-ORG` | Organización y gobernanza | Responsables, excepciones, repositorios oficiales y decisiones de configuración. |
| `E-FORM` | Evaluación formativa | Fricciones, cambios al marco, retroalimentación y rediseño. |
| `E-SUM` | Evaluación sumativa | Medición posterior, cumplimiento de indicadores y resultados comparativos. |

## Evidencias mínimas pendientes

| Código sugerido | Momento | Evidencia | Qué capturar | Relación con indicadores |
|:--|:--|:--|:--|:--|
| `E-GH-ORG-01` | Intervención | Repositorio organizacional `.github`. | Vista del repositorio `.github`, archivo `pull_request_template.md` y una solicitud nueva mostrando que la plantilla aparece. | I5, I6, I9. |
| `E-ORG-INT-01` | Intervención | Publicación de `STD-GIT-001 — Convención mínima de ramas` en SharePoint. | Captura del documento publicado, mostrando código, nombre, versión, estado, fecha y secciones principales de la convención. | I3, I4, I9. |
| `E-ORG-INT-02` | Intervención | Publicación o carga de la plantilla operativa de solicitud de integración. | Captura del documento o plantilla publicada, mostrando secciones de tarea relacionada, resumen, cambios, componentes, archivos, comportamiento esperado, riesgo, plan de prueba, verificación, validación y lista mínima. | I5, I6, I9. |
| `E-ORG-INT-03` | Intervención | Publicación del estándar `STD-GIT-002 — Convención mínima de solicitudes de integración`. | Captura del estándar publicado, mostrando reglas para título de la solicitud de integración, uso obligatorio de la plantilla, validación y excepciones. | I5, I6, I9. |
| `E-ORG-INT-04` | Intervención | Publicación del estándar `STD-GIT-003 — Convención mínima de commits`. | Captura del estándar publicado, mostrando formato de commits, tipos mínimos, ejemplos, reglas de redacción, relación con ramas y solicitudes de integración, excepciones y validación mínima. | I4, I9. |
| `E-ORG-INT-05` | Intervención | Organización documental de estándares técnicos en SharePoint. | Captura de carpetas y archivos de estándares técnicos, incluyendo `01 - Git` y `02 - Pull Request` con sus documentos correspondientes. | I3, I4, I5, I6, I9. |
| `E-GH-BASE-01` | Línea base | Repositorios institucionales y no institucionales. | Lista de repositorios observados, ubicación institucional o excepción, sin exponer enlaces públicos. | I2, I9. |
| `E-GH-BASE-02` | Línea base | Ramas permanentes heterogéneas. | Vista de ramas con `main`, `Production`, `Prod`, `Stage`, `Staging`, `TEST`, `test` u otras equivalencias observadas. | I3, RQ5.1. |
| `E-GH-BASE-03` | Línea base | Solicitudes de integración previas. | PRs fusionadas en la ventana base, mostrando ausencia o presencia de descripción, verificación y validación. | I5, I6. |
| `E-GH-BASE-04` | Línea base | Commits o ramas sin convención documentada. | Ejemplos anonimizados de ramas y commits antes del marco. | I3, I4. |
| `E-ODOO-BASE-01` | Línea base | Tareas Central. | Tareas del periodo base con estado, responsable codificado y componente, ocultando datos sensibles. | I1. |
| `E-ODOO-BASE-02` | Línea base | Tarea amplia o poco granular. | Ejemplo de tarea que agrupa varios objetivos o componentes, si aplica. | I1, RQ2, RQ3. |
| `E-TEST-BASE-01` | Línea base | Evidencia de pruebas existente o ausencia documentada. | Comando, salida, registro o constatación de que no existe evidencia ejecutable en componente crítico. | I7. |
| `E-GH-INT-01` | Intervención | Primera solicitud usando la plantilla. | PR creada después del marco con plantilla completada, tarea, verificación y validación. | I5, I6, I9. |
| `E-GH-INT-02` | Intervención | Cierre de solicitud de integración. | PR fusionada y eliminación posterior de rama temporal. | I3, I5, I9. |
| `E-GH-INT-04` | Intervención | Configuración de ramas permanentes en Central. | Creación de `main`, `Stage` y `Production`, y retiro de `master` cuando fue técnicamente seguro. | I3, RQ5.1, I9. |
| `E-ODOO-INT-01` | Intervención | Tarea real posterior al marco. | Tarea `CCC-7336` con proyecto, componente y responsable codificado. | I1, I9. |
| `E-ORG-INT-06` | Intervención / rediseño | Publicación de `STD-GIT-001` V1.1. | Actualización de ramas permanentes a `main`, `Stage` y `Production`. | I3, I9. |
| `E-TEST-INT-01` | Intervención | Verificación técnica en Central. | Ejecución de prueba unitaria, construcción, prueba de API o prueba manual documentada con resultado. | I7. |
| `E-FORM-01` | Evaluación formativa | Fricciones de uso del marco. | Comentarios, observaciones o casos donde la plantilla/regla necesitó ajuste. | Rediseño formativo. |
| `E-SUM-01` | Evaluación sumativa | Medición posterior. | Tabla comparativa línea base frente a periodo posterior en Central. | I1-I9. |

## Datos que debe registrar cada evidencia

| Campo | Descripción |
|:--|:--|
| Código de evidencia | Identificador único, por ejemplo `E-GH-ORG-01`. |
| Momento | Línea base, intervención, evaluación formativa o evaluación sumativa. |
| Fecha de captura | Día en que se tomó la captura o se descargó el registro. |
| Fecha del evento | Día del PR, commit, tarea, despliegue o prueba observada. |
| Fuente | GitHub, Odoo, terminal, repositorio, ambiente u otra fuente. |
| Proyecto/componente | Central Odoo, Central API, Central Frontend u otro contexto diagnóstico. |
| Participantes | Usar códigos `DEV-001` a `DEV-004`; no nombres completos. |
| Qué demuestra | Una oración concreta sobre el hecho respaldado. |
| Indicador relacionado | I1-I9, si aplica. |
| Sensibilidad | Alta, media o baja; definir si puede mostrarse en tesis pública o solo describirse. |

## Evidencias registradas

| Código | Archivos | Momento | Qué demuestra | Indicadores relacionados |
|:--|:--|:--|:--|:--|
| `E-ORG-INT-01` | `evidencias/E-ORG-INT-01_STD-GIT-001_convencion_minima_ramas_sharepoint - 1.png`; `evidencias/E-ORG-INT-01_STD-GIT-001_convencion_minima_ramas_sharepoint - 2.png`; `evidencias/E-ORG-INT-01_STD-GIT-001_convencion_minima_ramas_sharepoint - 3.png` | Intervención | Publicación en SharePoint del estándar `STD-GIT-001 — Convención mínima de ramas`, dividido en tres capturas por extensión del contenido. | I3, I4, I9. |
| `E-ORG-INT-02` | `evidencias/E-ORG-INT-02_plantilla_operativa_pull_request_sharepoint - 1.png`; `evidencias/E-ORG-INT-02_plantilla_operativa_pull_request_sharepoint - 2.png`; `evidencias/E-ORG-INT-02_plantilla_operativa_pull_request_sharepoint - 3.png` | Intervención | Publicación o carga de la plantilla operativa de solicitud de integración, dividida en tres capturas por extensión del contenido. Esta evidencia respalda la plantilla operativa que se completa en la descripción de la solicitud de integración. | I5, I6, I9. |
| `E-ORG-INT-03` | `evidencias/E-ORG-INT-03_STD-GIT-002_convencion_minima_solicitudes_integracion_sharepoint - 1.png`; `evidencias/E-ORG-INT-03_STD-GIT-002_convencion_minima_solicitudes_integracion_sharepoint - 2.png`; `evidencias/E-ORG-INT-03_STD-GIT-002_convencion_minima_solicitudes_integracion_sharepoint - 3.png`; `evidencias/E-ORG-INT-03_STD-GIT-002_convencion_minima_solicitudes_integracion_sharepoint - 4.png`; `evidencias/E-ORG-INT-03_STD-GIT-002_convencion_minima_solicitudes_integracion_sharepoint - 5.png`; `evidencias/E-ORG-INT-03_STD-GIT-002_convencion_minima_solicitudes_integracion_sharepoint - 6.png` | Intervención | Publicación del estándar `STD-GIT-002 — Convención mínima de solicitudes de integración`, diferenciado de la plantilla operativa e incluyendo reglas de título, descripción, validación y excepciones. | I5, I6, I9. |
| `E-ORG-INT-04` | `evidencias/E-ORG-INT-04_STD-GIT-003_convencion_minima_commits_sharepoint - 1.png`; `evidencias/E-ORG-INT-04_STD-GIT-003_convencion_minima_commits_sharepoint - 2.png`; `evidencias/E-ORG-INT-04_STD-GIT-003_convencion_minima_commits_sharepoint - 3.png`; `evidencias/E-ORG-INT-04_STD-GIT-003_convencion_minima_commits_sharepoint - 4.png`; `evidencias/E-ORG-INT-04_STD-GIT-003_convencion_minima_commits_sharepoint - 5.png` | Intervención | Publicación del estándar `STD-GIT-003 — Convención mínima de commits`, dividido en cinco capturas por extensión del contenido. | I4, I9. |
| `E-ORG-INT-05` | `evidencias/E-ORG-INT-05_estructura_estandares_tecnicos_sharepoint - 1.png`; `evidencias/E-ORG-INT-05_estructura_estandares_tecnicos_sharepoint - 2.png` | Intervención | Estructura documental en SharePoint: carpeta `Estandares tecnicos/01 - Git` con `STD-GIT-001-convencion-de-ramas.md` y `STD-GIT-003-convencion-de-commits.md`; carpeta `Estandares Tecnicos/02 - Pull Request` con `STD-GIT-002-convencion-de-pull-requests.md` y `STD-GIT-002-pull_request_template.md`. | I3, I4, I5, I6, I9. |
| `E-GH-ORG-01` | `evidencias/E-GH-ORG-01_repositorio_github_organizacional_ramas_template.png` | Intervención | Repositorio organizacional `.github` con rama `main` y rama temporal `config/ADM-4940_config_pr_template` para configuración de la plantilla de solicitudes de integración. La rama temporal evidencia adopción inicial, aunque el uso de guion bajo se registra como fricción frente a la convención definida. | I3, I5, I6, I9. |
| `E-ODOO-INT-01` | `evidencias/E-ODOO-INT-01_tarea_CCC-7336_validar_tests_unitarios_API_Central.png` | Intervención | Tarea real `CCC-7336` para validar pruebas unitarias en la API de Central. | I1, I9. |
| `E-GH-INT-01` | Cuatro capturas `evidencias/E-GH-INT-01_PR_CCC-7336_aplicacion_marco-01_titulo_rama_tarea_resumen - 01.png` a `- 04.png`. | Intervención | Solicitud de integración real `CCC-7336` con rama temporal, título conforme, relación con tarea y plantilla operativa completada. | I3, I4, I5, I6, I9. |
| `E-GH-INT-02` | `evidencias/E-GH-INT-02_PR_CCC-7336_cierre_integracion - 01_rama_eliminada.png`; `evidencias/E-GH-INT-02_PR_CCC-7336_cierre_integracion - 02_PR_fusionada.png`. | Intervención | Fusión de la solicitud de integración y eliminación de la rama temporal. | I3, I5, I9. |
| `E-GH-INT-04` | `evidencias/E-GH-INT-04_configuracion_ramas_permanentes_Central-01_creacion_main.png`; `evidencias/E-GH-INT-04_configuracion_ramas_permanentes_Central-02_creacion_Stage_Production.png`; `evidencias/E-GH-INT-04_configuracion_ramas_permanentes_Central-03_retiro_master.png`. | Intervención | Configuración de ramas permanentes `main`, `Stage` y `Production` y retiro de `master` en el repositorio intervenido. | I3, RQ5.1, I9. |
| `E-TEST-INT-01` | `evidencias/E-TEST-INT-01_CCC-7336_API_169_pruebas_unitarias_exitosas.png`. | Intervención | Ejecución satisfactoria de 169 pruebas unitarias en la API de Central. | I7. |
| `E-ORG-INT-06` | `evidencias/E-ORG-INT-06_STD-GIT-001_V1_1_actualizacion_ramas_permanentes_sharepoint - 01.png`; `evidencias/E-ORG-INT-06_STD-GIT-001_V1_1_actualizacion_ramas_permanentes_sharepoint - 02.png`. | Intervención / rediseño | Publicación de `STD-GIT-001` V1.1 con la convención `main`, `Stage` y `Production`. | I3, I9. |
| `E-FORM-01` | `tesis_ds/08_registro_formativo_CCC-7336.md`. | Evaluación formativa | Aplicación real sin fricción operativa reportada y ajuste contextual V1.1 documentado. | Rediseño formativo. |

## Reglas de anonimización

- No publicar nombres completos de desarrolladores.
- No publicar enlaces privados de repositorios, rutas internas, credenciales ni código sensible.
- Difuminar nombres de clientes si no son necesarios para la defensa.
- Mantener códigos de participantes: `DEV-001`, `DEV-002`, `DEV-003` y `DEV-004`.
- Si una captura contiene información sensible inevitable, conservarla solo como evidencia privada y describirla en la tesis con su código.

## Pendientes inmediatos

1. Registrar `E-SUM-01` con comparación posterior contra la línea base, después de definir su periodo de observación.
2. Antes de incorporar resultados en la tesis, mantener separada toda evidencia como línea base, intervención, evaluación formativa o evaluación sumativa.
