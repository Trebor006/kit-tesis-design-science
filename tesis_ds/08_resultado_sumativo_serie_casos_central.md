# E-SUM-02. Evaluación sumativa de campo mediante serie acotada de casos — Central

## Propósito y decisión de alcance

Esta evaluación sumativa valora la utilidad inicial de la iteración V1.0–V1.1 del marco en tres cambios reales y cerrados de Central: `CCC-7336` en Central API, y `CCC-7480` y `CCC-7477` en Central Frontend. `CCC-7336` fue la aplicación formativa de V1.0 que produjo el rediseño V1.1; los dos casos de Frontend aportan evidencia posterior al rediseño. La unidad de análisis es un cambio trazable cerrado, no una organización ni un período de adopción institucional. La selección incluye los tres cambios cerrados para los cuales se recuperó una cadena completa de tarea, cambio técnico y desenlace al corte de evidencia declarado por el tesista.

El plan original contemplaba una ventana posterior equivalente a la línea base del 21 de septiembre al 4 de octubre de 2026. La evidencia disponible no permite reconstruir de forma exhaustiva todos los cambios de un período completo, sus denominadores de *commits* ni la validez de todas las tareas en Odoo. En vez de ocultar esa limitación o calcular porcentajes aparentes, se documenta una desviación metodológica: evaluación de campo sumativa mediante una serie acotada de tres casos cerrados. La decisión reduce el alcance de la inferencia, pero conserva los criterios fijados antes de construir y permite reportar cuáles se cumplen, cuáles no pueden calcularse y por qué.

La serie usa trazas de Odoo, GitHub y resultados técnicos. Esta triangulación es coherente con el reporte de estudios de caso en Ingeniería de Software, aunque no convierte los tres cambios en una muestra estadística de equipos pequeños (Runeson & Höst, 2009).

## Casos incluidos y trazabilidad mínima

| Caso | Componente | Tarea | Evidencia de integración | Evidencia de verificación | Estado al corte |
|:--|:--|:--|:--|:--|:--|
| `CCC-7336` | Central API | `E-ODOO-INT-01` | `E-GH-INT-01`; `E-GH-INT-02` | `E-TEST-INT-01`: 169 pruebas unitarias exitosas. | Cerrado, fusionado y rama eliminada. |
| `CCC-7480` | Central Frontend | `E-ODOO-INT-02` | `E-GH-INT-06`; `E-GH-INT-08` | `E-TEST-INT-03`: pruebas Karma visibles de `ContractsComponent`; plantilla con 19 pruebas focalizadas exitosas y comprobaciones TypeScript. | Cerrado, fusionado y rama eliminada. |
| `CCC-7477` | Central Frontend | `E-ODOO-INT-03` | `E-GH-INT-07`; `E-GH-INT-09` | Comprobaciones TypeScript declaradas como exitosas; excepción documentada: Karma y escritura de salida bloqueadas por `EPERM`. | Cerrado, fusionado y rama eliminada. |

`CCC-7480` en Central API se conserva como evidencia parcial de aplicación y prueba (`E-GH-INT-03`, `E-GH-INT-05`, `E-TEST-INT-02`), pero no se incorpora al denominador de cambios cerrados porque al corte disponible no tenía evidencia de fusión ni eliminación de rama. Esta decisión evita presentar un cambio en curso como éxito o fracaso concluido.

## Resultado frente a criterios fijados antes de construir

| Indicador | Criterio predefinido | Resultado observable en la serie | Veredicto y límite |
|:--|:--|:--|:--|
| I1. Tareas visibles y válidas | ≥ 80 % de tareas activas visibles y válidas. | 3 de 3 casos tienen tarea visible e identificable en Odoo. Las capturas no permiten auditar todos los campos de “tarea válida” para cada caso. | Visibilidad demostrada; validez completa no calculable. |
| I2. Repositorio institucional o excepción | 100 % de componentes críticos con repositorio institucional o excepción documentada. | Central API y Central Frontend permanecen fuera de la organización institucional. La evidencia disponible describe esa condición, pero no acredita una ficha C0 de excepción formal aplicada para cada componente. | No evaluable como cumplimiento de I2; tampoco se declara institucionalización. |
| I3. Ramas conformes | ≥ 80 % de ramas conformes. | Las tres ramas observables asociadas a los casos siguen `<tipo>/<codigo-tarea>-<descripcion-corta>`. | 3 de 3 casos con rama conforme; no se infiere tasa de todas las ramas del período. |
| I4. *Commits* conformes | ≥ 80 % de *commits* conformes. | Cada caso tiene al menos un *commit* visible con `<tipo>(<codigo-tarea>): <descripcion>`. No se recuperó el historial completo de todos los *commits* de los casos. | Conformidad demostrada por caso; porcentaje de *commits* no calculable. |
| I5. Cambios integrados por solicitud | ≥ 70 % de cambios integrados por solicitud. | Los 3 de 3 cambios cerrados se integraron mediante solicitud fusionada hacia `main`. | Criterio alcanzado en la serie acotada; sin inferencia organizacional. |
| I6. Solicitudes con evidencia mínima | ≥ 70 % de solicitudes con evidencia mínima. | Las 3 de 3 solicitudes cerradas incluyen plantilla: tarea, resumen, riesgo, plan de prueba, verificación y validación o excepción. | Criterio alcanzado en la serie acotada. |
| I7. Verificación técnica | Al menos un componente crítico con evidencia técnica. | API: 169 pruebas unitarias exitosas. Frontend de `CCC-7480`: pruebas Karma focalizadas visibles, 19 pruebas declaradas exitosas y comprobaciones TypeScript. | Criterio alcanzado. |
| I9. Evidencia trazable de entregables | Mejora cualitativa de tarea → rama → *commit* → solicitud → evidencia. | La cadena se recorre en los tres casos; `CCC-7477` conserva una excepción técnica explícita. | Mejora cualitativa demostrada por caso, no sostenida institucionalmente. |

## Interpretación sumativa

La serie demuestra que el marco puede aplicarse en cambios reales de dos componentes de Central y producir trazabilidad visible desde la tarea hasta la integración. También evidencia que la plantilla hace observable la diferencia entre una verificación satisfactoria —como las pruebas de API y las pruebas focalizadas de `CCC-7480`— y una excepción técnica —como el bloqueo `EPERM` en `CCC-7477`. Esta distinción es un resultado de utilidad del artefacto: no obliga a declarar una prueba inexistente como exitosa para completar una solicitud.

La evaluación no demuestra que PRX haya adoptado el marco institucionalmente, que todos los *commits* del período sean conformes ni que los indicadores mejoren de forma sostenida. La falta de una ventana completa y de denominadores exhaustivos impide estimar proporciones organizacionales. En consecuencia, las conclusiones solo sostienen aplicabilidad inicial y utilidad trazable en la serie observada.

## Amenazas a la validez y efecto residual

| Amenaza | Mitigación aplicada | Impacto residual |
|:--|:--|:--|
| Selección de casos cerrados. | Se declara el criterio de inclusión y se conserva `CCC-7480` API como cambio en curso, fuera del denominador. | Alto para tasas de adopción; medio para aplicabilidad de la cadena. |
| Tesista como diseñador y responsable de Central Frontend. | Separación entre evidencia, interpretación y límites; casos API y Frontend se distinguen; no se declara revisión independiente. | Alto para causalidad y adopción independiente. |
| Denominadores incompletos de tareas y *commits*. | No se calculan porcentajes cuando no existe inventario completo. | Alto para I1 e I4; bajo para la existencia de trazas de los casos. |
| Excepción técnica en `CCC-7477`. | La plantilla registra `EPERM` y no la transforma en prueba exitosa. | Medio para la verificación de ese caso. |
| Un solo proyecto y dos componentes. | Condiciones de contorno explícitas y generalización analítica prudente. | Alto para transferencia a otros equipos u organizaciones. |

## Veredicto de E-SUM-02

La evaluación de campo sumativa queda ejecutada como serie acotada de tres casos cerrados de Central. El artefacto demuestra utilidad inicial para producir trazabilidad, integración y evidencia de verificación o de excepción documentada. La contribución de conocimiento queda limitada a principios de diseño de alcance analítico inicial para equipos pequeños con baja estandarización; no se reclama adopción sostenida, eficacia organizacional ni teoría de diseño.

## Referencias

Runeson, P., & Höst, M. (2009). Guidelines for conducting and reporting case study research in software engineering. *Empirical Software Engineering, 14*(2), 131–164. https://doi.org/10.1007/s10664-008-9102-8
