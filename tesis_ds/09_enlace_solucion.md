# E9. Enlace propuesta ↔ solución

## Propósito

Este documento enlaza el problema de diseño con la solución construida mediante una matriz de trazabilidad. La finalidad es demostrar, con evidencia, que el artefacto no solo fue documentado, sino que responde a los requisitos derivados de la línea base y produce condiciones para resolver el problema observado.

E9 integra la construcción, la evaluación formativa y la evaluación sumativa acotada. La matriz no declara cumplimiento final del problema de diseño ni mejora sostenida: distingue requisitos demostrados en casos, requisitos no evaluados y condiciones sin cumplimiento acreditado.

## Cadena de trazabilidad esperada

La cadena mínima que el marco busca producir es:

```text
tarea → rama → commit → solicitud de integración → evidencia de verificación → validación
```

La línea base mostró que esta cadena existía solo de forma parcial, aislada o histórica. La solución propuesta busca convertirla en una práctica mínima, común y verificable.

## Matriz problema → requisito → decisión → evidencia

| Problema de diseño observado | Requisito relacionado | Decisión de diseño | Evidencia disponible | Grado de cumplimiento | Limitación actual |
|:--|:--|:--|:--|:--|:--|
| Repositorios y responsabilidades no siempre explícitos. | RQ1, RQ4 | Exigir repositorio oficial o excepción documentada, responsable técnico y mecanismo de excepción. | `07b_requisitos.md`; `07c_diseno_artefacto.md`; `06_codificacion_participantes.md`. | Parcial/no evaluable. | No existe ficha C0 aplicada que acredite formalmente las excepciones de Central API y Frontend. |
| Tareas visibles con granularidad desigual. | RQ2, RQ3 | Definir tarea válida y criterio de división. | `06_linea_base_odoo_tareas.md`; `E-ODOO-INT-01` a `E-ODOO-INT-03`. | Visibilidad demostrada en 3 casos; validez completa no calculable. | No se recuperó inventario ni campos completos de todas las tareas del período. |
| Ausencia de convención documentada de ramas. | RQ5 | Crear `STD-GIT-001 — Convención mínima de ramas`. | `E-ORG-INT-01`; `E-ORG-INT-06`; `E-GH-INT-01`; `E-GH-INT-06`; `E-GH-INT-07`. | Demostrado en 3 casos cerrados. | Falta medición sostenida de uso. |
| Ramas permanentes heterogéneas o ausentes. | RQ5.1 | Declarar ramas permanentes, equivalencias y normalización progresiva. | `06_evidencia_nombres_ramas.md`; `E-GH-INT-04`; `E-ORG-INT-06`. | Parcial. | Configuración demostrada en un repositorio intervenido; faltan inventario y excepciones de los demás. |
| Ausencia de convención documentada de commits. | RQ6 | Crear `STD-GIT-003 — Convención mínima de commits`. | `E-ORG-INT-04`; `E-GH-INT-01`; `E-GH-INT-06`; `E-GH-INT-07`. | Conformidad demostrada por caso. | No se recuperó historial completo para calcular una tasa de commits. |
| Riesgo de adoptar flujo pesado tipo GitFlow. | RQ6.1 | Adoptar flujo basado en tronco, ramas cortas y `squash merge`. | `E-GH-INT-01`; `E-GH-INT-02`; `E-GH-INT-06`; `E-GH-INT-07`. | Aplicado en 3 casos cerrados. | No se comparó con GitFlow ni se demuestra superioridad causal. |
| Solicitudes de integración sin descripción homogénea. | RQ7 | Crear plantilla operativa de solicitud de integración. | `E-ORG-INT-02`; `E-GH-INT-01`; `E-GH-INT-08`; `E-GH-INT-09`. | Cumplido en 3 de 3 solicitudes cerradas de la serie. | No equivale a conformidad sostenida de todas las solicitudes futuras. |
| Título de PR no controlado por plantilla. | RQ7, RQ10 | Crear `STD-GIT-002` con regla de título de PR. | `E-ORG-INT-03`; `E-GH-INT-01`; `E-GH-INT-08`; `E-GH-INT-09`. | Demostrado en 3 solicitudes cerradas. | No demuestra adopción sostenida. |
| Confusión entre solicitud trazable y revisión independiente. | RQ8, RQ9 | Definir validación progresiva: revisión por tercero, auto-validación documentada, validación automática o excepción. | `STD-GIT-002`; `07c_diseno_artefacto.md`; `E-GH-INT-08`; `E-GH-INT-09`. | Parcial. | Hay auto-validación y excepción explícitas, pero no evidencia comparativa de revisión por tercero. |
| Solicitudes sin evidencia mínima de verificación. | RQ10 | Exigir método y evidencia de verificación en plantilla PR. | `E-GH-INT-01`; `E-TEST-INT-01`; `E-GH-INT-08`; `E-GH-INT-09`. | Demostrado en 3 solicitudes cerradas. | El tercer caso registra excepción `EPERM`; no hay tasa de período. |
| Pruebas unitarias o evidencia técnica no institucionalizadas. | RQ11 | Exigir al menos una evidencia técnica en componente crítico. | `E-TEST-INT-01`. | Cumplido en primera aplicación. | La evidencia se limita a Central API y no demuestra cobertura institucional. |
| Entregas o ambientes con trazabilidad parcial. | RQ12 | Definir registro mínimo de entrega y ramas permanentes. | `07c_diseno_artefacto.md`; `STD-GIT-001`. | Pendiente/parcial. | Falta entrega real trazada. |
| Necesidad de comparar antes/después. | RQ13 | Definir indicadores I1-I9 y plan de evaluación E8. | `06_consolidacion_indicadores.md`; `08_resultado_sumativo_serie_casos_central.md`. | Parcial, con resultados de caso. | No existe período posterior comparable ni denominadores organizacionales completos. |
| Riesgo de reducir el marco a GitHub/Odoo. | RQ14 | Separar regla general e instanciación PRX. | `07c_diseno_artefacto.md`; `07f_ficha_artefacto.md`. | Alto. | Debe mantenerse en la traducción ALSIE. |

## Evidencias que ya respaldan solución construida

| Evidencia | Relación con la solución |
|:--|:--|
| `E-ORG-INT-01` | Demuestra publicación del estándar mínimo de ramas. |
| `E-ORG-INT-02` | Demuestra publicación de la plantilla operativa de solicitud de integración. |
| `E-ORG-INT-03` | Demuestra publicación del estándar mínimo de solicitudes de integración. |
| `E-ORG-INT-04` | Demuestra publicación del estándar mínimo de commits. |
| `E-ORG-INT-05` | Demuestra organización institucional de estándares técnicos. |
| `E-GH-ORG-01` | Demuestra instanciación técnica inicial en el repositorio `.github` y revela fricción de adopción. |
| `E-ODOO-INT-01` | Demuestra la existencia de una tarea real posterior al marco. |
| `E-GH-INT-01` | Demuestra aplicación de rama, título, plantilla, commit y vínculo con tarea en `CCC-7336`. |
| `E-GH-INT-02` | Demuestra fusión de la solicitud y eliminación de la rama temporal. |
| `E-GH-INT-04` | Demuestra configuración de ramas permanentes en el repositorio intervenido. |
| `E-TEST-INT-01` | Demuestra 169 pruebas unitarias exitosas en Central API. |
| `E-ORG-INT-06` | Demuestra publicación de la actualización V1.1 de la convención de ramas. |
| `E-GH-INT-06`, `E-GH-INT-08` y `E-TEST-INT-03` | Demuestran una segunda aplicación posterior en Central Frontend para `CCC-7480`: rama y *commit* conformes, solicitud fusionada hacia `main`, plantilla completa, eliminación de rama y pruebas unitarias visibles de `ContractsComponent`. |
| `E-ODOO-INT-02` | Demuestra que `CCC-7480` corresponde a una tarea posterior real de Central. |
| `E-ODOO-INT-03`, `E-GH-INT-07` y `E-GH-INT-09` | Demuestran que `CCC-7477` corresponde a una tarea real posterior de Central Frontend y que recorrió la cadena *commit* → solicitud fusionada → plantilla → eliminación de rama, con excepción de verificación documentada. |

## Consolidación del enlace con la evaluación sumativa

`08_resultado_sumativo_serie_casos_central.md` completa el enlace entre requisitos e indicadores para tres cambios cerrados. El resultado no llena retrospectivamente los denominadores de un período completo; por ello, los eslabones I1 e I4 se reportan como utilidad demostrada por caso y no como porcentajes de adopción. I2 tampoco se declara cumplido: los repositorios externos se conservan como excepciones de transición, no como resultado atribuido al marco.

| Cadena evaluada | Evidencia sumativa | Grado de cumplimiento | Límite declarado |
|:--|:--|:--|:--|
| Tarea → rama → *commit* → solicitud fusionada | `CCC-7336`, `CCC-7480` Frontend y `CCC-7477`; `E-ODOO-INT-01` a `E-ODOO-INT-03`; `E-GH-INT-01`, `E-GH-INT-02`, `E-GH-INT-06` a `E-GH-INT-09`. | Demostrada en 3 de 3 casos cerrados. | No equivale a adopción de todos los cambios de Central. |
| Solicitud → evidencia de verificación o excepción | `E-TEST-INT-01`, `E-TEST-INT-03`, `E-GH-INT-08`, `E-GH-INT-09`. | Demostrada en 3 de 3 solicitudes cerradas de la serie. | `CCC-7477` tiene excepción `EPERM`, no prueba completa ejecutada. |
| Repositorio institucional o excepción | Línea base y ficha del artefacto. | No cumplido como institucionalización; condición de transición documentada. | No se atribuye mejora de I2. |
| Entrega/configuración C5 | Diseño C5 y evidencia de ramas permanentes. | No evaluado en una entrega real. | Se conserva como componente diseñado, no como resultado de utilidad. |

## Demostración versus evaluación

La evidencia disponible demuestra construcción, instanciación y aplicación real del artefacto en `CCC-7336`, `CCC-7480` Frontend y `CCC-7477`. La evaluación sumativa demuestra utilidad inicial en esta serie de casos, no mejora sostenida. La publicación de estándares, la configuración de ramas y las solicitudes fusionadas muestran que la solución puede usarse en Central; la evidencia no permite extender esa afirmación a todos los cambios futuros ni al conjunto de PRX.

Esta distinción es crítica: que existan estándares no significa que el equipo los haya adoptado; que exista plantilla no significa que las solicitudes contengan evidencia de verificación; que exista repositorio `.github` no significa que Central haya mejorado sus indicadores. La evidencia de campo disponible permite afirmar la aplicabilidad inicial del artefacto en tres cambios, no su adopción sostenida.

## Limitaciones del enlace actual

1. La serie contiene tres cambios cerrados en un único proyecto, no un período completo de adopción.
2. La primera fricción observada (`config/ADM-4940_config_pr_template`) indica comprensión inicial parcial de la convención de ramas.
3. Los repositorios externos de API y Frontend no acreditan institucionalización; se tratan como excepciones de transición.
4. C5 no tiene evidencia de entrega real y no se usa para sostener utilidad del marco.
5. Los principios se respaldan solo con generalización analítica inicial y deben reevaluarse si Central produce nuevos cambios.

## Estado del gate E9

E9 queda **cerrado con limitaciones explícitas**. La matriz enlaza el problema, requisitos, decisiones y evidencia de tres aplicaciones cerradas, e identifica los eslabones no cumplidos o no evaluados sin sustituirlos por afirmaciones de éxito. La solución queda demostrada como aplicable y útil en la serie acotada; no se declara mejora institucional sostenida.
