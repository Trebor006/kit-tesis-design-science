# E9. Enlace propuesta ↔ solución

## Propósito

Este documento enlaza el problema de diseño con la solución construida mediante una matriz de trazabilidad. La finalidad es demostrar, con evidencia, que el artefacto no solo fue documentado, sino que responde a los requisitos derivados de la línea base y produce condiciones para resolver el problema observado.

E9 se mantiene como **matriz de enlace parcial**. Ya existen evidencias de construcción, aplicación real y verificación técnica en Central; todavía falta la comparación sumativa posterior. Por tanto, se declara cumplimiento de la cadena en un caso real, no cumplimiento final ni mejora sostenida del problema de diseño.

## Cadena de trazabilidad esperada

La cadena mínima que el marco busca producir es:

```text
tarea → rama → commit → solicitud de integración → evidencia de verificación → validación
```

La línea base mostró que esta cadena existía solo de forma parcial, aislada o histórica. La solución propuesta busca convertirla en una práctica mínima, común y verificable.

## Matriz problema → requisito → decisión → evidencia

| Problema de diseño observado | Requisito relacionado | Decisión de diseño | Evidencia disponible | Grado preliminar de cumplimiento | Limitación actual |
|:--|:--|:--|:--|:--|:--|
| Repositorios y responsabilidades no siempre explícitos. | RQ1, RQ4 | Exigir repositorio oficial o excepción documentada, responsable técnico y mecanismo de excepción. | `07b_requisitos.md`; `07c_diseno_artefacto.md`; `06_codificacion_participantes.md`. | Parcial. | Falta ficha por componente Central en E7f/E8 con repositorio y ramas declaradas. |
| Tareas visibles con granularidad desigual. | RQ2, RQ3 | Definir tarea válida y criterio de división. | `06_linea_base_odoo_tareas.md`; `E-ODOO-INT-01`. | Parcial. | Existe una tarea posterior usada para PR real; falta medir proporción de tareas válidas en periodo posterior. |
| Ausencia de convención documentada de ramas. | RQ5 | Crear `STD-GIT-001 — Convención mínima de ramas`. | `E-ORG-INT-01`; `E-ORG-INT-06`; `E-GH-INT-01`. | Alto en construcción y primera aplicación. | Falta medición sostenida de uso. |
| Ramas permanentes heterogéneas o ausentes. | RQ5.1 | Declarar ramas permanentes, equivalencias y normalización progresiva. | `06_evidencia_nombres_ramas.md`; `E-GH-INT-04`; `E-ORG-INT-06`. | Parcial. | Configuración demostrada en un repositorio intervenido; faltan inventario y excepciones de los demás. |
| Ausencia de convención documentada de commits. | RQ6 | Crear `STD-GIT-003 — Convención mínima de commits`. | `E-ORG-INT-04`; `E-GH-INT-01`. | Alto en construcción y primera aplicación. | Un caso no demuestra adopción sostenida. |
| Riesgo de adoptar flujo pesado tipo GitFlow. | RQ6.1 | Adoptar flujo basado en tronco, ramas cortas y `squash merge`. | `E-GH-INT-01`; `E-GH-INT-02`. | Alto en primera aplicación. | Falta observar más de un ciclo. |
| Solicitudes de integración sin descripción homogénea. | RQ7 | Crear plantilla operativa de solicitud de integración. | `E-ORG-INT-02`; `E-GH-INT-01`. | Alto en primera aplicación. | Falta medición posterior de conformidad. |
| Título de PR no controlado por plantilla. | RQ7, RQ10 | Crear `STD-GIT-002` con regla de título de PR. | `E-ORG-INT-03`; `E-GH-INT-01`. | Alto en primera aplicación. | Un título conforme no demuestra adopción sostenida. |
| Confusión entre solicitud trazable y revisión independiente. | RQ8, RQ9 | Definir validación progresiva: revisión por tercero, auto-validación documentada, validación automática o excepción. | `STD-GIT-002`; `07c_diseno_artefacto.md`. | Parcial. | Falta caso real con validación o excepción documentada. |
| Solicitudes sin evidencia mínima de verificación. | RQ10 | Exigir método y evidencia de verificación en plantilla PR. | `E-GH-INT-01`; `E-TEST-INT-01`. | Alto en primera aplicación. | Falta comparar proporción posterior contra la línea base. |
| Pruebas unitarias o evidencia técnica no institucionalizadas. | RQ11 | Exigir al menos una evidencia técnica en componente crítico. | `E-TEST-INT-01`. | Cumplido en primera aplicación. | La evidencia se limita a Central API y no demuestra cobertura institucional. |
| Entregas o ambientes con trazabilidad parcial. | RQ12 | Definir registro mínimo de entrega y ramas permanentes. | `07c_diseno_artefacto.md`; `STD-GIT-001`. | Pendiente/parcial. | Falta entrega real trazada. |
| Necesidad de comparar antes/después. | RQ13 | Definir indicadores I1-I9 y plan de evaluación E8. | `06_consolidacion_indicadores.md`; `08_resultado_sumativo_inicial_CCC-7336.md`. | Parcial. | Existe comparación de un caso; falta medición por periodo comparable. |
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

## Evidencia pendiente para afirmar mejora sumativa

| Evidencia pendiente | Por qué es necesaria |
|:--|:--|
| Medición posterior por periodo comparable | Permitirá contrastar tasas de adopción contra la línea base sin depender de un solo cambio. |

## Demostración versus evaluación

La evidencia disponible demuestra construcción, instanciación y aplicación real del artefacto en `CCC-7336`. No demuestra todavía evaluación completa ni mejora sostenida. La publicación de estándares, la configuración de ramas y la solicitud fusionada muestran que la solución puede usarse en Central; la evaluación sumativa requiere comparar resultados posteriores contra la línea base.

Esta distinción es crítica: que existan estándares no significa que el equipo los haya adoptado; que exista plantilla no significa que las solicitudes contengan evidencia de verificación; que exista repositorio `.github` no significa que Central haya mejorado sus indicadores. Por ello, el enlace actual se declara como inicial y pendiente de evidencia de campo.

## Limitaciones del enlace actual

1. La evidencia disponible se concentra en productos institucionales y configuración inicial, no todavía en uso sostenido.
2. La primera fricción observada (`config/ADM-4940_config_pr_template`) indica adopción parcial de la convención de ramas.
3. La aplicación evidencia un solo cambio real; no permite inferir adopción sostenida.
4. Falta comparación sumativa de indicadores contra la línea base.
5. La contribución de conocimiento aún no puede formularse como validada; solo puede formularse como contribución preliminar sustentada en una aplicación inicial.

## Estado del gate E9

E9 queda **avanzado**, con trazabilidad demostrada en una aplicación real y comparación inicial de caso. No queda cerrado porque falta una medición posterior por periodo comparable, necesaria para sostener afirmaciones de mejora frente a la línea base y completar el grado de cumplimiento de cada requisito.
