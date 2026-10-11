# E7d. Plan de construcción y versiones

## Propósito

Este documento define qué versión del **Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización** se construirá primero, qué queda fuera de alcance, qué evidencias debe producir y cuándo estará listo para evaluación formativa. En Design Science, la construcción no es solo implementación operativa; es una secuencia de versiones que permite aprender, ajustar el artefacto y evitar que la evaluación sea una justificación posterior.

## Criterio para decidir qué entra en la versión 1

Una regla, plantilla o mecanismo entra en la versión 1 cuando cumple simultáneamente los siguientes criterios:

| Criterio | Pregunta operativa | Decisión esperada |
|:--|:--|:--|
| Necesidad | ¿Sin esto no se puede medir visibilidad, trazabilidad, verificación o entrega? | Si la respuesta es sí, entra. |
| Trazabilidad | ¿Se vincula con un requisito de E7b y un indicador de E6? | Si no hay vínculo, queda fuera o como mejora posterior. |
| Factibilidad | ¿Puede aplicarse en Central con DEV-001, DEV-002 y DEV-003 sin depender de una reorganización completa? | Si requiere cambios organizacionales mayores, no entra en versión 1. |
| Evidencia | ¿Produce una evidencia observable por un tercero? | Si no deja evidencia, no sirve para la evaluación inicial. |
| Ligereza | ¿El beneficio supera la carga adicional para el equipo? | Si aumenta fricción sin aportar medición, queda fuera. |
| Riesgo | ¿Puede romper ramas, despliegues, Odoo.sh, repositorios o trabajo activo? | Si el riesgo es alto, se documenta equivalencia y se posterga normalización. |
| Transferibilidad | ¿Es parte del marco o solo una configuración local de GitHub/Odoo? | Si es local, se documenta como instanciación PRX, no como regla universal. |

Este criterio protege el alcance de maestría: el artefacto debe ser suficientemente completo para evaluarse, pero no tan amplio que se convierta en una transformación organizacional imposible de observar en el tiempo disponible.

## Versión mínima viable del artefacto

La versión mínima viable del marco será **V1.0-Central**. Su objetivo es permitir que el proyecto Central produzca evidencia observable de gestión visible, trazabilidad técnica, solicitud de integración válida y verificación básica.

| Elemento | Entra en V1.0-Central | Queda fuera de V1.0-Central |
|:--|:--|:--|
| Precondiciones | Ficha mínima de componente, responsable codificado, repositorio oficial o excepción. | Migración completa de todos los repositorios históricos. |
| Tareas | Definición de tarea válida y criterio de división. | Rediseño completo del proceso de gestión de proyectos. |
| Ramas permanentes | Declarar rama por defecto, validación, producción y equivalencias. | Renombrar ramas históricas sin análisis de dependencias. |
| Ramas temporales | Convención `<tipo>/<codigo-tarea>-<descripcion-corta>`. | Automatización obligatoria para bloquear nombres inválidos. |
| Commits | Convención `<tipo>(<codigo-tarea>): <descripcion breve>`. | Reescritura de historial previo. |
| Solicitudes de integración | Plantilla mínima obligatoria mediante repositorio organizacional `.github`. | Reglas automáticas obligatorias de bloqueo por descripción incompleta. |
| Validación | Auto-validación documentada, validación automática o revisión por tercero si es factible. | Exigir revisión independiente en todos los componentes desde el primer ciclo. |
| Verificación | Método y evidencia mínima de verificación por cambio funcional. | Cobertura de pruebas completa o canalización CI/CD madura. |
| Entrega | Registro mínimo de ambiente, rama/versión, fecha, responsable y mecanismo cuando exista entrega relevante. | Sistema formal de gestión de versiones o liberaciones. |
| Seguimiento | Indicadores I1-I9 y registro de fricciones. | Tablero automatizado de métricas. |

## Versiones previstas

| Versión | Tipo de prototipo | Pregunta de diseño | Producto esperado | Criterio de avance |
|:--|:--|:--|:--|:--|
| V0.1 | Exploratorio | ¿El problema real es falta total de prácticas o falta de homogeneidad, trazabilidad y evidencia? | Línea base E6, indicadores I1-I9 y evidencias privadas iniciales. | Línea base documentada antes de intervención. |
| V0.2 | Analítico-formativo | ¿Las reglas mínimas cubren el problema sin sobrecargar al equipo? | Requisitos E7b, diseño E7c y plantilla de solicitud de integración. | Requisitos trazables y diseño C0-C6 coherente. |
| V1.0-Central | Operacional-formativo | ¿Puede el equipo Central aplicar el marco en trabajo real y producir evidencia mínima? | Marco aplicado en Central con tareas, ramas, commits, solicitudes y verificación. | Al menos un ciclo de uso real con fricciones y ajustes documentados. |
| V1.1-Central | Rediseño formativo | ¿Qué reglas deben ajustarse después del primer uso real? | Versión ajustada del marco, plantilla o reglas. | Cambios documentados con razón y evidencia. |
| V1.2-Central | Sumativo inicial | ¿La versión ajustada mejora los indicadores frente a la línea base? | Medición posterior comparada contra línea base. | Evidencia suficiente para evaluar utilidad y formular principios de diseño. |

La tesis no debe presentar V1.2 como teoría general. Con una aplicación inicial en Central, la afirmación aceptable es de generalización analítica hacia equipos pequeños con condiciones similares.

## Construcción de V1.0-Central

| Producto de construcción | Archivo o soporte | Responsable | Evidencia esperada |
|:--|:--|:--|:--|
| Documento de diseño del marco | `tesis_ds/07c_diseno_artefacto.md` | Tesista | Versión fechada del diseño. |
| Plantilla de solicitud de integración | `tesis_ds/07c_plantilla_solicitud_integracion.md` y `.github/pull_request_template.md` | Tesista / PRX | `E-GH-ORG-01`. |
| Convención de ramas y commits | Documento del marco y comunicación interna | Tesista | Captura o registro de la convención comunicada. |
| Declaración de ramas permanentes | Por repositorio Central | Responsable de componente | Evidencia de rama por defecto, validación, producción o equivalencia. |
| Aplicación en solicitudes nuevas | GitHub | DEV-001, DEV-002, DEV-003 según componente | PRs posteriores con plantilla y evidencia mínima. |
| Verificación técnica básica | Repositorio, terminal o captura | Responsable del componente | `E-TEST-INT-01` u otro código equivalente. |
| Registro de fricciones | Bitácora de evaluación formativa | Tesista | `E-FORM-01`. |

## Criterio de suficiencia para pasar a evaluación formativa

V1.0-Central estará lista para evaluación formativa cuando se cumplan estas condiciones:

- La plantilla de solicitud de integración esté disponible en la organización mediante el repositorio `.github`.
- Central tenga definidos sus componentes, responsables codificados y repositorios o excepciones.
- Cada repositorio de Central tenga declaradas sus ramas permanentes y equivalencias.
- La convención de ramas y commits esté comunicada a los responsables de Central.
- Exista al menos una solicitud de integración nueva donde pueda observarse el uso de la plantilla o la fricción producida por ella.
- Exista un mecanismo para registrar evidencia de verificación, aunque sea prueba manual documentada o salida de comando.
- Las evidencias privadas estén categorizadas como línea base, intervención o evaluación.

Si una condición no se cumple, no se debe fingir que la evaluación formativa comenzó. Se documenta como bloqueo o excepción y se decide si se ajusta el marco o el alcance.

## Riesgos de construcción y mitigación

| Riesgo | Impacto | Mitigación |
|:--|:--|:--|
| Confundir configuración GitHub con artefacto completo. | Reduce la tesis a ingeniería local. | Mantener separación entre marco, productos operativos e instanciación PRX. |
| Tomar evidencia después y tratarla como línea base. | Invalida comparación antes/después. | Registrar fecha de captura y fecha del evento observado. |
| Renombrar ramas históricas sin verificar dependencias. | Puede romper despliegues o automatizaciones. | Documentar equivalencias antes de normalizar. |
| Exigir revisión independiente donde no hay disponibilidad. | Bloquea adopción y genera incumplimiento artificial. | Aceptar auto-validación documentada como excepción explícita. |
| Agregar automatización prematura de validación de PRs. | Desplaza tiempo de evaluación y aumenta fricción. | Tratar GitHub Actions como mejora posterior, salvo decisión explícita y acotada. |
| No obtener evidencia de pruebas en Central. | Debilita I7 y la verificación técnica básica. | Priorizar al menos un componente crítico con prueba ejecutable o evidencia técnica equivalente. |
| Publicar información sensible. | Riesgo ético y organizacional. | Usar códigos de evidencia, participantes anonimizados y capturas privadas. |

## Decisiones sobre mejoras posteriores

El flujo de trabajo de GitHub Actions para validar que la descripción de la solicitud de integración cumpla la plantilla queda clasificado como **mejora posterior**. Puede construirse si no compromete el cronograma, pero no será criterio obligatorio de V1.0-Central. Si se incorpora, deberá documentarse como apoyo técnico de la instanciación PRX y no como componente universal del marco.

Otras mejoras posteriores son: bloqueo automático de ramas mal nombradas, tablero automatizado de indicadores, reglas de protección avanzadas, `CODEOWNERS` obligatorio y canalización CI/CD completa. Estas mejoras pueden ser valiosas, pero exceden la versión mínima necesaria para evaluar el principio de diseño del marco.

## Estado del gate E7d

E7d queda **suficiente para el hito**. La versión mínima viable está definida, las versiones tienen pregunta de diseño, el criterio de suficiencia para evaluación formativa es explícito y los riesgos principales tienen mitigación. El siguiente paso metodológico es construir/aplicar V1.0-Central, registrar verificación interna en E7e y preparar la evaluación formativa de E8.
