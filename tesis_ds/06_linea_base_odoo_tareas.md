# Línea base específica del tablero de tareas en Odoo

## Propósito

Este documento registra la línea base de visibilidad del trabajo en el tablero interno de tareas implementado en Odoo antes de aplicar el marco ligero. La medición se concentra en si las tareas reales del equipo están registradas, asignadas, desagregadas y trazables hacia trabajo técnico observable. No se evalúa desempeño individual; se evalúa la capacidad del proceso actual para hacer visible el trabajo.

## Ventana de observación

La ventana principal de observación de línea base es del **21 de septiembre de 2026** al **4 de octubre de 2026**. Cuando se use evidencia histórica previa a esa ventana, debe declararse como contexto y no como conteo principal del periodo.

## Registro PConst: ticket amplio de backend y frontend

| Campo | Valor |
|:--|:--|
| Proyecto | PConst |
| Componentes afectados | Backend y frontend |
| Cantidad de tareas Odoo visibles en la ventana | 1 tarea principal; luego subdividida por el tesista en subtareas. |
| Descripción breve del ticket principal | Crear servicios y pantallas para clientes, proyectos y archivos de proyectos, incluyendo endpoints, pantallas frontend, subida de archivos a AWS S3 y generación de enlaces firmados temporales. |
| ¿El ticket agrupa varias actividades técnicas? | Sí. |
| Responsable codificado | DEV-003 |
| Estado del ticket | Finalizado. |
| Fecha de creación o actualización | Creado en mayo; programado en junio con 29,5 horas ejecutadas de 32 disponibles. El ticket evidencia que el desarrollo debía haberse realizado en febrero. |
| Evidencia disponible | Ticket principal de servicio en Odoo, denominado por el tesista como “superticket”. |
| Observación metodológica | El ticket concentra varias funcionalidades y actividades técnicas en una sola unidad de trabajo. Esto reduce la visibilidad del avance, dificulta priorización, asignación y seguimiento, y obliga a reconstruir el trabajo real mediante subtareas posteriores. |

## Actividades reales agrupadas dentro del ticket

| Grupo | Actividad identificada |
|:--|:--|
| Backend - clientes | Crear endpoints para crear, editar, obtener, listar y eliminar clientes. |
| Backend - proyectos | Crear endpoints para crear, editar, obtener, listar y eliminar proyectos. |
| Backend - archivos | Crear endpoints para crear, editar, obtener, listar y eliminar archivos de proyectos. |
| Integración con AWS S3 | Subir archivos a un bucket S3. |
| Acceso a archivos | Generar enlaces públicos firmados para acceder a documentos por tiempo limitado. |
| Frontend - clientes | Construir gestión de clientes. |
| Frontend - proyectos | Construir gestión de proyectos. |
| Frontend - archivos | Construir manejo de archivos. |
| Verificación | Desarrollar pruebas. |
| Configuración | Definir configuraciones compartidas en la API. |

## Subtareas creadas posteriormente por el tesista

| Código interno | Subtarea |
|:--|:--|
| ST-01 | Desarrollar servicios REST de clientes. |
| ST-02 | Desarrollar servicios REST de proyectos. |
| ST-03 | Desarrollar servicios REST de archivos de proyecto. |
| ST-04 | Frontend: gestión de clientes. |
| ST-05 | Frontend: gestión de proyectos. |
| ST-06 | Frontend: manejo de archivos. |
| ST-07 | Desarrollo de pruebas. |
| ST-08 | Configuraciones compartidas en API. |

## Contenido funcional resumido del ticket principal

El ticket de servicio corresponde al proyecto PConst Platform y agrupa el desarrollo de un módulo completo de clientes, proyectos y archivos. El backend usa Express.js, TypeScript, AWS Lambda y Supabase; el frontend usa Angular y PrimeNG. El ticket incluye creación de tablas en Supabase, endpoints protegidos para clientes, proyectos y archivos, configuración de AWS S3, subida y eliminación de archivos, generación de enlaces de acceso y pantallas de gestión en frontend.

El ticket también incluye criterios de aceptación funcional, configuración de rutas protegidas, uso de `authMiddleware`, integración con `HttpClient`, componentes PrimeNG y reglas de eliminación en cascada. Además, se añadió el campo de estado del proyecto con los siguientes valores: **En proceso**, **Atascado**, **Inactivo**, **Completado** y **Pre-construcción**.

## Hallazgo de línea base

El caso PConst muestra que una sola tarea visible en Odoo puede contener múltiples actividades de backend, frontend, integración, pruebas, configuración y despliegue. Aunque el ticket es detallado, su granularidad es demasiado amplia para controlar avance por componente, detectar bloqueos tempranos y relacionar cambios técnicos con unidades pequeñas de trabajo. Para la investigación, este caso aporta evidencia de baja visibilidad operativa: el trabajo existía, pero estaba agrupado de forma que dificultaba seguimiento, priorización y trazabilidad fina.

## Relación con indicadores

| Indicador | Interpretación para PConst |
|:--|:--|
| I1. Visibilidad de tareas activas | Existe una tarea visible, pero de granularidad excesiva. Debe contarse como tarea visible, con observación de baja desagregación. |
| I9. Evidencia trazable para respaldo de entregables | La trazabilidad es parcial: existe ticket, pero la relación tarea → subtarea → rama/commit → solicitud de integración → evidencia de verificación no está completa dentro del registro original. |

## Limitaciones de información en proyectos Odoo

Para Central Backend Odoo y Ansular Backend Odoo, el tesista no cuenta todavía con información suficiente del tablero de tareas Odoo. Esta ausencia no debe ocultarse ni completarse con inferencias. Se registrará como limitación de línea base y como evidencia de que la visibilidad del trabajo no está distribuida de forma homogénea entre componentes y responsables.

| Proyecto | Estado de información de tareas | Tratamiento metodológico |
|:--|:--|:--|
| Central Backend Odoo | Información insuficiente al momento de la línea base. | Pendiente de confirmación con desarrolladores o responsables Odoo. |
| Ansular Backend Odoo | Información insuficiente al momento de la línea base. | Pendiente de confirmación con desarrolladores o responsables Odoo. |

## Evidencia contextual Central: ticket pequeño de frontend y API

Este registro corresponde a evidencia histórica fuera de la ventana principal de línea base. No se contabiliza como tarea activa entre el 21 de septiembre de 2026 y el 4 de octubre de 2026, pero sí se conserva como evidencia contextual de que, en Central Frontend, el tesista ha comenzado a separar solicitudes en tareas pequeñas y trazables.

| Campo | Valor |
|:--|:--|
| Proyecto | Central |
| Componentes afectados | Frontend y API |
| Fecha del ticket | 1 de septiembre de 2026 |
| Fecha de finalización | 9 de septiembre de 2026 |
| Descripción breve del ticket | Incluir campos de información del operador en la creación y visualización de contratos. |
| Campos agregados | `operatorName` y `operatorCode`. |
| Origen de los datos | `operatorCode` capturado desde el inicio de sesión; `operatorName` obtenido desde la respuesta del inicio de sesión. |
| Cambio posterior identificado | Se agregó el campo `isOperatorRequired` en el inicio de sesión para determinar si debe enviarse la información del operador, incluso cuando no se cumplan otras condiciones, especialmente para usuarios de AAAgency. |
| ¿Agrupa varias actividades técnicas? | Parcialmente. El ticket es pequeño, pero involucró coordinación entre frontend y API. |
| Estado del ticket | Finalizado. |
| Evidencia disponible | Ticket compartido de Central donde también registró horas el desarrollador encargado del API. |
| Observación metodológica | El ticket muestra una práctica más granular en Central, porque el tesista registra o solicita tareas pequeñas y el desarrollador del API registró horas en el mismo ticket. La trazabilidad frontend ↔ API queda mejor respaldada que en la versión preliminar, aunque todavía debe verificarse si los cambios del API quedaron vinculados a commits o solicitudes de integración. |

### Actividades reales identificadas

| Área | Actividad |
|:--|:--|
| Frontend | Capturar `operatorCode` desde el inicio de sesión. |
| Frontend | Capturar `operatorName` desde la respuesta del inicio de sesión. |
| Frontend | Enviar `operatorName` y `operatorCode` al crear contrato. |
| Frontend | Incluir los campos de operador en la lista de contratos. |
| API | Ajustar el inicio de sesión para devolver `isOperatorRequired`. |
| API | Definir mediante validación del API si debe enviarse información del operador para usuarios de AAAgency. |

### Evidencia histórica de Central Frontend asociada al ticket CCC-4407

Esta evidencia corresponde al 2 de septiembre de 2026, por lo que queda fuera de la ventana principal de línea base. Se registra como evidencia contextual histórica porque muestra un intento del tesista de estandarizar la trazabilidad entre ticket, rama, solicitud de integración y commits.

| Campo | Valor |
|:--|:--|
| Proyecto | Central |
| Componente | Frontend |
| Ticket relacionado | CCC-4407 |
| Solicitud de integración | `Feature/ctn 4407 refactor contract list - #24` |
| Rama | `feature/CCC-4407` |
| Destino de la solicitud de integración | `test` |
| Estrategia de integración | `squash merge` al fusionar la solicitud de integración. |
| Fecha | 2 de septiembre de 2026 |
| ¿Está dentro de la ventana 21-09-2026 a 04-10-2026? | No |
| Uso en la tesis | Evidencia contextual histórica; no se contabiliza en indicadores principales de línea base. |

| Hash parcial | Mensaje | Observación |
|:--|:--|:--|
| `e28385f` | `feature(CCC-4407):Se almacena la información sobre si es usuario aaagency, basandose en el campo isOperatorRequired` | Evidencia de asociación entre commit y ticket. |
| `c6b50ab` | `feature(CCC-4407): - Actualizacion del operator code, obtenido desde el login al iniciar sesion, y no desde el response en el login, se agrega un nuevo campo loginUserName` | Evidencia de cambio funcional asociado al inicio de sesión. |
| `7ab8525` | `feature(CCC-4407): - Se muestra la información del operador en la lista de contratos` | Evidencia de cambio de visualización en lista de contratos. |

Autor codificado de la evidencia histórica de Central Frontend: `DEV-003`.

Aunque los commits muestran una convención práctica al incluir el código `CCC-4407`, la convención todavía no cuenta como estándar institucional documentado. La solicitud de integración desde `feature/CCC-4407` hacia `test` y el uso de `squash merge` muestran una práctica técnica ordenada en este caso, pero para la línea base formal se interpreta como práctica local promovida por el tesista, no como regla homogénea de PRX.

El tesista aclara que esta práctica fue introducida progresivamente por él desde que asumió el componente Central Frontend. Antes de esa intervención, el proyecto no estaba gestionado de forma estable en GitHub institucional; cuando el repositorio fue entregado, contenía un único commit inicial. Por tanto, este caso no debe presentarse como práctica institucional previa, sino como antecedente práctico y motivación directa de la propuesta: convertir prácticas aisladas aplicadas por una persona en un marco común para el equipo de desarrollo de software, responsables técnicos y jefes de proyecto.

### Interpretación para línea base

Este caso no debe mezclarse con los indicadores principales de la ventana 21-09-2026 a 04-10-2026. Su valor está en mostrar contraste: en Central existe una práctica de registrar una tarea pequeña compartida entre frontend y API, incluso con horas registradas por el desarrollador encargado del API, mientras que en otros componentes todavía hay menor visibilidad o evidencia incompleta. Esta diferencia interna refuerza la necesidad de un marco común, porque las prácticas dependen de la persona o componente y no de un estándar institucional.

## Pendientes para cerrar esta línea base de tareas

- Guardar evidencia del ticket principal de PConst, ocultando datos sensibles si corresponde.
- Guardar evidencia del ticket de Central sobre información del operador y de la solicitud de integración `#24`, ocultando datos sensibles si corresponde.
- Confirmar si las subtareas creadas por el tesista quedaron registradas en Odoo o solo fueron desagregación operativa externa.
- Verificar, si es posible, los commits o solicitudes de integración del API relacionados con el cambio `isOperatorRequired` en Central.
- Obtener, si es posible, al menos una captura o exportación de tareas de Central Backend Odoo y Ansular Backend Odoo.
- Consolidar el indicador I1 con el resto de proyectos observados.
