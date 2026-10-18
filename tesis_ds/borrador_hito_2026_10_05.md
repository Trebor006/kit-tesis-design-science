# Borrador del hito 2026-10-05: diagnóstico y propuesta del artefacto

## Propósito del borrador

Este borrador integra el diagnóstico de línea base y la decisión de diseño del artefacto para preparar el hito del 5 de octubre de 2026. No es todavía el capítulo final de la tesis; es una versión de trabajo para mostrar que el problema práctico fue observado con evidencia y que la propuesta no será una lista aislada de buenas prácticas, sino un marco ligero, progresivo y evaluable bajo Design Science.

## Estado metodológico

El trabajo se encuentra en cierre de E6 y entrada formal a E7. E6 ya cuenta con evidencia real de línea base en GitHub y en el tablero interno de tareas implementado en Odoo. E7a queda decidido a favor de un marco ligero progresivo, y el siguiente paso será convertir esa decisión en requisitos, diseño preliminar y plan de construcción.

## Problema confirmado por línea base

La línea de software a medida de PRX no carece completamente de prácticas técnicas; el problema es más preciso y más defendible: las prácticas existen de forma parcial, no homogénea y dependiente de personas o componentes. En Central Frontend, por ejemplo, el tesista introdujo prácticas de rama, solicitud de integración, referencia a ticket y fusión mediante `squash merge`, pero esa práctica no representa todavía un estándar institucional. En proyectos Odoo se observan solicitudes de integración, pero sin evidencia mínima de verificación. En otros componentes, como Central API o PConst, existen repositorios fuera de la organización institucional o trabajo no trazado dentro de la ventana observada.

Esta situación confirma el problema de diseño: PRX necesita una ruta ligera, común y verificable para adoptar prácticas mínimas de gestión técnica. El problema de investigación —que en el formato institucional se registrará como problema científico— se mantiene como la brecha sobre cómo diseñar marcos ligeros de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de desarrollo con baja estandarización.

## Evidencia resumida de línea base

| Fuente | Hallazgo principal | Implicación para el diseño |
|:--|:--|:--|
| GitHub | 3 de 7 componentes están en GitHub institucional de PRX; los demás permanecen en cuenta personal u otra organización. | El marco debe distinguir repositorio institucional, repositorio oficialmente reconocido y excepción documentada. |
| GitHub | No existe convención documentada de ramas ni de commits. | El marco debe exigir una convención mínima documentada, no solo prácticas informales. |
| GitHub | Hay 5 solicitudes de integración fusionadas en la ventana, pero 0 con evidencia mínima de verificación y sin garantía de revisión independiente. | El marco debe definir qué hace válida una solicitud de integración, qué evidencia mínima debe adjuntarse y cuándo se requiere revisor distinto del autor. |
| Odoo/tareas | PConst tuvo un ticket amplio que agrupó backend, frontend, AWS S3, pruebas y configuración. | El marco debe definir tarea válida, granularidad y criterio de división. |
| Evidencia histórica | Central Frontend muestra trazabilidad local introducida por el tesista. | La propuesta debe convertir prácticas individuales en reglas comunes, no presentar esas prácticas como estándar institucional previo. |
| Odoo/GitHub | Central API reporta cambios en la ventana que no fueron subidos al repositorio. | El marco debe hacer visible el trabajo no trazado y exigir vínculo entre tarea y cambio técnico. |

## Artefacto decidido

El artefacto se define como un **Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización**.

La tipología principal del artefacto es **marco**, con componentes de método, plantillas operativas, reglas mínimas, indicadores y niveles de adopción. No se trata de una guía genérica ni de una implantación directa de GitHub, Scrum, CMMI o ISO/IEC 29110. GitHub y Odoo son instanciaciones de PRX; el marco debe ser transferible analíticamente a equipos que usen otras herramientas equivalentes.

## Principios de diseño transversales

| Principio | Definición operacional |
|:--|:--|
| Ligereza | El marco exige el mínimo de reglas necesarias para producir visibilidad, trazabilidad y verificación básica; no intenta cubrir todos los procesos de Ingeniería de Software. |
| Progresividad | Las prácticas se adoptan por niveles; no se exige todo de golpe a un equipo con baja estandarización. |
| Verificabilidad | Toda regla debe producir evidencia observable por un tercero. Una afirmación de cumplimiento no basta. |
| Agnosticismo de herramienta | El marco define qué debe existir; PRX lo instancia con Odoo y GitHub, pero otra organización podría usar Jira, GitLab, Trello u otra combinación equivalente. |
| Trazabilidad bidireccional | Debe poder seguirse el hilo tarea ↔ rama ↔ commit ↔ solicitud de integración ↔ evidencia de verificación, y viceversa. |
| Responsabilidad mínima | Una persona puede cumplir varios roles, pero la responsabilidad de tarea, revisión, repositorio y excepción no debe quedar implícita. |

## Componentes del marco

| Componente | Problema que resuelve | Evidencia esperada |
|:--|:--|:--|
| C0. Precondiciones y gobernanza mínima | El marco no puede aplicarse si no existe soporte mínimo de trabajo técnico compartido. | Herramienta de tareas, control de versiones, responsable técnico, responsables de repositorio y mecanismo de excepción. |
| C1. Gestión visible del trabajo | El trabajo existe, pero no siempre está visible o está en tickets demasiado grandes. | Tareas con descripción, responsable, componente, criterio de aceptación, estado y criterio de terminado. |
| C2. Gestión y trazabilidad del código | Hay cambios de código sin vínculo claro con tareas o repositorios oficiales. | Repositorio oficial o excepción documentada, rama principal definida, ramas y commits vinculados a tarea. |
| C3. Integración y revisión de cambios | Puede existir solicitud de integración sin descripción, revisión real ni campos mínimos. | Solicitudes de integración con plantilla, tarea relacionada, revisor, componentes afectados y revisión mínima. |
| C4. Verificación técnica básica | Se entrega código sin evidencia verificable de prueba. | Método de verificación y evidencia asociada: pasos, resultado, prueba ejecutada, registro o captura contextualizada. |
| C5. Entrega y configuración básica | Puede desarrollarse código trazable, pero no saberse qué versión llegó a qué ambiente. | Registro mínimo de ambiente, versión/rama desplegada, responsable, fecha y mecanismo de despliegue. |
| C6. Seguimiento y mejora del marco | Sin medición, no se sabe si el marco fue adoptado ni qué debe ajustarse. | Indicadores de adopción, incumplimientos, excepciones y rediseño formativo. |

## Niveles de adopción del marco

Estos niveles no son un modelo de madurez ni una versión reducida de CMMI. Solo describen el grado de adopción del marco propuesto.

| Nivel | Nombre | Evidencia principal |
|:--|:--|:--|
| 0 | No estructurado | Trabajo sin prácticas mínimas consistentes; línea base con evidencia dispersa o incompleta. |
| 1 | Visible | Tareas y repositorios identificables. |
| 2 | Trazable | Relación tarea ↔ rama ↔ commit. |
| 3 | Revisado | Cambios integrados mediante solicitud de integración con revisor y plantilla mínima. |
| 4 | Verificado | Solicitudes de integración con evidencia válida de verificación técnica. |
| 5 | Entregable trazable | Se conoce qué versión llegó a qué ambiente, cuándo, cómo y por quién. |

## Alternativas consideradas

| Alternativa | Decisión | Justificación |
|:--|:--|:--|
| Guía operativa de buenas prácticas | Descartada como artefacto principal. | Sería rápida, pero débil como contribución de Design Science; se parecería a capacitación interna. |
| Método operativo paso a paso | Integrada como componente interno. | Aporta aplicabilidad, pero sola sería demasiado procedimental y dependiente del flujo de PRX. |
| Marco ligero progresivo | Seleccionada. | Integra prácticas, roles, reglas, plantillas, niveles e indicadores; permite evaluación y transferibilidad analítica. |
| Adopción directa de Scrum, GitHub Flow, CMMI o ISO/IEC 29110 | Descartada como solución principal. | Son fuentes útiles de conocimiento, pero no resuelven la composición contextual ni la evaluación del artefacto. |

## Requisitos preliminares del artefacto

| Requisito | Tipo | Métrica o criterio preliminar | Fuente |
|:--|:--|:--|:--|
| RQ1. Definir tarea válida | Funcional | Toda tarea debe tener descripción, responsable, componente, criterio de aceptación y estado. | Línea base Odoo; caso PConst. |
| RQ2. Definir repositorio oficial o excepción | Contextual | Cada componente debe clasificarse como institucional, cliente, tercero o excepción documentada. | Línea base GitHub. |
| RQ3. Establecer convención mínima de ramas y commits | Funcional | Ramas y commits deben permitir vínculo directo o indirecto con tarea. | Línea base GitHub. |
| RQ4. Definir solicitud de integración válida | Funcional | Debe incluir tarea, descripción, componentes afectados, revisor y evidencia de verificación. | Línea base GitHub; I5 e I6. |
| RQ5. Diferenciar método y evidencia de verificación | Funcional | Cada cambio funcional debe declarar qué se verificó, cómo se verificó y con qué evidencia. | Línea base GitHub; ausencia de evidencia en solicitudes. |
| RQ6. Registrar entrega mínima | Contextual | Todo despliegue relevante debe identificar ambiente, versión/rama, fecha, responsable y mecanismo. | Hallazgos sobre despliegues y trazabilidad final. |
| RQ7. Medir adopción del marco | Evaluación | Indicadores de cumplimiento por componente y por periodo. | E6 y plan de evaluación. |

## Plan inmediato para construcción

El siguiente paso es formalizar el marco en una ficha reproducible. Esa ficha deberá incluir: objetivo, alcance, roles mínimos, componentes, reglas, plantillas, indicadores, niveles de adopción, excepciones y guía breve de aplicación en PRX. La primera versión no debe prometer automatización completa, DevOps completo ni certificación de procesos; debe concentrarse en producir evidencia mínima verificable.

En el componente de integración y revisión de cambios, el marco deberá reconocer explícitamente que la revisión independiente no existe actualmente como práctica institucional observable en PRX. Por tanto, la primera versión no debe fingir revisión por pares donde no la hay. La regla de diseño será progresiva: primero exigir solicitud de integración trazable; luego plantilla completa y evidencia mínima; después validación documentada; y, cuando exista disponibilidad real, revisión por una persona distinta del autor. Para componentes con un solo desarrollador, se permitirá auto-validación documentada como excepción, siempre que incluya lista de verificación y evidencia verificable.

Para el componente de trazabilidad del código, la primera versión del marco adoptará una convención mínima inspirada en Angular y Conventional Commits. Las ramas deberán usar el formato `<tipo>/<codigo-tarea>-<descripcion-corta>`, por ejemplo `feat/CCC-4407-operador-contrato`; los commits deberán usar `<tipo>(<codigo-tarea>): <descripcion breve>`, por ejemplo `feat(CCC-4407): agregar datos del operador en contratos`. El código de tarea deberá aparecer también en la solicitud de integración. Al fusionar, se recomendará `squash merge`, conservando el código de tarea en el mensaje final, y eliminación de la rama después de la fusión.

La línea base también registra variación en nombres de ramas permanentes y de validación: `Production`, `production`, `Prod`, `Stage`, `Staging`, `staging`, `stagin`, `staging-server`, `TEST`, `Test`, `test`, `COSVI` y `moriah`. Además, en algunos repositorios no existe una rama de validación equivalente a `Stage`, en otros no existe una rama de producción, y la rama por defecto varía entre `main` y ramas como `Production`. Por ello, el marco no solo definirá ramas temporales de trabajo; también exigirá que cada repositorio documente cuáles son sus ramas permanentes oficiales, cuál es su rama por defecto y qué representa cada una.

La convención institucional vigente para PRX es `main` como rama por defecto y tronco de integración, `Stage` como rama de validación cuando exista ambiente de pruebas, y `Production` como rama de producción solo cuando el mecanismo de despliegue lo requiera. La estandarización de nombres será progresiva para evitar riesgos al renombrar ramas históricas que podrían estar conectadas con despliegues, Odoo.sh u otras automatizaciones.

La plantilla mínima obligatoria de solicitud de integración será:

```markdown
## Tarea relacionada

Código de tarea:
Enlace o referencia:

## Descripción del cambio

¿Qué se cambió y por qué?

## Tipo de cambio

- [ ] feat
- [ ] fix
- [ ] hotfix
- [ ] config
- [ ] test
- [ ] docs
- [ ] refactor

## Componentes afectados

- [ ] Odoo Backend
- [ ] API
- [ ] Frontend
- [ ] Base de datos
- [ ] Configuración / despliegue
- [ ] Otro:

## Riesgo del cambio

- [ ] Bajo
- [ ] Medio
- [ ] Alto

Justificación si es medio o alto:

## Verificación realizada

Método:

- [ ] Prueba manual documentada
- [ ] Prueba unitaria
- [ ] Prueba de integración
- [ ] Prueba de API
- [ ] Construcción / compilación
- [ ] No aplica, con justificación

Evidencia:

## Validación

- [ ] Revisado por otra persona
- [ ] Auto-validación documentada
- [ ] Validación automática
- [ ] Excepción documentada

Validador o justificación:

## Checklist mínima

- [ ] Rama incluye código de tarea.
- [ ] Commits incluyen código de tarea.
- [ ] No incluye credenciales ni datos sensibles.
- [ ] Listo para `squash merge`.
- [ ] Rama se eliminará después de fusionar.
```

El marco adoptará un flujo basado en tronco inspirado en *Trunk-Based Development* —desarrollo basado en tronco—. No se adoptará GitFlow como flujo principal, porque introduce ramas permanentes y ceremonias de versión que resultan pesadas para el estado actual de PRX. La regla será mantener ramas cortas por tarea, integrar mediante solicitud de integración, preferir `squash merge`, eliminar la rama después de fusionar y conservar solo ramas permanentes necesarias para estabilidad y validación: `main`, `Stage` y `Production`, cuando el ambiente correspondiente exista.

## Plan inmediato de evaluación

La evaluación deberá conservar la estructura definida en el perfil: línea base previa, ciclo formativo con rediseño y evaluación sumativa inicial. Para reducir alcance y aumentar observabilidad, la aplicación inicial del marco se concentrará en el proyecto **Central**, porque contiene tres componentes —Odoo, API y frontend— y permite observar coordinación entre tres desarrolladores. Ansular y PConst se mantendrán como evidencia diagnóstica y contexto comparativo, pero no serán el foco principal de la primera aplicación.

En el ciclo formativo se aplicará el marco en Central, se registrarán fricciones y se ajustarán reglas o plantillas. En el ciclo sumativo se medirá el cambio en visibilidad, trazabilidad, solicitudes de integración válidas, evidencia mínima de verificación y, si es factible, entrega trazable. Esta delimitación protege el alcance de maestría y evita prometer evaluación simultánea en todos los proyectos observados.

## Pendientes antes de considerar cerrado el borrador

- Revisar la consolidación de indicadores en `06_consolidacion_indicadores.md` si aparece nueva evidencia antes de aplicar el marco.
- Requisitos del artefacto convertidos en `07b_requisitos.md`, suficiente para el hito.
- Diseño preliminar del artefacto creado en `07c_diseno_artefacto.md`, suficiente para el hito.
- Plan de construcción y versiones definido en `07d_plan_construccion.md`, suficiente para el hito.
- Guardar evidencia privada o capturas mínimas de la línea base, sin publicar datos sensibles.

## Referencias

Aniche, M. (2022). *Effective software testing: A developer's guide*. Manning Publications. https://www.manning.com/books/effective-software-testing

GitHub Docs. (s. f.). *GitHub flow*. Recuperado el 22 de septiembre de 2026, de https://docs.github.com/en/get-started/using-github/github-flow

International Organization for Standardization, & International Electrotechnical Commission. (2024a). *ISO/IEC 29110-1-1:2024: Systems and software engineering — Lifecycle profiles for very small entities (VSEs) — Part 1-1: Overview*. https://www.iso.org/standard/85337.html

Laporte, C. Y., Munoz, M., Mejia Miranda, J., & OConnor, R. V. (2018). Applying software engineering standards in very small entities: From startups to grownups. *IEEE Software, 35*(1), 99–103. https://doi.org/10.1109/MS.2017.4541041

Pino, F. J., García, F., & Piattini, M. (2008). Software process improvement in small and medium software enterprises: A systematic review. *Software Quality Journal, 16*(2), 237–261. https://doi.org/10.1007/s11219-007-9038-z

Schwaber, K., & Sutherland, J. (2020). *The Scrum Guide: The definitive guide to Scrum: The rules of the game*. https://scrumguides.org/scrum-guide.html

