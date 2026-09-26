# Plan individual de desarrollo de la propuesta

## Propósito

Este plan organiza el trabajo individual de Robert Cabrera Lara desde el perfil Design Science hasta una predefensa interna prevista para la última semana de octubre o, como máximo, la primera semana de noviembre de 2026. El plan no sustituye al cronograma académico institucional; traduce el perfil en tareas ejecutables para desarrollar, aplicar y documentar la propuesta.

## Punto de partida

El perfil Design Science está construido y revisado en `tesis_ds/03_perfil_ds_limpio.md`. El problema, el objeto de estudio, el campo de acción, el artefacto, la estrategia de evaluación y la contribución esperada ya están formulados. E6 está fortalecido con instrumentos, pero todavía no está cerrado porque falta levantar línea base real en PRX.

## Objetivo operativo

Desarrollar, aplicar y evaluar una primera versión del marco ligero de adopción inicial de prácticas de Ingeniería de Software en la línea de software a medida de PRX, documentando la evaluación formativa, el rediseño, la evaluación sumativa inicial y los principios de diseño resultantes.

## Plan por semanas

| Semana | Actividad | Producto verificable | Riesgo principal | Mitigación |
|:--|:--|:--|:--|:--|
| 1 | Publicar repositorio, estudiar perfil, confirmar proyectos piloto y levantar línea base. | Enlace público; línea base preliminar; proyectos piloto seleccionados. | No tener datos suficientes en Odoo o GitHub. | Registrar ausencia de evidencia como parte del diagnóstico y usar entrevistas breves. |
| 2 | Ejecutar E7a y E7b: alternativas de solución y requisitos del artefacto. | `07a_alternativas.md` y `07b_requisitos.md`. | Elegir una solución por preferencia personal. | Usar matriz de decisión con factibilidad, novedad, costo, riesgo y sustento teórico. |
| 3 | Diseñar el marco: componentes, reglas, ruta de adopción, productos de trabajo y criterios de verificación. | `07c_diseno_artefacto.md` con diagrama y trazabilidad requisito → componente. | Convertir el marco en una lista genérica de buenas prácticas. | Mantener precondiciones, reglas mínimas y evidencia exigida por práctica. |
| 4 | Formalizar la versión 1.0 del marco y verificarla con revisión interna o expertos. | `07d_plan_construccion.md`, `07e_construccion_verificacion.md` y versión 1.0 del marco. | No contar con revisión externa mínima. | Usar al menos un responsable técnico o par con experiencia para revisión estructurada. |
| 5 | Aplicar evaluación formativa en PRX. | Hallazgos formativos documentados; fricciones de aplicación. | Confundir demostración con evaluación. | Registrar qué pregunta de diseño responde el ciclo formativo y qué se aprendió. |
| 6 | Rediseñar el marco y ejecutar evaluación sumativa inicial. | Versión 1.1 del marco; medición contra criterios de éxito. | Ajustar criterios después de ver resultados. | Mantener criterios predefinidos; cualquier cambio se documenta como rediseño, no como éxito. |
| 7 | Analizar resultados y elaborar matriz propuesta ↔ solución. | `08_evaluacion.md` y `09_enlace_solucion.md`. | Hacer afirmaciones más amplias que la evidencia. | Declarar límites, amenazas a la validez y transferibilidad analítica. |
| 8 | Formular principios de diseño y preparar documento completo para predefensa interna. | `10_contribucion_conclusiones.md`; paquete de predefensa. | Presentar solo el artefacto y no la contribución. | Usar plantilla objetivo → contexto → mecanismo → principio. |

## Entregables mínimos antes de predefensa interna

1. Perfil Design Science limpio y estudiado.
2. Línea base real con evidencia de Odoo, GitHub, repositorios y entrevistas.
3. Marco ligero versión 1.0 y versión rediseñada 1.1.
4. Evaluación formativa con rediseño documentado.
5. Evaluación sumativa inicial contra criterios predefinidos.
6. Matriz de trazabilidad problema → requisito → decisión → evidencia → contribución.
7. Principios de diseño con contexto, mecanismo y condiciones de contorno.
8. Amenazas a la validez con mitigación e impacto residual.

## Restricciones metodológicas

CMMI se mantendrá como antecedente conceptual de mejora de capacidades, no como objetivo de certificación ni como criterio de éxito. La contribución no será “mejorar PRX”, sino derivar principios de diseño para marcos ligeros en equipos pequeños con baja formalización. La generalización será analítica y limitada a contextos estructuralmente similares.

## Próxima acción inmediata

La próxima acción es levantar la línea base real usando `tesis_ds/06_instrumentos_linea_base.md` y, en paralelo, iniciar E7a con alternativas de solución. No debe construirse el marco operacional antes de registrar los valores iniciales de los indicadores.
