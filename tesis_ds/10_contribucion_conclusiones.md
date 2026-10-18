# E10. Contribución y conclusiones preliminares

## Propósito

Este documento articula la contribución preliminar de la investigación y las conclusiones disponibles hasta el estado actual del trabajo. La contribución se formula como **principios de diseño candidatos**, porque ya se ejecutó una evaluación formativa con una solicitud de integración real en Central y se documentó el rediseño V1.1, pero todavía falta la evaluación sumativa inicial.

Por rigor metodológico, este documento no afirma que los principios estén validados. Los principios se presentan como formulaciones derivadas del diagnóstico, del diseño, de la construcción, de una primera aplicación formativa y de un resultado sumativo inicial de caso; deberán ajustarse después de una medición posterior por periodo comparable.

## Tipo de contribución reclamada

La contribución esperada corresponde al nivel de maestría en Design Science: **principios de diseño para construir marcos ligeros de adopción inicial de prácticas de Ingeniería de Software en equipos pequeños de desarrollo con baja estandarización**. El artefacto construido —el marco V1.0-Central y sus productos operativos— es el vehículo para generar evidencia, no la contribución final por sí mismo.

La tesis no reclama una teoría de diseño general ni una solución universal para todos los equipos de Ingeniería de Software. La generalización prevista es analítica y condicionada: los principios podrán ser útiles para equipos pequeños o áreas de software con baja estandarización, herramientas de trabajo existentes y necesidad de producir evidencia mínima de trazabilidad.

## Contribución preliminar en una oración

Esta investigación propone principios de diseño para construir marcos ligeros, progresivos y verificables de gestión técnica trazable en equipos pequeños de desarrollo con baja estandarización, sustentados en el diseño, construcción y evaluación formativa inicial de un marco aplicado en la línea de software a medida de PRX.

## Principios de diseño candidatos

Los siguientes principios usan la estructura objetivo → contexto → mecanismo → principio. Su estado es **candidato**, no validado.

### P1. Principio de trazabilidad mínima progresiva

Para mejorar la trazabilidad del trabajo técnico en equipos pequeños con baja estandarización, el marco debe exigir una cadena mínima tarea → rama → commit → solicitud de integración → evidencia de verificación, porque una cadena corta y observable reduce ambigüedad operativa sin imponer un proceso pesado.

Este principio se materializa en `STD-GIT-001`, `STD-GIT-002`, `STD-GIT-003` y la plantilla operativa de solicitud de integración. La cadena fue recorrida en `CCC-7336`; su validez sigue siendo preliminar hasta compararla con la línea base y observar un periodo posterior.

### P2. Principio de formalización mínima antes de automatización

Para iniciar adopción en equipos con prácticas heterogéneas y herramientas ya existentes, el marco debe formalizar primero reglas simples y productos de trabajo observables antes de exigir automatización, porque la automatización prematura puede aumentar fricción y ocultar que el equipo todavía no comparte una comprensión común de la práctica.

Este principio justifica que GitHub Actions, validaciones estrictas y reglas automáticas queden como extensión futura. En la versión inicial, la prioridad fue publicar estándares, plantilla y estructura documental, y registrar fricciones de adopción.

### P3. Principio de separación entre estándar y plantilla operativa

Para evitar que una plantilla sea confundida con una regla completa de trabajo, el marco debe diferenciar entre el estándar institucional que define criterios de validez y la plantilla operativa que guía el llenado de la solicitud, porque la plantilla puede estructurar la descripción, pero no cubre por sí sola reglas como título, validación, excepciones y trazabilidad.

Este principio emergió durante la construcción, cuando se distinguió `STD-GIT-002` de `pull_request_template.md`. La distinción permitió cerrar una brecha de diseño: la plantilla de PR no define el título de la solicitud.

### P4. Principio de validación progresiva

Para introducir revisión y control en componentes con disponibilidad limitada de revisores, el marco debe distinguir entre solicitud trazable, plantilla completa, auto-validación documentada, validación automática y revisión por tercero, porque exigir revisión independiente desde el inicio puede bloquear la adopción o producir cumplimiento ficticio.

Este principio responde a la línea base: existían solicitudes de integración, pero no evidencia de revisión independiente. La versión inicial acepta auto-validación documentada como excepción explícita, no como sustituto silencioso de revisión por pares.

### P5. Principio de evidencia mínima verificable

Para mejorar la confianza en los cambios integrados, el marco debe exigir que cada solicitud declare método de verificación y evidencia asociada, porque una solicitud de integración sin evidencia de prueba, construcción o validación no permite distinguir entre integración técnica y cambio verificado.

Este principio se operacionaliza en la plantilla PR y en `STD-GIT-002`. `E-TEST-INT-01` aporta evidencia inicial de 169 pruebas unitarias exitosas en Central API; falta evaluar si la evidencia mínima se sostiene en un periodo posterior.

### P6. Principio de normalización gradual de repositorios históricos

Para estandarizar ramas permanentes en repositorios existentes, el marco debe exigir primero declaración de equivalencias y dependencias antes de renombrar ramas, porque los nombres de ramas pueden estar conectados a despliegues, automatizaciones u Odoo.sh.

Este principio responde a la evidencia de ramas heterogéneas (`Production`, `Prod`, `Stage`, `Staging`, `TEST`, `test` y otras variantes). La normalización gradual reduce riesgo operativo y permite avanzar sin romper mecanismos existentes.

## Condiciones de contorno

Los principios candidatos aplican, hasta donde permite la evidencia actual, bajo estas condiciones:

- equipos pequeños o áreas de software con baja estandarización;
- existencia de algún mecanismo de tareas, aunque sea parcial;
- uso de control de versiones basado en Git o equivalente;
- posibilidad de crear solicitudes de integración o mecanismo equivalente;
- disposición mínima para documentar reglas y excepciones;
- necesidad de trazabilidad observable más que de automatización completa;
- contexto donde la revisión independiente puede no estar siempre disponible.

No se recomienda extrapolar estos principios sin ajuste a organizaciones con procesos altamente regulados, equipos grandes con canales formales de entrega, entornos con cumplimiento normativo estricto o productos donde cada cambio exige auditoría externa.

## Conclusiones preliminares

1. La línea base confirmó que el problema no era ausencia absoluta de herramientas, sino adopción parcial y heterogénea de prácticas de gestión técnica. Esta precisión permitió diseñar un marco ligero y progresivo, en lugar de imponer un modelo de madurez o un proceso pesado.

2. La construcción inicial produjo un conjunto coherente de productos operativos: `STD-GIT-001`, `STD-GIT-002`, `STD-GIT-003`, plantilla operativa de solicitud de integración, estructura documental en SharePoint y repositorio `.github`. En `CCC-7336`, estos productos permitieron crear y fusionar una solicitud de integración con trazabilidad y ejecutar 169 pruebas unitarias exitosas.

3. La evaluación formativa no reportó fricción operativa en `CCC-7336`. Sí produjo un ajuste contextual: `STD-GIT-001` V1.1 formalizó `Stage` y `Production` con mayúscula, alineándose con configuraciones históricas de repositorios Odoo sin atribuirlas retrospectivamente al estándar institucional.

4. La separación entre estándar y plantilla de solicitud de integración fue una decisión de diseño relevante. Sin esa separación, el artefacto habría dejado sin controlar el título del PR, debilitando la trazabilidad.

5. Todavía no existe evidencia suficiente para afirmar que el marco mejora sostenidamente los indicadores en Central. La evaluación sumativa debe comparar un periodo posterior contra la línea base.

## Amenazas a la validez de la contribución

| Amenaza | Impacto | Mitigación |
|:--|:--|:--|
| Principios formulados antes de evaluación completa. | Los principios podrían cambiar después de la aplicación real. | Declararlos como candidatos y actualizarlos tras E8. |
| Intervención realizada por el tesista. | Puede existir sesgo de confirmación. | Documentar fricciones, excepciones y evidencias privadas. |
| Aplicación inicial en un solo proyecto. | Limita transferibilidad. | Declarar generalización analítica y condiciones de contorno. |
| Una aplicación no equivale a adopción. | Un caso real no demuestra uso sostenido. | Ejecutar `E-SUM-01` y limitar afirmaciones al caso formativo mientras tanto. |
| Verificación técnica limitada a un componente. | La evidencia inicial no cubre todos los componentes de Central. | Declarar el alcance de Central API y no extrapolar cobertura institucional. |

## Trabajo pendiente para validar contribución

Para pasar de contribución preliminar a contribución validada, se requiere:

1. Realizar una medición posterior por periodo comparable, que complemente el resultado inicial de caso `E-SUM-01`.
2. Ajustar los principios candidatos en función de evidencia sumativa adicional, no de conveniencia narrativa.

## Estado del gate E10

E10 queda **iniciado como contribución y conclusiones preliminares**, pero no cerrado. Los principios de diseño están formulados con contexto y mecanismo, pero deben validarse mediante evaluación formativa, rediseño y evaluación sumativa inicial. No se debe presentar esta versión como conclusión final de tesis.
