
## Insumos iniciales para E2

El contexto de PRX no es homogéneo. La empresa desarrolla sistemas para clientes, sitios web, sistemas basados en Odoo y aplicaciones empresariales. El equipo asociado a Odoo muestra prácticas relativamente más ordenadas, porque cuenta con experiencia previa y ha impulsado el uso de tableros Kanban dentro de un Odoo interno para la gestión de tareas.

Actualmente PRX usa Odoo para registrar tareas, pero el uso todavía no está estabilizado. Algunos responsables de proyecto están siendo inducidos u obligados a registrar actividades, mientras que algunos desarrolladores continúan autogestionándose sin registrar tareas. La evidencia preliminar del problema incluye errores en producción, conflictos en repositorios, proyectos sin repositorio, desarrolladores que no usaban Git, retrasos sin visibilidad de inicio o finalización, y desconocimiento sobre en qué trabaja cada desarrollador.

El tesista propuso como prácticas iniciales candidatas: estandarizar el uso de una herramienta de gestión de tareas, estandarizar despliegues, centralizar proyectos en una cuenta institucional de repositorios Git, incorporar pruebas unitarias, automatizar la ejecución de pruebas, usar agentes para validar calidad de código y estandarizar commits. Estas prácticas son potencialmente evaluables, pero todavía están sobredimensionadas para un primer ciclo; deberán priorizarse según impacto, factibilidad y evidencia disponible.

## Nota de delimitación

Debe evitarse mezclar herramientas sin justificación. Si PRX ya usa Odoo para tareas, proponer Jira como estándar requiere explicar por qué sustituir o complementar Odoo sería necesario. En esta etapa conviene formular la práctica como “estandarización de la gestión visible de tareas” y no como adopción de una herramienta específica.

## Decisión de delimitación del contexto de aplicación

El marco se diseñará con alcance conceptual transversal para el departamento de desarrollo de PRX, que incluye líneas de trabajo diferenciadas en WordPress, Odoo y software a medida. No obstante, la aplicación inicial y la evaluación se delimitarán a la línea de **software a medida**, porque es el equipo que se está conformando recientemente y presenta mayor necesidad de reglas comunes para trabajar correctamente.

Esta decisión evita dos errores metodológicos: primero, tratar a PRX como si fuera una organización homogénea; segundo, prometer una evaluación simultánea en todas las líneas de trabajo sin evidencia suficiente. El marco podrá incluir reglas comunes para todo el departamento —gestión visible de tareas, repositorios institucionales, convenciones de ramas y commits, trazabilidad mínima y registro de incidencias—, pero su evaluación inicial se concentrará en software a medida.

## Formulación inicial del contexto del problema de diseño

PRX es una empresa pequeña que cuenta con un departamento de desarrollo de software compuesto por líneas de trabajo diferenciadas: WordPress, Odoo y software a medida. La línea de software a medida se encuentra en proceso de conformación y profesionalización, dentro de un departamento de aproximadamente siete desarrolladores. La empresa utiliza Odoo para la gestión de tareas, pero la adopción todavía es irregular: algunos responsables registran el trabajo, mientras que algunos desarrolladores continúan autogestionándose sin visibilidad suficiente para el resto del equipo.

La línea de software a medida desarrolla sistemas para clientes y aplicaciones empresariales. En este contexto se observaron problemas de gestión técnica inicial: proyectos sin repositorio institucional, uso irregular de Git, conflictos en repositorios, retrasos sin visibilidad de inicio o finalización, desconocimiento sobre las actividades de algunos desarrolladores, errores en producción, pruebas principalmente manuales, documentación escasa y despliegues manuales.

## Evidencia preliminar por proyectos de software a medida

El tesista identificó evidencia preliminar en varios proyectos de la línea de software a medida:

1. **Proyecto Central.** El desarrollo está compuesto por tres soluciones: un frontend en Angular, una API y un backend en Odoo. El tesista observó que la API y el frontend no cumplían principios de diseño como SOLID ni prácticas de código limpio. Se realizó refactorización del frontend y de la API, además de incorporar pruebas unitarias en la API.

2. **Proyecto Ansular.** El frontend consume directamente datos enviados por el backend en Odoo. Se reportaron problemas de lentitud. Durante una refactorización se introdujeron defectos que debieron corregirse con urgencia, lo que evidencia riesgo técnico asociado a cambios sin una red de pruebas o verificación suficiente.

3. **Proyecto PConst.** No existían pruebas unitarias y el despliegue hacia AWS Lambda no estaba empaquetado o automatizado de forma estable. El tesista tuvo que solicitar la creación de repositorios para obtener acceso al código, lo que evidencia que algunos proyectos no estaban institucionalizados en un repositorio Git desde el inicio.

## Interpretación para el problema de diseño

La evidencia no debe redactarse principalmente como “el código no cumplía SOLID” o “se refactorizó el proyecto”, porque eso desplaza el problema hacia calidad interna de código y convierte la tesis en una intervención técnica puntual. Para mantener la coherencia con el tema elegido, estos casos deben interpretarse como síntomas de un problema más amplio de gestión técnica inicial: ausencia de repositorios institucionales desde el inicio, falta de criterios mínimos de calidad, ausencia de pruebas unitarias en componentes críticos, cambios sin verificación suficiente, despliegues manuales o no estandarizados y baja visibilidad del estado técnico de los proyectos.

La delimitación debe concentrarse en prácticas mínimas transversales que puedan observarse antes y después de aplicar el marco. Las prácticas candidatas más consistentes con la evidencia son: repositorio institucional por proyecto, gestión visible de tareas, convención mínima de ramas y commits, lista de verificación previa a despliegue, registro de incidencias o defectos y pruebas unitarias iniciales para componentes críticos.

## Prácticas seleccionadas para la primera versión del marco

Para evitar sobrealcance, la primera versión del marco se concentrará en cuatro prácticas mínimas y una precondición:

- **Precondición:** cada proyecto de software a medida debe estar alojado en el repositorio institucional de PRX en GitHub, bajo control de la empresa y no en cuentas personales de desarrolladores.
- **Práctica 1:** gestión visible de tareas.
- **Práctica 2:** convención mínima de ramas y commits.
- **Práctica 3:** uso de solicitudes de integración de cambios, conocidas en GitHub como *pull requests*. En la tesis se describirán como solicitudes de integración de cambios, es decir, revisiones previas antes de integrar cambios a la rama principal.
- **Práctica 4:** pruebas unitarias iniciales en componentes críticos.

Estas prácticas fueron seleccionadas por su relación directa con la evidencia preliminar: proyectos sin repositorio institucional, baja visibilidad del trabajo, conflictos o uso irregular de Git, cambios introducidos sin revisión suficiente y defectos asociados a refactorizaciones sin una red mínima de pruebas.

## Solución conceptual inicial

La solución conceptual es un marco ligero de adopción inicial de prácticas de Ingeniería de Software para la línea de software a medida de PRX. El marco no buscará certificar madurez ni implantar un modelo completo de mejora de procesos. Su función será proporcionar una ruta mínima, aplicable y evaluable para que un equipo pequeño adopte prácticas comunes de gestión técnica desde el inicio de los proyectos.

El marco deberá incluir, al menos, un diagnóstico inicial de prácticas, una ruta de adopción por niveles o pasos, reglas mínimas por práctica, productos de trabajo esperados y criterios de verificación. La contribución no será que PRX use GitHub u Odoo, sino los principios de diseño que permitan construir marcos ligeros de adopción inicial para organizaciones pequeñas con baja formalización.

## Criterios de éxito preliminares

Para la aplicación inicial en la línea de software a medida de PRX se definieron criterios de éxito preliminares, fijados antes de la construcción del artefacto:

1. Al menos 80 % de las tareas activas del equipo deben estar registradas y visibles en el tablero interno de gestión de tareas implementado en Odoo durante el periodo de evaluación.
2. Al menos 80 % de los cambios de código deben seguir la convención mínima de ramas y commits definida por el marco.
3. Al menos 70 % de los cambios integrados deben pasar por solicitudes de integración de cambios en GitHub.
4. Al menos un componente crítico por proyecto piloto debe contar con pruebas unitarias iniciales ejecutables.

La evaluación inicial se planifica con cinco desarrolladores de la línea de software a medida durante dos semanas. Este periodo permite una evaluación formativa y una evaluación sumativa inicial, pero no soporta afirmaciones amplias sobre todas las microempresas de software. La contribución deberá formularse con condiciones de contorno estrictas: equipos pequeños, baja formalización, adopción inicial de prácticas y contexto organizacional similar al de PRX.

## Formulación preliminar del problema de diseño

En la línea de software a medida de PRX, un equipo pequeño de aproximadamente cinco desarrolladores participantes desarrolla sistemas para clientes y aplicaciones empresariales en un contexto de profesionalización reciente. Aunque la empresa utiliza Odoo para la gestión de tareas y GitHub como repositorio institucional, la adopción de prácticas mínimas no está estabilizada: existen tareas no visibles, uso irregular de Git, proyectos con repositorios creados tardíamente, ausencia de solicitudes de integración de cambios, pruebas unitarias escasas y defectos introducidos durante refactorizaciones que debieron corregirse con urgencia.

El problema práctico consiste en que el equipo carece de una ruta ligera y común para adoptar prácticas mínimas de gestión técnica desde el inicio de los proyectos. Esta carencia reduce la visibilidad del trabajo, dificulta la coordinación, incrementa el riesgo de cambios no verificados y limita la institucionalización del conocimiento técnico. La solución conceptual es un marco ligero de adopción inicial de prácticas de Ingeniería de Software que defina precondiciones, prácticas mínimas, productos de trabajo, criterios de verificación y una ruta de adopción aplicable a equipos pequeños con baja formalización.

# Delimitación consolidada

## Distinción conceptual

En este estudio se distinguen cinco elementos que no deben confundirse. El **problema de diseño** expresa qué situación práctica debe mejorarse mediante un artefacto. El **problema de investigación**, que en el formato institucional se registrará como **problema científico**, expresa qué brecha de conocimiento se abordará al construir y evaluar ese artefacto. El **objeto de estudio**, bajo Design Science, no es la empresa PRX ni su proceso actual, sino el artefacto propuesto con su tipología declarada. El **campo de acción** delimita el espacio temático, organizacional y temporal donde el artefacto será construido, aplicado y evaluado. La **propuesta** describe el artefacto que se construirá y la contribución esperada a nivel de maestría.

## Problema de diseño

En la línea de software a medida de PRX, un equipo pequeño de desarrollo construye sistemas para clientes, aplicaciones empresariales y soluciones integradas con tecnologías como Angular, APIs y Odoo. Aunque la empresa utiliza Odoo para la gestión de tareas y GitHub como repositorio institucional, la adopción de prácticas mínimas de gestión técnica todavía no está estabilizada. Existen tareas no visibles, uso irregular de Git, repositorios creados tardíamente, ausencia de solicitudes de integración de cambios, pruebas unitarias escasas y cambios que introducen defectos que deben corregirse con urgencia.

El problema práctico consiste en que el equipo carece de una ruta ligera, común y verificable para adoptar prácticas mínimas de Ingeniería de Software desde el inicio de los proyectos. Esta carencia reduce la visibilidad del trabajo, dificulta la coordinación técnica, debilita la trazabilidad de cambios, aumenta el riesgo de defectos no detectados y limita la institucionalización del conocimiento técnico. La solución conceptual es un marco ligero que indique qué prácticas mínimas adoptar primero, cómo aplicarlas y cómo verificar su cumplimiento sin imponer la carga de un modelo de mejora de procesos completo.

Los criterios preliminares de éxito, fijados antes de la construcción del artefacto, son: al menos 80 % de las tareas activas registradas y visibles en el tablero interno de gestión de tareas implementado en Odoo; al menos 80 % de los cambios de código conformes con una convención mínima de ramas y commits; al menos 70 % de los cambios integrados mediante solicitudes de integración de cambios en GitHub; y al menos un componente crítico por proyecto piloto con pruebas unitarias iniciales ejecutables.

## Problema de investigación

El **problema de investigación**, que en el formato institucional se registrará como **problema científico**, se formula como una brecha entre los modelos generales de mejora de procesos de software y las necesidades de adopción inicial de equipos pequeños con baja formalización. Existen modelos, marcos y prácticas de mejora de procesos que orientan la madurez organizacional, pero su adopción puede resultar pesada o poco operativa para empresas emergentes pequeñas que necesitan comenzar con prácticas mínimas, visibles y verificables antes de aspirar a una mejora de procesos más amplia.

La brecha que aborda este estudio es la falta de evidencia situada sobre cómo diseñar un marco ligero de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de empresas emergentes de software, de modo que el marco sea suficientemente simple para aplicarse en contextos de baja formalización y suficientemente estructurado para mejorar la visibilidad del trabajo, la trazabilidad de cambios y la verificación básica del código. La investigación no busca demostrar que PRX “sube de nivel CMMI”, sino generar conocimiento transferible sobre el diseño de marcos ligeros para esta clase de equipos.

## Objeto de estudio

En Design Science, el objeto de estudio se resignifica: no es PRX, no es el departamento de desarrollo y no es el proceso actual observado. El objeto de estudio es el **marco ligero de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de empresas emergentes de software**.

La tipología principal del artefacto es **marco**, porque integrará constructos, prácticas, reglas de aplicación, productos de trabajo y criterios de verificación. También contiene un componente metodológico, porque propondrá una ruta de adopción por pasos. Su estructura preliminar incluye: diagnóstico inicial de prácticas, precondición de repositorio institucional en GitHub, ruta de adopción, reglas mínimas para tareas visibles, ramas y commits, solicitudes de integración de cambios, pruebas unitarias iniciales y criterios de verificación.

## Campo de acción

El campo de acción se delimita a la adopción inicial de prácticas mínimas de Ingeniería de Software en equipos pequeños de empresas emergentes de software con baja formalización de gestión técnica. El contexto empírico inicial será la línea de software a medida de PRX, dentro de un departamento de desarrollo que también incluye líneas de WordPress y Odoo. La aplicación y evaluación inicial se concentrarán en cinco desarrolladores de la línea de software a medida durante un periodo de dos semanas.

La delimitación excluye la certificación formal de madurez, la implantación completa de CMMI, la transformación integral de todos los procesos organizacionales y la automatización avanzada mediante agentes de calidad de código. Esas dimensiones pueden aparecer como antecedentes, restricciones o trabajo futuro, pero no forman parte del núcleo evaluable de la tesis.

## Propuesta

La propuesta consiste en construir y evaluar un marco ligero de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de empresas emergentes de software. El marco tendrá como precondición que todo proyecto piloto esté alojado en el GitHub institucional de la organización y se concentrará en cuatro prácticas mínimas: gestión visible de tareas, convención de ramas y commits, solicitudes de integración de cambios y pruebas unitarias iniciales en componentes críticos.

La evaluación prevista tendrá un ciclo formativo y un ciclo sumativo inicial dentro del periodo disponible. El ciclo formativo permitirá observar fricciones de aplicación y rediseñar el marco; el ciclo sumativo inicial permitirá contrastar los criterios preliminares de éxito. La contribución esperada de maestría no será el marco como documento operativo aislado, sino los principios de diseño que se deriven de su construcción y evaluación para orientar marcos ligeros similares en equipos pequeños con baja formalización.

## Estado del gate E2

E2 queda parcialmente satisfecha. El problema de diseño, el problema de investigación —que en el formato institucional se registrará como problema científico—, el objeto de estudio, el campo de acción y la propuesta ya cuentan con una formulación coherente. Falta verificar la base bibliográfica inicial sobre mejora de procesos de software, modelos de madurez y adopción de prácticas en empresas pequeñas antes de cerrar definitivamente la etapa.

