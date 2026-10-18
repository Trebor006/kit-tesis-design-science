# Consolidación de indicadores de línea base

## Propósito

Este documento consolida los indicadores de línea base levantados antes de aplicar el marco ligero progresivo. La finalidad es fijar el punto de comparación para la evaluación posterior del artefacto y evitar que los criterios de éxito se ajusten después de observar resultados. Cuando la evidencia disponible no permite calcular un porcentaje confiable, el valor se declara como parcial, pendiente o contextual, sin inventar precisión numérica.

## Ventana y fuentes

La ventana principal de observación es del **21 de septiembre de 2026** al **4 de octubre de 2026**. La evidencia histórica anterior a esa ventana se conserva como contexto, pero no se contabiliza en los indicadores principales.

Las fuentes usadas son:

- línea base GitHub documentada en `tesis_ds/06_linea_base_github.md`;
- línea base de tareas en Odoo documentada en `tesis_ds/06_linea_base_odoo_tareas.md`;
- instrumentos definidos en `tesis_ds/06_instrumentos_linea_base.md`;
- evidencia contextual declarada por el tesista y desarrolladores, diferenciada de los datos observados en la ventana.

## Tabla consolidada de indicadores

| Indicador | Línea base actual | Fuente principal | Interpretación | Criterio posterior esperado | Estado de evidencia |
|:--|:--|:--|:--|:--|:--|
| I1. Visibilidad de tareas activas | Parcial. Existe evidencia de tareas visibles, pero con granularidad desigual y acceso incompleto en componentes Odoo. | Odoo; `06_linea_base_odoo_tareas.md`. | PConst muestra una tarea visible pero excesivamente amplia; Central tiene evidencia contextual de tareas pequeñas; Central Backend Odoo y Ansular Backend Odoo tienen información insuficiente. | ≥ 80 % de tareas activas visibles y válidas según campos mínimos del marco. | Parcial; requiere evidencia adicional o aceptación de limitación documentada. |
| I2. Componentes con repositorio institucional | 3 de 7 componentes, equivalente a 42,86 %. | GitHub; `06_linea_base_github.md`. | Central Odoo, Central Frontend y Ansular Backend están en PRX; Central API, Ansular Frontend, PConst Backend y PConst Frontend están fuera de la organización institucional. | 100 % de componentes críticos en repositorio institucional o con excepción documentada. | Suficiente para línea base. |
| I3. Cumplimiento de convención documentada de ramas | 0 %. | GitHub; revisión de ramas. | Existen patrones usados en algunos componentes, pero no una convención institucional documentada. | ≥ 80 % de ramas conformes con la convención definida por el marco. | Suficiente para línea base formal. |
| I4. Cumplimiento de convención documentada de commits | 0 %. | GitHub; revisión de commits. | Central Odoo y Central Frontend muestran prácticas aparentes, pero no existe estándar institucional documentado. | ≥ 80 % de commits conformes con la convención definida por el marco. | Suficiente para línea base formal. |
| I5. Cambios integrados mediante solicitudes de integración | 5 de 5 cambios integrados observables en GitHub durante la ventana, equivalente a 100 %. | GitHub; `06_linea_base_github.md`. | Central Odoo registró 1 solicitud y Ansular Backend 4 solicitudes; todas fueron fusionadas dentro de las fechas indicadas. Este valor solo cubre cambios observables en GitHub durante la ventana; no incluye trabajo no subido, como el caso reportado de Central API. Además, no implica revisión independiente, porque en varios componentes un solo desarrollador crea y fusiona sus propias solicitudes. | ≥ 70 % de cambios integrados mediante solicitud de integración. | Suficiente para cambios observables en GitHub; mantener advertencia sobre trabajo no trazado y ausencia de revisión independiente. |
| I6. Solicitudes con evidencia mínima de verificación | 0 de 5 solicitudes, equivalente a 0 %. | GitHub; revisión de solicitudes. | Las solicitudes registradas tienen commits y ramas asociadas, pero no evidencia mínima de verificación declarada. | ≥ 70 % de solicitudes con evidencia mínima de verificación. | Suficiente para línea base. |
| I7. Componentes críticos con verificación técnica mínima | Parcial. PConst tiene pruebas unitarias, pruebas de integración y pruebas de extremo a extremo declaradas; falta evidencia posterior ejecutada y vinculada a una solicitud real de Central. | Repositorios; declaración del tesista; pendiente de ejecución/evidencia. | Existen capacidades técnicas heterogéneas, pero todavía no constituyen un estándar institucional común ni evidencian aplicación del marco en Central. | Al menos un componente crítico de Central con prueba, construcción, prueba de API o verificación técnica documentada. | Parcial; requiere `E-TEST-INT-01`. |
| I8. Defectos o correcciones urgentes | Contextual. Se observan cambios correctivos en Ansular Backend y antecedentes de correcciones o ajustes, pero no se usará como criterio principal. | GitHub; entrevistas/declaraciones; solicitudes Odoo. | La ventana es insuficiente para inferir reducción de defectos; sirve para interpretar necesidad de verificación y revisión. | No aplica como criterio principal; se usará para interpretación cualitativa. | Contextual. |
| I9. Evidencia trazable para respaldo de entregables | Parcial. Existen cadenas de trazabilidad incompletas; Central Frontend muestra trazabilidad histórica local, pero no es estándar institucional. | Odoo + GitHub; `06_linea_base_odoo_tareas.md`; `06_linea_base_github.md`. | La cadena tarea → rama → commit → solicitud → evidencia existe solo en casos aislados y, en algunos casos, fuera de la ventana. | Mejora cualitativa documentada en trazabilidad de entregables; no se fija porcentaje principal en esta versión. | Parcial; suficiente como indicador contextual. |

## Lectura diagnóstica de la línea base

La línea base muestra un patrón consistente: PRX no parte de ausencia absoluta de herramientas ni de prácticas técnicas, sino de una adopción parcial, heterogénea y dependiente de personas. Existen repositorios, solicitudes de integración, tareas y pruebas en algunos componentes, pero no hay una regla común que permita exigir evidencia homogénea. Este hallazgo evita formular el problema como “no usan buenas prácticas” y lo precisa como ausencia de un marco común, ligero y verificable.

El caso GitHub confirma la falta de institucionalización completa: solo 3 de 7 componentes están en la organización PRX. El caso de solicitudes de integración muestra una tensión relevante: los 5 cambios integrados observables en GitHub durante la ventana pasaron por solicitudes de integración fusionadas, pero no necesariamente por revisión independiente, ya que en varios componentes un solo desarrollador concentra el trabajo y puede fusionar sus propias solicitudes. Además, 0 de esas 5 solicitudes incluyeron evidencia mínima de verificación. Por tanto, el problema no es únicamente abrir solicitudes de integración, sino convertirlas en un mecanismo verificable de revisión, trazabilidad y control. El caso Odoo muestra dos extremos: PConst tenía una tarea visible pero demasiado amplia, mientras Central Frontend presenta trazabilidad histórica más ordenada porque el tesista introdujo prácticas locales. Esta variación entre componentes es precisamente la razón para diseñar un marco común.

## Implicaciones para el diseño del artefacto

| Hallazgo | Implicación de diseño |
|:--|:--|
| Repositorios fuera de PRX o con ubicación ambigua. | El marco debe exigir repositorio oficial o excepción documentada. |
| Convenciones usadas pero no documentadas. | El marco debe diferenciar práctica informal de regla institucional verificable. |
| Nombres de ramas permanentes y de validación no estandarizados; ausencia de `Stage` o `Production` en algunos repositorios; rama por defecto variable. | El marco debe exigir que cada repositorio documente sus ramas oficiales, su propósito, su rama por defecto y sus equivalencias antes de imponer renombramientos. |
| Solicitudes sin evidencia de verificación. | El marco debe definir solicitud de integración válida y evidencia mínima aceptable. |
| Solicitudes creadas y fusionadas por la misma persona. | El marco debe distinguir entre solicitud de integración trazable y solicitud de integración revisada por un tercero, con excepción documentada para componentes de un solo desarrollador. |
| Ausencia de revisión independiente como práctica institucional observable. | El marco no debe asumir revisión por pares inexistente; debe introducir validación progresiva: solicitud trazable, plantilla completa, evidencia mínima, validación documentada y revisión por tercero cuando sea factible. |
| Tickets demasiado grandes. | El marco debe definir tarea válida, granularidad y criterio de división. |
| Prácticas locales introducidas por el tesista. | El marco debe convertir prácticas aisladas en reglas comunes, no atribuirlas falsamente a toda la organización. |
| Cambios no subidos a repositorio durante la ventana. | El marco debe visibilizar trabajo no trazado y exigir vínculo entre tarea y cambio técnico. |

## Delimitación de aplicación inicial

Aunque la línea base considera evidencia de Central, Ansular y PConst, la primera aplicación del marco se concentrará en **Central**. Esta decisión reduce el alcance operativo y mejora la observabilidad, porque Central contiene tres componentes —Odoo, API y frontend— y permite analizar cómo el marco coordina trabajo entre desarrolladores distintos. Ansular y PConst permanecerán como evidencia diagnóstica y contraste contextual, pero no como foco principal de la primera evaluación.

## Estado del cierre de E6

E6 queda suficientemente consolidada para avanzar al diseño del artefacto. No obstante, no se declara cerrada de forma absoluta porque todavía faltan evidencias privadas o capturas mínimas de respaldo, especialmente en repositorios Odoo y en pruebas unitarias por proyecto. Estas ausencias no impiden avanzar a E7b, pero deben mantenerse registradas como limitaciones y amenazas a la validez.

## Declaración de fijación de línea base

Los valores de línea base fueron levantados sobre la ventana del 21 de septiembre de 2026 al 4 de octubre de 2026, antes de aplicar el marco ligero progresivo. Cualquier cambio posterior en indicadores, criterios o valores esperados deberá tratarse como rediseño documentado y no como ajuste retroactivo de la evaluación.
