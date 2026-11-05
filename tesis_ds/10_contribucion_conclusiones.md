# E10. Contribución y conclusiones

## Propósito

Este documento articula la contribución y las conclusiones resultantes del diagnóstico, la construcción, la evaluación formativa con rediseño V1.1 y la evaluación de campo sumativa mediante una serie acotada de tres casos cerrados en Central. La contribución se formula como principios de diseño con **respaldo empírico inicial**, no como teoría de diseño ni como evidencia de adopción institucional sostenida.

La evaluación sumativa no recuperó un período completo comparable con la línea base. Por rigor metodológico, los principios se formulan con generalización analítica limitada: distinguen entre principios respaldados directamente en los tres casos, principios parcialmente respaldados y decisiones de diseño aún no evaluadas. Esta precisión impide convertir una serie de casos útiles en una afirmación que la evidencia no soporta.

## Tipo de contribución reclamada

La contribución esperada corresponde al nivel de maestría en Design Science: **principios de diseño para construir marcos ligeros de adopción inicial de prácticas de Ingeniería de Software en equipos pequeños de desarrollo con baja estandarización**. El artefacto construido —el marco V1.0-Central y sus productos operativos— es el vehículo para generar evidencia, no la contribución final por sí mismo.

La tesis no reclama una teoría de diseño general ni una solución universal para todos los equipos de Ingeniería de Software. La generalización prevista es analítica y condicionada: los principios podrán ser útiles para equipos pequeños o áreas de software con baja estandarización, herramientas de trabajo existentes y necesidad de producir evidencia mínima de trazabilidad.

## Contribución en una oración

Esta investigación aporta principios de diseño con respaldo empírico inicial para construir marcos ligeros, progresivos y verificables de gestión técnica trazable en equipos pequeños de desarrollo con baja estandarización, sustentados en el diseño, construcción, rediseño y evaluación de tres cambios reales en Central.

## Principios de diseño y nivel de respaldo

Los siguientes principios usan la estructura objetivo → contexto → mecanismo → principio. Su respaldo se califica de acuerdo con `E-SUM-02`, sin atribuir a todos la misma fuerza de evidencia.

### P1. Principio de trazabilidad mínima progresiva

Para mejorar la trazabilidad del trabajo técnico en equipos pequeños con baja estandarización, el marco debe exigir una cadena mínima tarea → rama → commit → solicitud de integración → evidencia de verificación, porque una cadena corta y observable reduce ambigüedad operativa sin imponer un proceso pesado.

Este principio se materializa en `STD-GIT-001`, `STD-GIT-002`, `STD-GIT-003` y la plantilla operativa de solicitud de integración. La cadena fue recorrida en `CCC-7336`, `CCC-7480` Frontend y `CCC-7477`; su respaldo es inicial y se limita a los tres cambios cerrados de Central.

### P2. Principio de formalización mínima antes de automatización

Para iniciar adopción en equipos con prácticas heterogéneas y herramientas ya existentes, el marco debe formalizar primero reglas simples y productos de trabajo observables antes de exigir automatización, porque la automatización prematura puede aumentar fricción y ocultar que el equipo todavía no comparte una comprensión común de la práctica.

Este principio justifica que GitHub Actions, validaciones estrictas y reglas automáticas queden como extensión futura. En la versión inicial, la prioridad fue publicar estándares, plantilla y estructura documental, y registrar fricciones de adopción. La serie evidencia que la formalización permitió aplicar la cadena en cambios reales; no compara su costo o efectividad contra una automatización temprana.

### P3. Principio de separación entre estándar y plantilla operativa

Para evitar que una plantilla sea confundida con una regla completa de trabajo, el marco debe diferenciar entre el estándar institucional que define criterios de validez y la plantilla operativa que guía el llenado de la solicitud, porque la plantilla puede estructurar la descripción, pero no cubre por sí sola reglas como título, validación, excepciones y trazabilidad.

Este principio emergió durante la construcción, cuando se distinguió `STD-GIT-002` de `pull_request_template.md`. Las tres solicitudes cerradas conservaron título trazable y plantilla con tareas, riesgo, verificación y validación, lo que respalda inicialmente que ambos productos cumplen funciones distintas.

### P4. Principio de validación progresiva

Para introducir revisión y control en componentes con disponibilidad limitada de revisores, el marco debe distinguir entre solicitud trazable, plantilla completa, auto-validación documentada, validación automática y revisión por tercero, porque exigir revisión independiente desde el inicio puede bloquear la adopción o producir cumplimiento ficticio.

Este principio responde a la línea base: existían solicitudes de integración, pero no evidencia de revisión independiente. Las plantillas de `CCC-7480` y `CCC-7477` registran auto-validación y excepción de forma explícita, no como sustituto silencioso de revisión por pares. La evaluación no prueba todavía que esta progresión mejore la calidad frente a una revisión independiente.

### P5. Principio de evidencia mínima verificable

Para mejorar la confianza en los cambios integrados, el marco debe exigir que cada solicitud declare método de verificación y evidencia asociada, porque una solicitud de integración sin evidencia de prueba, construcción o validación no permite distinguir entre integración técnica y cambio verificado.

Este principio se operacionaliza en la plantilla PR y en `STD-GIT-002`. `E-TEST-INT-01` aporta 169 pruebas unitarias exitosas en Central API; `CCC-7480` Frontend aporta pruebas focalizadas visibles y comprobaciones TypeScript, mientras `CCC-7477` registra una excepción técnica explícita. Las tres solicitudes cerradas documentan evidencia o excepción, lo que respalda el principio en la serie, no su sostenimiento organizacional.

### P6. Principio de normalización gradual de repositorios históricos

Para estandarizar ramas permanentes en repositorios existentes, el marco debe exigir primero declaración de equivalencias y dependencias antes de renombrar ramas, porque los nombres de ramas pueden estar conectados a despliegues, automatizaciones u Odoo.sh.

Este principio responde a la evidencia de ramas heterogéneas (`Production`, `Prod`, `Stage`, `Staging`, `TEST`, `test` y otras variantes). La normalización gradual reduce riesgo operativo y permite avanzar sin romper mecanismos existentes. No fue evaluado en una transición de repositorio o entrega real; permanece como decisión de diseño fundamentada para evaluación posterior.

## Clasificación explícita del respaldo

| Principio | Respaldo de la evaluación | Interpretación admisible |
|:--|:--|:--|
| P1. Trazabilidad mínima progresiva | Directo en tres cambios cerrados. | Principio con respaldo empírico inicial de aplicabilidad. |
| P2. Formalización mínima antes de automatización | Parcial: la formalización antecede las aplicaciones, sin comparación con automatización. | Decisión de diseño plausible; no se afirma superioridad causal. |
| P3. Separación entre estándar y plantilla | Directo en tres solicitudes completas. | Principio con respaldo empírico inicial de utilidad operativa. |
| P4. Validación progresiva | Parcial: auto-validación y excepción documentadas; sin revisión por tercero comparada. | Principio condicionado para contextos con revisores limitados. |
| P5. Evidencia mínima verificable | Directo en tres solicitudes, con resultados y excepción visibles. | Principio con respaldo empírico inicial de utilidad y transparencia. |
| P6. Normalización gradual de repositorios históricos | Sin evaluación de transición ni entrega real. | Decisión fundamentada; no se presenta como principio validado. |

## Condiciones de contorno

Los principios aplican, hasta donde permite la evidencia actual, bajo estas condiciones:

- equipos pequeños o áreas de software con baja estandarización;
- existencia de algún mecanismo de tareas, aunque sea parcial;
- uso de control de versiones basado en Git o equivalente;
- posibilidad de crear solicitudes de integración o mecanismo equivalente;
- disposición mínima para documentar reglas y excepciones;
- necesidad de trazabilidad observable más que de automatización completa;
- contexto donde la revisión independiente puede no estar siempre disponible.

No se recomienda extrapolar estos principios sin ajuste a organizaciones con procesos altamente regulados, equipos grandes con canales formales de entrega, entornos con cumplimiento normativo estricto o productos donde cada cambio exige auditoría externa.

## Conclusiones

1. La línea base confirmó que el problema no era ausencia absoluta de herramientas, sino adopción parcial y heterogénea de prácticas de gestión técnica. Esta precisión permitió diseñar un marco ligero y progresivo, en lugar de imponer un modelo de madurez o un proceso pesado.

2. La construcción inicial produjo un conjunto coherente de productos operativos: `STD-GIT-001`, `STD-GIT-002`, `STD-GIT-003`, plantilla operativa de solicitud de integración, estructura documental en SharePoint y repositorio `.github`. En `CCC-7336`, `CCC-7480` Frontend y `CCC-7477`, estos productos permitieron crear tareas trazables, solicitudes fusionadas y evidencia de verificación o excepción explícita.

3. La evaluación formativa no reportó fricción operativa en `CCC-7336`. Sí produjo un ajuste contextual: `STD-GIT-001` V1.1 formalizó `Stage` y `Production` con mayúscula, alineándose con configuraciones históricas de repositorios Odoo sin atribuirlas retrospectivamente al estándar institucional.

4. La separación entre estándar y plantilla de solicitud de integración fue una decisión de diseño relevante. Sin esa separación, el artefacto habría dejado sin controlar el título del PR, debilitando la trazabilidad.

5. La evaluación sumativa de tres casos demuestra utilidad inicial del marco, pero no evidencia suficiente para afirmar que mejora sostenidamente los indicadores de Central. Las afirmaciones finales se restringen a aplicabilidad, trazabilidad y transparencia de verificación o excepción en los cambios observados.

## Amenazas a la validez de la contribución

| Amenaza | Impacto | Mitigación |
|:--|:--|:--|
| Serie sumativa acotada, no período completo. | Los principios pueden sobreestimar adopción si se extrapolan a todos los cambios. | Declarar serie, criterios de inclusión y ausencia de tasas organizacionales. |
| Intervención realizada por el tesista. | Puede existir sesgo de confirmación. | Documentar fricciones, excepciones y evidencias privadas. |
| Aplicación inicial en un solo proyecto. | Limita transferibilidad. | Declarar generalización analítica y condiciones de contorno. |
| Tres aplicaciones no equivalen a adopción. | La serie no demuestra uso sostenido ni institucional. | Limitar la contribución a aplicabilidad inicial y reevaluar ante nuevos cambios de Central. |
| Verificación técnica limitada a dos componentes y tres casos. | La evidencia no cubre todos los componentes ni todos los cambios de Central. | Declarar el alcance de Central API y Central Frontend, sin extrapolar cobertura institucional. |

## Trabajo futuro

1. Repetir la evaluación con todos los cambios de una ventana posterior completa, incluyendo denominadores de tareas y *commits*.
2. Evaluar C5 en una entrega real y documentar el resultado de las excepciones de repositorio externo.
3. Contrastar P2, P4 y P6 con otro equipo o proyecto antes de ampliar su alcance.

## Estado del gate E10

E10 queda **cerrado con contribución de alcance analítico inicial**. P1, P3 y P5 cuentan con respaldo directo en la evaluación de campo sumativa; P2 y P4 son principios parcialmente respaldados y P6 queda como decisión de diseño no validada. La tesis no reclama teoría de diseño, adopción institucional ni efectividad sostenida.
