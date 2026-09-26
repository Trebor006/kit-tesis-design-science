# E6. Diagnóstico con indicadores y criterios

## Propósito del diagnóstico

El diagnóstico no se formulará como una descripción general de PRX. En Design Science, el diagnóstico debe demostrar que el problema de diseño existe y establecer una línea base contra la cual se evaluará el artefacto. Por ello, los indicadores se concentran en las cuatro prácticas seleccionadas para el marco ligero: gestión visible de tareas, convención de ramas y commits, solicitudes de integración de cambios y pruebas unitarias iniciales.

Los valores esperados se fijan antes de construir el artefacto, para evitar criterios definidos a posteriori. Las líneas base numéricas no deben inventarse: se levantarán antes de aplicar el marco mediante Revisión del tablero interno de gestión de tareas implementado en Odoo, GitHub, repositorios de proyectos piloto y entrevistas breves con participantes. Si un proyecto no tiene registro suficiente, esa ausencia se documentará como parte de la línea base.

## Unidad de análisis

- **Organización:** PRX.
- **Línea de trabajo evaluada:** software a medida.
- **Participantes previstos:** cinco desarrolladores.
- **Periodo de observación previsto:** dos semanas.
- **Herramientas observables:** Odoo para tareas y GitHub institucional para repositorios, ramas, commits y solicitudes de integración de cambios.
- **Proyectos piloto:** pendientes de selección formal; la evidencia preliminar proviene de Central, Ansular y PConst.

## Indicadores del diagnóstico

| Código | Indicador | Definición operacional | Fórmula o regla de medición | Fuente de datos | Línea base | Valor esperado | Relación con el problema |
|:--|:--|:--|:--|:--|:--|:--|:--|
| I1 | Visibilidad de tareas activas | Proporción de tareas reales del equipo que están registradas y visibles en el tablero interno de gestión de tareas implementado en Odoo durante el periodo de observación. | `(Número de tareas activas registradas en Odoo / Número total de tareas activas identificadas por Odoo + entrevista + observación) × 100` | Tablero interno de gestión de tareas implementado en Odoo; entrevista breve a desarrolladores; revisión de asignaciones del responsable del equipo. | A levantar antes de aplicar el marco. La evidencia cualitativa inicial indica adopción irregular de Odoo y autogestión no registrada. | ≥ 80 % de tareas activas visibles. | Mide si el marco mejora la visibilidad del trabajo y reduce autogestión invisible. |
| I2 | Proyectos con repositorio institucional | Existencia de repositorio en GitHub institucional de PRX para cada proyecto piloto. | `Sí/No` por proyecto piloto; opcionalmente `% de proyectos piloto con repositorio institucional`. | GitHub institucional de PRX; revisión de proyectos piloto. | A levantar antes de aplicar el marco. La evidencia inicial indica que algunos repositorios fueron creados tardíamente o tuvieron que solicitarse. | 100 % de proyectos piloto con repositorio institucional antes de aplicar las prácticas de ramas, commits y solicitudes de integración. | Es precondición para trazabilidad técnica y control de cambios. |
| I3 | Cumplimiento de convención de ramas | Proporción de ramas creadas durante el periodo que cumplen la convención mínima definida por el marco. | `(Número de ramas conformes / Número total de ramas creadas en el periodo) × 100` | GitHub; historial de ramas; revisión del repositorio. | A levantar antes de aplicar el marco. Si no existe convención previa, la línea base se registra como 0 % de conformidad formal. | ≥ 80 % de ramas conformes. | Mide orden mínimo del trabajo técnico y trazabilidad de cambios. |
| I4 | Cumplimiento de convención de commits | Proporción de commits del periodo que cumplen la convención mínima definida por el marco. | `(Número de commits conformes / Número total de commits del periodo) × 100` | GitHub; historial de commits. | A levantar antes de aplicar el marco. Si no existe convención previa, la línea base se registra como 0 % de conformidad formal. | ≥ 80 % de commits conformes. | Mide trazabilidad comprensible de cambios y reducción de ambigüedad técnica. |
| I5 | Cambios integrados mediante solicitudes de integración | Proporción de cambios integrados a la rama principal mediante solicitudes de integración de cambios en GitHub. | `(Número de cambios integrados mediante solicitud de integración / Número total de cambios integrados a rama principal) × 100` | GitHub; historial de solicitudes de integración y fusiones. | A levantar antes de aplicar el marco. La evidencia inicial indica ausencia o uso no estabilizado de solicitudes de integración. | ≥ 70 % de cambios integrados mediante solicitudes de integración. | Mide revisión previa y control mínimo antes de integrar cambios. |
| I6 | Solicitudes de integración con evidencia mínima de verificación | Proporción de solicitudes de integración que incluyen descripción del cambio y evidencia mínima de verificación, como prueba ejecutada, captura, lista de verificación o resultado de pruebas unitarias. | `(Número de solicitudes de integración con evidencia mínima / Número total de solicitudes de integración del periodo) × 100` | GitHub; descripción de solicitudes de integración; comentarios de revisión; resultados de pruebas si existen. | A levantar antes de aplicar el marco. Si no existen solicitudes de integración, la línea base es 0 %. | ≥ 70 % de solicitudes de integración con evidencia mínima de verificación. | Mide si la solicitud de integración funciona como mecanismo de control y no solo como trámite. |
| I7 | Componentes críticos con pruebas unitarias iniciales | Existencia de pruebas unitarias ejecutables para al menos un componente crítico por proyecto piloto. | `Sí/No` por proyecto piloto; evidencia: comando de ejecución y resultado. | Repositorio GitHub; código fuente; herramienta de pruebas del proyecto. | A levantar antes de aplicar el marco. La evidencia inicial indica ausencia de pruebas unitarias en PConst e incorporación posterior de pruebas en API de Central. | Al menos un componente crítico por proyecto piloto con pruebas unitarias ejecutables. | Mide verificación básica del código en áreas de mayor riesgo. |
| I8 | Defectos o correcciones urgentes asociados a cambios recientes | Número de defectos o correcciones urgentes reportadas durante el periodo y asociadas a cambios recientes. | Conteo de incidencias registradas o reportadas por entrevista breve; clasificación por proyecto. | tablero interno de gestión de tareas implementado en Odoo si registra incidencias; GitHub Issues si aplica; entrevistas; mensajes o registros internos disponibles. | A levantar antes de aplicar el marco. La evidencia inicial incluye defectos introducidos durante refactorización en Ansular. | No se fija reducción porcentual en dos semanas; se usará como indicador contextual y de amenaza a la validez. | Ayuda a interpretar si la verificación mínima reduce riesgo, pero el periodo es corto para prometer reducción estadística. |

## Criterios de éxito fijados antes de la construcción

Los criterios de éxito principales del artefacto serán los siguientes:

1. **Criterio de visibilidad:** al menos 80 % de las tareas activas del equipo de software a medida estarán registradas y visibles en el tablero interno de gestión de tareas implementado en Odoo durante el periodo de evaluación.
2. **Criterio de trazabilidad de ramas y commits:** al menos 80 % de las ramas y commits creados durante el periodo cumplirán la convención mínima definida por el marco.
3. **Criterio de revisión previa:** al menos 70 % de los cambios integrados a la rama principal pasarán por solicitudes de integración de cambios en GitHub.
4. **Criterio de verificación mínima:** al menos 70 % de las solicitudes de integración incluirán evidencia mínima de verificación.
5. **Criterio de pruebas unitarias iniciales:** al menos un componente crítico por proyecto piloto contará con pruebas unitarias ejecutables.
6. **Criterio de aplicabilidad:** los cinco desarrolladores participantes podrán aplicar las reglas del marco durante el periodo de evaluación sin requerir capacitación extensa ni intervención permanente del investigador.

## Indicadores no usados como criterios de éxito principales

El número de defectos o correcciones urgentes se registrará como evidencia contextual, pero no será criterio principal de éxito en esta versión del estudio. Dos semanas no bastan para demostrar reducción confiable de defectos en producción, y prometerlo produciría una afirmación más amplia que la evidencia disponible. Este indicador servirá para interpretar riesgos y orientar trabajo futuro, no para declarar éxito o fracaso del marco.

## Fuentes mínimas para levantar línea base

La línea base debe levantarse antes de construir o aplicar el artefacto mediante cuatro fuentes:

1. Revisión del tablero interno de gestión de tareas implementado en Odoo para identificar tareas activas, tareas no registradas y responsables.
2. Revisión del GitHub institucional de PRX para verificar repositorios, ramas, commits y solicitudes de integración.
3. Revisión de repositorios de proyectos piloto para identificar pruebas unitarias existentes y forma de ejecución.
4. Entrevistas breves a los cinco desarrolladores para detectar trabajo no visible, fricciones de Git y prácticas reales no registradas.

## Advertencia metodológica

Los criterios quedan fijados antes de construir el artefacto. Si durante el ciclo formativo se descubre que un criterio fue técnicamente inviable o que no mide el problema real, el cambio podrá realizarse únicamente como rediseño documentado, indicando fecha, razón y efecto sobre la evaluación. No se aceptará ajustar criterios después de observar resultados para hacer que el artefacto parezca exitoso.

## Estado del gate E6

E6 queda en estado preliminar. Los indicadores tienen definición operacional, fuente de datos y valor esperado, pero las líneas base numéricas todavía deben levantarse antes de aplicar el marco. El gate no se cerrará hasta contar con al menos una medición inicial real de Odoo, GitHub y repositorios piloto, además de evidencia de contexto obtenida mediante entrevistas o revisión documental.


## Plan operativo para levantar la línea base

La línea base se levantará antes de aplicar el marco y antes de construir la versión operacional del artefacto. Esta regla protege la evaluación contra criterios definidos a posteriori y permite demostrar que el problema de diseño existe con evidencia del contexto, no solo con percepción del investigador. La línea base no debe completarse con estimaciones informales cuando existan registros verificables en el tablero interno de gestión de tareas implementado en Odoo o en GitHub.

### Ventana de observación

La ventana mínima de observación será de dos semanas previas a la aplicación del marco, o el periodo inmediatamente anterior que contenga actividad suficiente en los proyectos piloto seleccionados. Si no existe actividad suficiente en dos semanas, se ampliará retrospectivamente la revisión de GitHub hasta encontrar cambios relevantes, documentando la fecha inicial y final usada para cada repositorio. Esta decisión debe registrarse porque puede afectar la comparabilidad entre línea base y evaluación sumativa.

### Proyectos piloto

Los proyectos piloto se seleccionarán con tres criterios: a) pertenecer a la línea de software a medida; b) tener actividad reciente o planificada durante el periodo de evaluación; c) permitir observación de tareas, cambios de código y verificación básica. La evidencia preliminar proviene de Central, Ansular y PConst, pero la selección final no debe asumirse sin verificar disponibilidad real de repositorios, participantes y trabajo activo.

| Proyecto candidato | Criterio de inclusión | Evidencia disponible | Decisión de selección | Observación |
|:--|:--|:--|:--|:--|
| Central | Actividad en línea de software a medida; evidencia previa de pruebas incorporadas posteriormente. | Por confirmar en GitHub y tablero interno de tareas. | Pendiente. | No registrar como piloto hasta verificar actividad durante la ventana. |
| Ansular | Evidencia preliminar de defectos introducidos por refactorización. | Por confirmar en GitHub, tareas e incidencias. | Pendiente. | Útil para observar trazabilidad y verificación mínima. |
| PConst | Evidencia preliminar de ausencia de pruebas unitarias. | Por confirmar en repositorio y tareas. | Pendiente. | Útil para observar incorporación inicial de pruebas. |

### Procedimiento de recolección

1. **Congelar la fecha de línea base.** Registrar fecha y hora de inicio del levantamiento, responsable y ventana observada.
2. **Seleccionar proyectos piloto.** Confirmar que cada proyecto tenga trabajo activo, repositorio disponible o necesidad explícita de crearlo, y participación de al menos un desarrollador del equipo evaluado.
3. **Revisar el tablero interno de gestión de tareas implementado en Odoo.** Extraer tareas activas, responsables, estado, fecha de creación y relación con trabajo real declarado por los desarrolladores.
4. **Revisar GitHub institucional.** Verificar existencia de repositorio, ramas creadas, commits, fusiones a rama principal, solicitudes de integración de cambios y evidencia de verificación registrada.
5. **Revisar pruebas unitarias.** Identificar si existe estructura de pruebas, comando de ejecución, pruebas ejecutables y componentes críticos cubiertos.
6. **Realizar entrevistas breves.** Confirmar trabajo no registrado, fricciones de uso de GitHub, prácticas reales de integración y verificación, y casos recientes de correcciones urgentes.
7. **Consolidar indicadores.** Calcular I1 a I8 con evidencia trazable; cuando un dato no exista, registrar “sin evidencia disponible” en lugar de inventar un valor.
8. **Firmar cierre de línea base.** Registrar que los valores fueron fijados antes de aplicar el marco y antes de ejecutar la evaluación formativa.

### Reglas de codificación para los indicadores

| Indicador | Regla de codificación | Decisión ante ausencia de dato |
|:--|:--|:--|
| I1. Visibilidad de tareas activas | Una tarea cuenta como visible si está registrada en el tablero interno de gestión de tareas implementado en Odoo, tiene responsable y corresponde a trabajo activo del periodo. | Si el desarrollador declara trabajo activo no registrado, cuenta en el denominador, no en el numerador. |
| I2. Repositorio institucional | Un proyecto cumple si su repositorio existe en la cuenta institucional de GitHub de PRX antes de aplicar las prácticas. | Si el código está en repositorio personal o comprimido localmente, se registra como no conforme. |
| I3. Convención de ramas | Una rama es conforme si sigue la convención mínima que será declarada por el marco. Si antes del marco no existe convención, la conformidad formal es 0 %. | No inferir conformidad por nombres “entendibles” si no existía convención previa documentada. |
| I4. Convención de commits | Un commit es conforme si su mensaje sigue la convención mínima declarada. Si no había convención previa, la conformidad formal es 0 %. | No reclasificar commits antiguos como conformes después de definir la convención. |
| I5. Solicitudes de integración | Un cambio cuenta como integrado mediante solicitud si existe registro de solicitud de integración de cambios asociado a la fusión. | Fusiones directas a rama principal cuentan en el denominador y no en el numerador. |
| I6. Evidencia mínima de verificación | La solicitud cuenta si incluye descripción y evidencia verificable: prueba ejecutada, captura, lista de verificación, resultado de prueba o comentario técnico equivalente. | Una solicitud vacía o con solo “listo” no cuenta como evidencia mínima. |
| I7. Pruebas unitarias iniciales | Cumple si existe al menos una prueba unitaria ejecutable para un componente crítico y se registra comando/resultado de ejecución. | Código de prueba no ejecutable o no verificable no cuenta. |
| I8. Defectos o correcciones urgentes | Registrar conteo y descripción breve de defectos asociados a cambios recientes. | Si no hay registro formal, usar entrevista como evidencia cualitativa y marcar fuente. |

### Control de sesgos durante la línea base

La línea base será vulnerable al sesgo del investigador porque el tesista conoce el artefacto que se quiere construir y puede tender a seleccionar evidencia que confirme el problema. Para mitigar esa amenaza, cada valor deberá estar respaldado por una fuente rastreable: enlace o captura del tablero interno de tareas, enlace o identificador de GitHub, resultado de comando de pruebas, o respuesta de entrevista fechada. Cuando exista discrepancia entre lo declarado por un participante y lo registrado en herramientas, la discrepancia se documentará como hallazgo, no se resolverá por intuición.

### Instrumentos mínimos de recolección

Los instrumentos operativos se documentan en `tesis_ds/06_instrumentos_linea_base.md`. Ese archivo contiene la ficha de extracción de tareas, la ficha de extracción de GitHub, la ficha de pruebas unitarias y la guía de entrevista breve. Ningún instrumento debe modificarse después de levantar datos sin registrar fecha, motivo y efecto sobre la comparabilidad.

## Estado actualizado del gate E6

E6 queda fortalecido, pero todavía no cerrado. Ya existen indicadores, reglas de codificación, fuentes, procedimiento de línea base e instrumentos mínimos. El cierre metodológico de E6 ocurrirá solo cuando se registren valores reales de línea base para los proyectos piloto seleccionados y exista al menos una fuente de contexto real adicional a la literatura, como entrevistas breves o revisión documental interna.
