# Estado de la tesis Design Science

## Identificación

- **Tesista:** Robert Cabrera Lara.
- **Programa:** Maestría en Ingeniería de Software.
- **Tutor:** Luis Roberto Pérez Rios, Ph.D.
- **Fecha de inicio:** 2026-09-22.
- **Enfoque metodológico:** Design Science en Ingeniería de Software.

## Encuadre metodológico

El trabajo se desarrollará bajo el estándar de una tesis de maestría en Design Science. En este nivel, la contribución esperada no se limita a construir un artefacto útil para una organización, sino a formular principios de diseño validados y transferibles analíticamente a una clase de problemas. La instanciación, método, marco, modelo o guía que se construya será el vehículo de aprendizaje y evaluación; la contribución de conocimiento deberá expresarse posteriormente como principios de diseño sustentados en evidencia.

## Avances previos declarados

Robert Cabrera Lara declaró una idea inicial orientada a construir una guía para ayudar a una empresa que desarrolla software de manera artesanal a avanzar desde un nivel inicial de madurez hacia prácticas mínimas de gestión y desarrollo. La motivación surge del caso de PRX, empresa que originalmente se dedicaba a la venta de servidores y que actualmente ofrece servicios de desarrollo de software sin contar con procesos definidos. Según el análisis preliminar del tesista, la empresa se encontraría en un nivel inicial o equivalente a nivel 0 respecto a CMMI, aunque esta afirmación todavía requiere verificación conceptual y empírica.

El tesista propone que la guía no sirva solo para PRX, sino también para empresas emergentes formadas por estudiantes o equipos pequeños que desean fundar una empresa de software y no saben cómo iniciar prácticas mínimas de desarrollo. Esta intuición apunta inicialmente a un posible artefacto de tipo método, guía operativa o marco ligero de adopción de prácticas, pero la tipología no está decidida.

## Experiencia del tesista

El tesista es ingeniero de software, cuenta con diplomados en DevOps y gestión de software, cursa la Maestría en Ingeniería de Software y declara cerca de diez años de experiencia en desarrollo de software. Indica experiencia amplia en metodologías, patrones, diseño y temas relacionados con ingeniería de software.

## Restricciones de tiempo

- **Tiempo disponible declarado:** un mes.
- **Fecha exacta de entrega del perfil:** 2026-09-28.
- **Fecha prevista de defensa:** pendiente de precisar.

## Etapas completadas

- E0. Encuadre: completada el 2026-09-22.

## Decisiones tomadas

1. El programa queda fijado como Maestría en Ingeniería de Software.
2. El tutor queda fijado como Luis Roberto Pérez Rios, Ph.D.
3. El trabajo se gestionará en archivos Markdown dentro del directorio `tesis_ds/`.
4. La idea inicial se tratará como una intuición de Design Science que aún debe delimitarse; no se acepta todavía como problema de investigación.

## Pendientes inmediatos

1. Precisar si existe una fecha tentativa de defensa.
2. Iniciar E1 con la identificación del área de experiencia mayor y la disponibilidad real del contexto PRX.

## Riesgos iniciales

- Existe riesgo de confundir una mejora organizacional o consultoría de procesos con una tesis de Design Science. Para evitarlo, la investigación deberá distinguir el problema de diseño del problema de investigación, que en el formato institucional se registrará como problema científico.
- Existe riesgo de usar CMMI como etiqueta diagnóstica sin evidencia suficiente o sin adecuación al tamaño y madurez de una empresa pequeña. Esta afirmación deberá verificarse antes de incorporarse al perfil.
- Existe riesgo de sobrealcance si se pretende llevar una empresa de nivel inicial a nivel 2 en un mes. El alcance debe calibrarse al tiempo disponible y a la evidencia evaluable.


## Registro de avance 2026-09-22

Se cerró E0 con fecha de entrega del perfil fijada para el 2026-09-28. Dado que el plazo es de seis días calendario, el alcance inicial debe concentrarse en producir un perfil de investigación defendible y no en prometer resultados de implementación o evaluación que todavía no existen.


## Registro E1 2026-09-22

Se identificó como área de experiencia mayor el desarrollo de software empresarial, con énfasis en backend, integración, arquitectura, DevOps, calidad y gestión técnica. Se generó una primera lista de temas candidatos en 	esis_ds/01_areas_y_temas.md. E1 queda abierta hasta que el tesista seleccione uno o dos temas y se confirme el acceso real al contexto PRX.



## Registro E1 2026-09-22 - cierre

Se corrigió el contexto de PRC a PRX. Se cerró E1 con el tema base: marco ligero de adopción inicial de prácticas de Ingeniería de Software para microempresas y empresas emergentes. PRX cuenta con aproximadamente siete desarrolladores distribuidos en dos equipos, uno WordPress y otro de software a medida. El tesista tiene autorización para entrevistas y revisión de repositorios y documentos. Se avanza a E2 para delimitar problema de diseño, problema de investigación —que en el formato institucional se registrará como problema científico—, objeto de estudio, campo de acción y propuesta.


## Registro E2 2026-09-22

Se registraron insumos iniciales de delimitación: PRX desarrolla sistemas para clientes, sitios web, Odoo y aplicaciones empresariales; usa Odoo para tareas, pero su adopción es irregular; existen evidencias preliminares de mala gestión técnica en errores de producción, conflictos de repositorios, proyectos sin repositorio, uso irregular de Git, retrasos sin visibilidad y desconocimiento de asignaciones. Se identificaron prácticas candidatas, pero todavía deben priorizarse para evitar sobrealcance.


## Registro E2 2026-09-22 - delimitación de contexto

Se decidió delimitar la aplicación inicial y evaluación del marco a la línea de software a medida de PRX. El marco mantendrá alcance conceptual transversal para el departamento de desarrollo, pero la evidencia empírica inicial se generará en software a medida por ser el equipo en conformación y con mayor necesidad de reglas comunes.


## Registro E2 2026-09-22 - evidencia por proyectos

Se registró evidencia preliminar en los proyectos Central, Ansular y PConst. La evidencia muestra ausencia o creación tardía de repositorios, baja calidad interna de código, falta de pruebas unitarias, cambios con defectos introducidos, problemas de lentitud y despliegues no estandarizados hacia AWS Lambda. Se decidió interpretar estos casos como síntomas de gestión técnica inicial insuficiente, no como una tesis centrada exclusivamente en refactorización o calidad de código.


## Registro E2 2026-09-22 - prácticas del marco

Se seleccionaron las prácticas de la primera versión del marco: gestión visible de tareas, convención mínima de ramas y commits, solicitudes de integración de cambios y pruebas unitarias iniciales. Se declaró como precondición que cada proyecto esté alojado en el repositorio institucional GitHub de PRX.


## Registro E2 2026-09-22 - criterios preliminares

Se aceptaron criterios preliminares para la aplicación inicial del marco: 80 % de tareas activas visibles en Odoo, 80 % de cambios con convención de ramas y commits, 70 % de cambios integrados mediante solicitudes de integración en GitHub y al menos un componente crítico por proyecto piloto con pruebas unitarias iniciales ejecutables. La evaluación se planifica con cinco desarrolladores durante dos semanas.


## Registro E2 2026-09-22 - delimitación consolidada

Se consolidaron las formulaciones de problema de diseño, problema de investigación —que en el formato institucional se registrará como problema científico—, objeto de estudio, campo de acción y propuesta. E2 queda parcialmente satisfecha; falta verificar base bibliográfica inicial antes del cierre definitivo.


## Registro E4 2026-09-22 - marco teórico preliminar

Se construyó un marco teórico preliminar en 	esis_ds/04_marco_teorico.md con fuentes verificadas: ISO/IEC 29110-1-1:2024, ISO/IEC 29110-1-2:2024, SWEBOK Guide V4.0, Scrum Guide 2020, GitHub Flow, Effective Software Testing y CMMI Model Viewer. El marco sustenta decisiones de diseño del artefacto, pero requiere una búsqueda académica adicional sobre mejora de procesos en empresas pequeñas o emergentes antes de considerarse cerrado.


## Registro E6 2026-09-22 - indicadores y criterios

Se definieron indicadores preliminares de diagnóstico en 	esis_ds/06_diagnostico.md: visibilidad de tareas, repositorio institucional, conformidad de ramas, conformidad de commits, integración mediante solicitudes de cambios, evidencia mínima de verificación, pruebas unitarias iniciales y defectos/correcciones urgentes como indicador contextual. Los criterios de éxito quedaron fijados antes de construir el artefacto, pero las líneas base numéricas deben levantarse en Odoo, GitHub, repositorios piloto y entrevistas antes de aplicar el marco.


## Registro E3 2026-09-23 - título provisional

Se aceptó como título provisional: 'Marco ligero para la adopción inicial de prácticas de Ingeniería de Software en equipos pequeños de empresas emergentes: un estudio Design Science en la línea de software a medida de PRX'. El título declara artefacto, clase de problema, clase de contexto y contexto empírico inicial.


## Registro E3 2026-09-23 - pregunta de investigación

Se aceptó la pregunta principal: '¿Qué principios de diseño debe incorporar un marco ligero de adopción inicial de prácticas de Ingeniería de Software para mejorar la visibilidad del trabajo, la trazabilidad de cambios y la verificación básica del código en equipos pequeños de empresas emergentes de software con baja formalización?'. También se añadieron subpreguntas de diagnóstico, construcción, evaluación y contribución.


## Registro E3 2026-09-23 - objetivo general

Se aceptó el objetivo general: diseñar, construir y evaluar un marco ligero de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de empresas emergentes con baja formalización, orientado a mejorar visibilidad del trabajo, trazabilidad de cambios y verificación básica del código, y derivar principios de diseño aplicables a contextos similares.


## Registro E3 2026-09-23 - objetivos específicos

Se aceptaron seis objetivos específicos: diagnóstico, fundamentación, diseño y construcción, evaluación formativa con rediseño, evaluación sumativa y derivación de principios de diseño. Los objetivos quedan alineados con la lógica de Design Science y con la contribución esperada de maestría.


## Registro E3 2026-09-23 - proposición de diseño

Se aceptó una proposición de diseño en lugar de una hipótesis causal clásica: si un marco ligero organiza prácticas mínimas en una ruta gradual, verificable y ajustada a herramientas reales, entonces puede mejorar visibilidad, trazabilidad y verificación básica porque reduce ambigüedad operativa y convierte prácticas dispersas en acuerdos técnicos observables.


## Registro E3 2026-09-23 - metodología

Se aceptó DSRM de Peffers et al. como modelo metodológico principal. Se corrigió la ambigüedad de Odoo distinguiendo el tablero interno de gestión de tareas implementado en Odoo de Odoo como plataforma de desarrollo usada en proyectos de clientes.


## Registro E3 2026-09-23 - estrategia de evaluación

Se aceptó la estrategia de evaluación del perfil: línea base previa, evaluación formativa con rediseño, evaluación sumativa inicial y análisis de amenazas a la validez. La evaluación usará el tablero interno de tareas implementado en Odoo, GitHub institucional, repositorios piloto y entrevistas breves con cinco desarrolladores.


## Registro E3 2026-09-23 - contribución reclamada

Se aceptó la contribución reclamada: principios de diseño para marcos ligeros de adopción inicial de prácticas de Ingeniería de Software en equipos pequeños con baja formalización. Se aclaró que el marco aplicado en PRX será el artefacto evaluado, pero la contribución no se limitará al documento operativo del marco.


## Registro E3 2026-09-23 - cronograma

Se aceptó un cronograma de ejecución de ocho semanas posterior al perfil. El cronograma incluye diagnóstico, diseño, construcción/formalización, evaluación formativa, rediseño, evaluación sumativa inicial, análisis y escritura, protegiendo explícitamente el tiempo de rediseño.


## Registro E3 2026-09-23 - gate de contribución

Se aceptó la oración única de contribución original: 'Esta investigación aportará principios de diseño para construir marcos ligeros de adopción inicial de prácticas de Ingeniería de Software en equipos pequeños con baja formalización, sustentados en la construcción, aplicación, rediseño y evaluación de un marco en la línea de software a medida de PRX'. E3 queda sustancialmente construido, pendiente de revisión integrada.


## Registro E3 2026-09-23 - perfil integrado y matriz

Se añadió una versión integrada del perfil DS en 	esis_ds/03_perfil_ds.md, incluyendo planteamiento del problema, objeto de estudio, campo de acción, fundamentación preliminar, selección y muestra, plan de análisis y anexo previsto del artefacto. Se actualizó 	esis_ds/matriz_coherencia.md con los eslabones ya formulados y sus pendientes reales.


## Registro 2026-09-23 - revisión profunda y bibliografía

Se realizó revisión de calidad de E0 a E6 preliminar y se creó 	esis_ds/revision_calidad_e0_e6.md. Se validó bibliografía adicional mediante DOI/Crossref: Pino et al. (2008), Laporte et al. (2018), Buchalcevova (2021), Vives et al. (2022), Hevner et al. (2004) y Peffers et al. (2007). La bibliografía específica sobre mejora de procesos en pequeñas empresas queda parcialmente resuelta para el perfil.


## Registro E3 2026-09-23 - perfil limpio

Se generó 	esis_ds/03_perfil_ds_limpio.md como versión presentable y sin duplicaciones del perfil de investigación Design Science. Incluye título, problema de diseño, problema de investigación —que en el formato institucional se registrará como problema científico—, pregunta, objeto, campo, objetivos, proposición de diseño, fundamentación, metodología DSRM, evaluación, muestra, plan de análisis, contribución, cronograma, anexo previsto, oración única de contribución y referencias APA 7.


## Registro E3 2026-09-25 - revisión final del perfil limpio

Se revisó 	esis_ds/03_perfil_ds_limpio.md contra el gate de E3 y el capítulo de perfil Design Science. Se añadió la sección de criterio de suficiencia del artefacto para declarar cuándo el marco estará listo para evaluación sumativa. Se creó 	esis_ds/revision_final_perfil_limpio.md. E3 queda cerrada para fines de perfil, pendiente solo de traducción posterior al formato institucional.


## Registro E5 2026-09-25 - estado del arte preliminar

Se creó 	esis_ds/05_estado_del_arte.md con una revisión preliminar de soluciones y artefactos existentes: ISO/IEC 29110, CMMI, Scrum, GitHub Flow, solicitudes de integración de cambios, pruebas unitarias iniciales y literatura de mejora de procesos en pequeñas organizaciones. Se formuló la brecha de novedad relativa: el aporte no es inventar prácticas, sino componerlas en un marco ligero, gradual, contextualizado y evaluable para equipos pequeños con baja formalización. E5 queda preliminarmente satisfecho para fines de perfil, ampliable en la tesis completa.


## Registro E6 2026-09-25 - plan operativo de línea base

Se fortaleció 	esis_ds/06_diagnostico.md con el plan operativo para levantar la línea base: ventana de observación, criterios para seleccionar proyectos piloto, procedimiento de recolección, reglas de codificación, control de sesgos y estado actualizado del gate. Se creó 	esis_ds/06_instrumentos_linea_base.md con fichas para tablero interno de tareas implementado en Odoo, GitHub, pruebas unitarias, entrevista breve y consolidación de indicadores. E6 queda fortalecido, pero no cerrado hasta registrar valores reales de línea base.


## Registro 2026-09-25 - verificación frente a instrucciones ALSIE

Se creó 	esis_ds/verificacion_cumplimiento_alsie.md para contrastar el avance con las instrucciones del docente. El trabajo cumple sustancialmente lo metodológico: enfoque Design Science, tema, problema de investigación —que en el formato institucional se registrará como problema científico—, objeto/campo y perfil. Quedan pendientes operativos: publicar enlace público del repositorio, crear README.md, estudiar documentos generados y elaborar plan individual explícito de desarrollo de la propuesta.


## Registro 2026-09-25 - guía de revisión y plan individual

Como el repositorio ya tiene un README.md general del kit, se creó GUIA_REVISION_ENTREGA_ALSIE.md para orientar la revisión del avance individual sin reemplazar el README existente. También se creó 	esis_ds/plan_individual_desarrollo.md con el plan desde perfil hasta predefensa interna.

