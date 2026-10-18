# E-SUM-01. Resultado sumativo inicial de caso — CCC-7336

## Propósito y alcance

Este documento compara la situación de línea base de Central API con la primera aplicación real del marco en la tarea `CCC-7336`. Su unidad de análisis es un cambio de software trazable, no un periodo completo de adopción institucional. Por ello, el resultado se denomina **sumativo inicial de caso** y no demuestra mejora sostenida del equipo ni adopción institucional completa.

La línea base formal se levantó entre el 2026-09-21 y el 2026-10-04. La aplicación posterior corresponde a `CCC-7336`, ejecutada y cerrada el 2026-10-17 según las evidencias privadas registradas. La comparación se limita a Central API porque es el componente donde existe evidencia antes y después suficientemente identificable.

## Desviación respecto al plan original

El plan original preveía una medición posterior por periodo comparable a la línea base. La evidencia disponible permite, por ahora, una comparación de un único cambio real. Esta desviación se documenta antes de interpretar resultados: no se reemplaza retrospectivamente el criterio de evaluación ni se presentan porcentajes de un solo caso como adopción sostenida.

La razón de la delimitación es factual: `CCC-7336` es la única aplicación posterior del marco con cadena completa de evidencia disponible al momento de este registro. Si se obtiene actividad posterior suficiente, deberá añadirse una medición de periodo sin borrar ni alterar este resultado inicial.

## Comparación antes → después

| Indicador | Línea base de Central API | Resultado en `CCC-7336` | Interpretación prudente |
|:--|:--|:--|:--|
| I1. Visibilidad de tarea | No existe evidencia suficiente de tarea válida para Central API en la ventana base; se reportó trabajo no trazado en GitHub. | Existe la tarea `CCC-7336` en el tablero. | Mejora observable de visibilidad para este cambio; no se calcula proporción de tareas válidas. |
| I2. Repositorio institucional o excepción | Repositorio de Central API fuera de la organización institucional; migración pendiente. | La condición institucional completa sigue pendiente; la aplicación no se atribuye como migración institucional. | Sin mejora afirmada; debe existir excepción documentada hasta completar migración. |
| I3. Ramas conformes | 0 ramas creadas en la ventana y sin convención documentada. | Rama `test/CCC-7336-validar-tests-unitarios-api`, conforme con el formato vigente. | Conformidad demostrada en un caso. |
| I4. Commits conformes | 0 commits registrados en la ventana y sin convención documentada. | Commit `test(CCC-7336): validar y corregir tests unitarios`, con código de tarea. | Conformidad demostrada en un caso. |
| I5. Integración mediante solicitud | 0 solicitudes registradas en Central API durante la ventana. | Solicitud creada y fusionada hacia `main`. | Integración mediante solicitud demostrada en un caso. |
| I6. Evidencia mínima de verificación | Sin solicitudes de integración en la ventana; no existía evidencia asociada. | La cadena del caso incluye `E-TEST-INT-01`, con 169 pruebas exitosas. | Evidencia técnica existe para el caso; la plantilla debe mantener vínculo explícito con la evidencia final en futuras solicitudes. |
| I7. Verificación técnica | No existe evidencia ejecutada de pruebas para Central API en la línea base. | 169 pruebas unitarias ejecutadas exitosamente. | Criterio mínimo cumplido para Central API. |
| I9. Cadena trazable | Trabajo reportado no subido al repositorio; cadena incompleta. | Tarea → rama → commit → solicitud → prueba → fusión → eliminación de rama. | Cadena completa demostrada para un caso. |

## Evidencias utilizadas

| Código | Función en el resultado |
|:--|:--|
| `E-ODOO-INT-01` | Evidencia de tarea real `CCC-7336`. |
| `E-GH-INT-01` | Evidencia de rama, título, plantilla y commit de la solicitud. |
| `E-GH-INT-02` | Evidencia de fusión y eliminación de la rama temporal. |
| `E-GH-INT-04` | Evidencia de configuración de ramas permanentes del repositorio intervenido. |
| `E-TEST-INT-01` | Evidencia de 169 pruebas unitarias exitosas. |
| `E-ORG-INT-06` | Evidencia de publicación de `STD-GIT-001` V1.1. |

## Resultado frente a criterios

Para el cambio `CCC-7336`, los criterios de trazabilidad y verificación se cumplieron a nivel de caso: tarea identificable, rama y commit conformes, solicitud fusionada y prueba ejecutada. No se calcula cumplimiento porcentual de los umbrales 70 % u 80 % porque el denominador posterior es un solo cambio; afirmar 100 % en esas condiciones sería engañoso.

I2 no se declara cumplido: la migración de Central API a la organización institucional permanece pendiente. El marco admite esta condición como excepción documentada durante la transición, pero la excepción no equivale a cumplimiento del repositorio institucional.

## Amenazas a la validez

| Amenaza | Impacto residual | Tratamiento |
|:--|:--|:--|
| Un solo cambio posterior. | Alto. | Limitar inferencia a aplicabilidad inicial de un caso. |
| Autor del artefacto y ejecutor del caso coinciden. | Alto. | No afirmar adopción independiente ni efectividad del equipo. |
| Periodo posterior no equivalente a dos semanas. | Alto. | Declarar desviación y evitar tasas comparativas. |
| Evidencia técnica externa a la descripción inicial de la solicitud. | Medio. | Mantener la relación explícita mediante el código `E-TEST-INT-01` y reforzarla en usos futuros. |
| Repositorio no institucional. | Medio. | Declarar excepción pendiente de migración, sin atribuir mejora en I2. |

## Veredicto

`E-SUM-01` queda registrado como **resultado sumativo inicial de caso**, útil para sostener que el marco puede producir una cadena trazable y evidencia técnica en Central API. No es suficiente para cerrar una evaluación sumativa por periodo ni para validar principios de diseño de forma definitiva.
