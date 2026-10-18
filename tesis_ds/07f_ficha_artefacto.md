# E7f. Ficha del artefacto

## Identificación del artefacto

| Campo | Descripción |
|:--|:--|
| Nombre | Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización. |
| Versión documentada | V1.0-Central. |
| Tipología Design Science | Marco, con componentes de método, reglas mínimas, plantillas operativas, estándares, indicadores y niveles de adopción. |
| Contexto de primera aplicación | Proyecto Central de PRX: Central Odoo Backend, Central API y Central Frontend. |
| Estado actual | Construido documentalmente e instanciado parcialmente; pendiente de aplicación completa en una solicitud de integración real y evidencia técnica de verificación. |
| Archivos base | `07b_requisitos.md`, `07c_diseno_artefacto.md`, `07c_plantilla_solicitud_integracion.md`, `07d_plan_construccion.md`, `07e_construccion_verificacion.md`. |

## Problema que resuelve

El artefacto responde al problema de diseño observado en la línea de software a medida de PRX: la ausencia de una ruta ligera, común y verificable para adoptar prácticas mínimas de gestión técnica desde el inicio de los proyectos y producir evidencia verificable del trabajo realizado. La línea base mostró prácticas parciales y heterogéneas: repositorios dispersos, convenciones no documentadas, solicitudes de integración sin evidencia mínima de verificación, tareas de granularidad desigual y trazabilidad incompleta entre tarea, rama, commit, solicitud de integración y validación.

El problema de investigación —que en el formato institucional se registrará como problema científico— se formula como la brecha sobre cómo diseñar marcos ligeros de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de desarrollo con baja estandarización. Por tanto, el artefacto no se reduce a configurar GitHub ni a publicar documentos internos; esos elementos son instanciaciones de una solución de diseño más general.

## Alcance de la versión V1.0-Central

La versión V1.0-Central se concentra en hacer observable la cadena mínima de trazabilidad técnica. No pretende certificar procesos, implementar CMMI, adoptar ISO/IEC 29110 de forma completa ni automatizar todos los controles. La prioridad es producir evidencia suficiente para iniciar evaluación formativa.

| Incluido en V1.0-Central | Fuera de alcance inicial |
|:--|:--|
| Convención mínima de ramas. | Renombramiento masivo de ramas históricas. |
| Convención mínima de commits. | Reescritura de historial de commits. |
| Estándar mínimo de solicitudes de integración. | Revisión independiente obligatoria en todos los casos. |
| Plantilla operativa de solicitud de integración. | Validación automática obligatoria de todos los campos. |
| Organización documental de estándares técnicos. | Tablero automatizado de cumplimiento. |
| Repositorio organizacional `.github` como instanciación PRX. | Canalización CI/CD completa. |
| Registro de fricciones iniciales. | Evaluación sumativa final sin rediseño previo. |

## Componentes del marco

| Componente | Propósito | Producto operativo en V1.0-Central | Evidencia disponible |
|:--|:--|:--|:--|
| C0. Precondiciones y gobernanza mínima | Definir condiciones mínimas de aplicación: responsables, repositorio o excepción, y mecanismo de tareas. | Codificación de participantes y delimitación de Central. | `06_codificacion_participantes.md`; `07b_requisitos.md`. |
| C1. Gestión visible del trabajo | Evitar trabajo invisible o tareas demasiado amplias. | Reglas de tarea válida y criterio de división. | Línea base Odoo; pendiente de aplicación posterior en Central. |
| C2. Trazabilidad del código | Vincular rama y commit con tarea. | `STD-GIT-001`; `STD-GIT-003`. | `E-ORG-INT-01`; `E-ORG-INT-04`; `E-ORG-INT-05`; `E-GH-ORG-01`. |
| C3. Integración y revisión de cambios | Estandarizar solicitud de integración como punto de control. | Plantilla operativa de PR; `STD-GIT-002`; repositorio `.github`. | `E-ORG-INT-02`; `E-ORG-INT-03`; `E-ORG-INT-05`; `E-GH-ORG-01`. |
| C4. Verificación técnica básica | Exigir método y evidencia de verificación. | Sección de verificación en plantilla PR. | Pendiente `E-TEST-INT-01`. |
| C5. Entrega y configuración básica | Registrar ambiente, rama o versión, fecha, responsable y mecanismo. | Regla definida en diseño; aplicación pendiente. | Pendiente de aplicación en entrega real. |
| C6. Seguimiento y mejora | Registrar indicadores, fricciones, excepciones y rediseño. | Plan de evidencias y registro de fricción por nombre de rama. | `06_plan_evidencias_privadas.md`; `E-GH-ORG-01`. |

## Reglas mínimas del artefacto

### Ramas

Toda rama temporal de trabajo debe seguir el formato:

```text
<tipo>/<codigo-tarea>-<descripcion-corta>
```

Ejemplo:

```text
feat/CCC-4407-operador-contrato
```

Las ramas permanentes de la convención institucional vigente son `main`, `Stage` y `Production`, aplicadas según el mecanismo real de despliegue. Las ramas históricas no deben renombrarse sin revisar dependencias, automatizaciones u Odoo.sh.

### Commits

Todo commit relevante debe seguir el formato:

```text
<tipo>(<codigo-tarea>): <descripcion-breve>
```

Ejemplo:

```text
feat(CCC-4407): agregar datos del operador en contratos
```

La convención toma como referencia Conventional Commits 1.0.0, pero en PRX el campo entre paréntesis se usa para el código de tarea.

### Solicitudes de integración

Toda solicitud de integración debe tener título trazable:

```text
<tipo>(<codigo-tarea>): <descripcion breve>
```

Además, debe completar la plantilla operativa con tarea relacionada, resumen, cambios principales, componentes afectados, archivos modificados, comportamiento esperado, riesgo, plan de prueba, verificación realizada, evidencia, validación y lista mínima de control.

### Validación progresiva

El marco distingue entre solicitud trazable, plantilla completa, auto-validación documentada, validación automática y revisión por tercero. La auto-validación documentada se acepta como excepción cuando un componente tiene un solo responsable o no existe disponibilidad real de revisor independiente.

### Verificación mínima

Cada cambio funcional debe declarar qué se verificó, cómo se verificó y con qué evidencia. La evidencia puede ser prueba unitaria, prueba de integración, prueba de API, construcción, prueba manual documentada o justificación de no aplicabilidad.

## Estándares y productos operativos construidos

| Código | Producto | Función | Evidencia |
|:--|:--|:--|:--|
| `STD-GIT-001` | Convención mínima de ramas. | Define ramas permanentes, ramas temporales, tipos permitidos, procedimiento y excepciones. | `E-ORG-INT-01`. |
| `STD-GIT-002` | Convención mínima de solicitudes de integración. | Define título de PR, uso de plantilla, solicitud válida, validación y excepciones. | `E-ORG-INT-03`. |
| `STD-GIT-003` | Convención mínima de commits. | Define formato de commits, tipos permitidos, relación con tarea, squash y validación mínima. | `E-ORG-INT-04`. |
| `pull_request_template.md` | Plantilla operativa de solicitud de integración. | Estructura la descripción del PR y obliga a declarar evidencia mínima. | `E-ORG-INT-02`; `E-GH-ORG-01`. |
| Estructura SharePoint | Organización documental de estándares. | Ubica estándares Git y Pull Request en carpetas diferenciadas. | `E-ORG-INT-05`. |

## Evidencias disponibles

| Evidencia | Momento | Qué demuestra | Indicadores relacionados |
|:--|:--|:--|:--|
| `E-ORG-INT-01` | Intervención | Publicación de `STD-GIT-001 — Convención mínima de ramas`. | I3, I4, I9. |
| `E-ORG-INT-02` | Intervención | Publicación de la plantilla operativa de solicitud de integración. | I5, I6, I9. |
| `E-ORG-INT-03` | Intervención | Publicación de `STD-GIT-002 — Convención mínima de solicitudes de integración`. | I5, I6, I9. |
| `E-ORG-INT-04` | Intervención | Publicación de `STD-GIT-003 — Convención mínima de commits`. | I4, I9. |
| `E-ORG-INT-05` | Intervención | Estructura documental de estándares técnicos en SharePoint. | I3, I4, I5, I6, I9. |
| `E-GH-ORG-01` | Intervención | Repositorio `.github` y rama de configuración de plantilla PR. | I3, I5, I6, I9. |

## Instanciación PRX

En PRX, el marco se instancia mediante SharePoint para documentación institucional y GitHub para repositorios, ramas, commits y solicitudes de integración. El repositorio organizacional `.github` cumple la función de distribuir la plantilla de solicitud de integración, mientras que los estándares publicados en SharePoint funcionan como fuente normativa interna.

Esta instanciación no define universalmente el artefacto. Otro equipo con herramientas distintas podría aplicar el mismo marco usando GitLab, Azure DevOps, Jira, Confluence u otra combinación, siempre que conserve los productos de trabajo equivalentes: tarea, rama, commit, solicitud de integración, evidencia de verificación y registro de validación.

## Fricciones y limitaciones conocidas

| Limitación o fricción | Evidencia | Implicación |
|:--|:--|:--|
| La rama `config/ADM-4940_config_pr_template` usa guion bajo en la descripción. | `E-GH-ORG-01`. | La convención fue adoptada parcialmente; debe reforzarse el uso de guiones en la descripción corta. |
| Aún no existe una solicitud de integración real de Central que use toda la cadena del marco. | Pendiente `E-GH-INT-01`. | No se puede afirmar todavía evaluación de campo completa. |
| Aún falta evidencia técnica de verificación en un componente crítico de Central. | Pendiente `E-TEST-INT-01`. | I7 sigue débil para evaluación sumativa. |
| La publicación en SharePoint evidencia disponibilidad, no adopción efectiva por todos los desarrolladores. | `E-ORG-INT-01` a `E-ORG-INT-05`. | Debe complementarse con uso real y evaluación formativa. |

## Instrucciones mínimas de aplicación

1. Confirmar que existe una tarea asociada al cambio.
2. Crear rama temporal desde `main` usando `STD-GIT-001`.
3. Realizar commits con código de tarea usando `STD-GIT-003`.
4. Abrir solicitud de integración hacia `main`.
5. Nombrar la solicitud según `STD-GIT-002`.
6. Completar la plantilla operativa de solicitud de integración.
7. Registrar verificación realizada y evidencia.
8. Indicar validación: revisión por tercero, auto-validación documentada, validación automática o excepción.
9. Fusionar con `squash merge` cuando corresponda, conservando código de tarea.
10. Eliminar rama temporal después de fusionar.

## Criterio de reproducibilidad

Otro investigador o practicante puede reproducir el artefacto si dispone de:

- definición de componentes C0-C6;
- estándares `STD-GIT-001`, `STD-GIT-002` y `STD-GIT-003`;
- plantilla operativa de solicitud de integración;
- criterios de tarea válida, solicitud válida y evidencia mínima;
- indicadores I1-I9;
- separación entre línea base, intervención y evaluación;
- registro de fricciones y excepciones.

La reproducción no exige usar SharePoint ni GitHub, pero sí exige conservar productos de trabajo equivalentes y evidencias observables.

## Estado del artefacto para evaluación

El artefacto está **listo como versión construida documentalmente e instanciada parcialmente**. Está en condiciones de pasar a una primera aplicación real controlada en Central, pero todavía no debe presentarse como evaluado. Para habilitar evaluación formativa se requiere, como mínimo, una solicitud de integración real posterior al marco y una evidencia técnica de verificación.

## Estado del gate E7f

E7f queda **suficiente como ficha reproducible inicial del artefacto**. La ficha consolida identificación, alcance, componentes, reglas, productos operativos, evidencias, instanciación PRX, limitaciones e instrucciones mínimas de aplicación. El siguiente paso es preparar E8 con evaluación formativa, incorporando `E-GH-INT-01`, `E-TEST-INT-01` y las fricciones observadas durante el uso real.
