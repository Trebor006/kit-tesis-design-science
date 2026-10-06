# E7a. Alternativas de solución

## Propósito de la subetapa

Esta subetapa convierte la solución conceptual definida en la delimitación en alternativas reales de diseño del artefacto. En Design Science, el diseño no se justifica solo porque “parece conveniente”, sino porque documenta decisiones, alternativas descartadas y razones trazables al problema, a los requisitos preliminares y a la base de conocimiento. Esta regla protege la tesis contra el error de presentar una guía operativa como si fuera investigación.

El problema de diseño sigue siendo que la línea de software a medida de PRX carece de una ruta ligera, común y verificable para adoptar prácticas mínimas de gestión técnica desde el inicio de los proyectos y producir evidencia verificable del trabajo realizado. El problema de investigación —que en el formato institucional se registrará como problema científico— es la brecha sobre cómo diseñar marcos ligeros de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de desarrollo con baja estandarización.

## Criterios de comparación

Las alternativas se comparan con seis criterios. Estos criterios no miden todavía el éxito del artefacto en campo; sirven para decidir qué forma de solución es más coherente con el problema y con las restricciones de la tesis.

| Criterio | Descripción | Peso cualitativo |
|:--|:--|:--|
| Coherencia con el problema | Grado en que la alternativa responde a visibilidad del trabajo, trazabilidad de cambios, evidencia verificable y verificación básica. | Alto |
| Factibilidad en PRX | Posibilidad de aplicar la alternativa con cinco desarrolladores, herramientas existentes y tiempo limitado. | Alto |
| Ligereza de adopción | Capacidad de introducir reglas mínimas sin imponer una transformación organizacional pesada. | Alto |
| Sustento teórico y técnico | Relación con mejora de procesos en entidades pequeñas, transparencia, control de cambios, solicitudes de integración y pruebas unitarias. | Alto |
| Novedad relativa | Capacidad de producir conocimiento de diseño y no solo repetir una práctica conocida. | Medio |
| Riesgo de sobrealcance | Probabilidad de prometer más de lo que puede evaluarse en una tesis de maestría y en la ventana disponible. | Alto |

## Alternativa 1: marco mínimo de gestión técnica inicial

Esta alternativa propone un marco ligero centrado en un conjunto mínimo de prácticas técnicas y de gestión visibles: tareas registradas en un mecanismo de gestión de trabajo, repositorio oficial o excepción documentada como precondición, convención mínima de ramas y commits, solicitudes de integración de cambios y evidencia mínima de verificación, incluyendo pruebas unitarias iniciales en al menos un componente crítico por proyecto piloto. En PRX, esta alternativa se instancia con el tablero interno de gestión de tareas implementado en Odoo y repositorios GitHub.

Su fortaleza es que responde directamente a los indicadores definidos en E6 y evita ampliar el alcance hacia una transformación completa de procesos. Su debilidad es que puede parecer una lista de buenas prácticas si no se documentan con rigor la ruta de adopción, las reglas mínimas, los productos de trabajo y los principios de diseño derivados de la evaluación.

Esta alternativa se sustenta en la necesidad de adaptar prácticas de Ingeniería de Software a entidades pequeñas o muy pequeñas, evitando imponer estructuras desproporcionadas al tamaño del equipo (International Organization for Standardization & International Electrotechnical Commission, 2024a; Laporte et al., 2018). También se apoya en la transparencia, inspección y adaptación como mecanismos de gestión visible del trabajo (Schwaber & Sutherland, 2020), en el uso de flujo basado en ramas y solicitudes de integración de cambios (GitHub Docs, s. f.) y en la incorporación progresiva de pruebas unitarias como mecanismo de verificación técnica básica (Aniche, 2022).

## Alternativa 2: método operativo por flujo de trabajo

Esta alternativa define un método paso a paso desde la creación de una tarea hasta la entrega de un cambio. El método establecería entradas, salidas, responsables y criterios de entrada y salida para cada paso: registrar tarea, crear rama, realizar commits, abrir solicitud de integración, registrar evidencia de verificación, fusionar el cambio y actualizar el estado del entregable.

Su fortaleza es la claridad operacional. Un desarrollador podría seguir el método como una secuencia concreta, lo que reduce ambigüedad y facilita capacitación breve. Su debilidad es que puede quedar demasiado ligado al flujo específico de PRX y perder transferibilidad como marco de clase, especialmente si la evaluación se concentra en cumplimiento procedimental y no en principios de diseño.

Esta alternativa se aproxima más a un artefacto de tipo método. Sería válida en Design Science, pero exigiría evaluar aplicabilidad y efectividad del método como secuencia de trabajo. En el contexto actual, el riesgo es convertir el artefacto en un procedimiento interno demasiado dependiente de Odoo y GitHub, debilitando la contribución analítica para equipos similares.

## Alternativa 3: marco de adopción progresiva basado en niveles

Esta alternativa organiza la adopción en niveles. Un nivel inicial aseguraría visibilidad de tareas y repositorio institucional; un segundo nivel incorporaría convención de ramas y commits; un tercer nivel exigiría solicitudes de integración de cambios con evidencia mínima; y un cuarto nivel introduciría pruebas unitarias iniciales en componentes críticos.

Su fortaleza es que reconoce que equipos con baja estandarización no adoptan todas las prácticas de manera simultánea. La progresión por niveles puede reducir resistencia y permitir evaluación formativa de fricciones por etapa. Su debilidad es que puede requerir más tiempo de aplicación para demostrar avance entre niveles, lo cual tensiona el cronograma de la tesis.

Esta alternativa se sustenta en la lógica de mejora gradual de procesos en organizaciones pequeñas y muy pequeñas, donde la adopción debe calibrarse a la capacidad real del equipo (Pino et al., 2008; International Organization for Standardization & International Electrotechnical Commission, 2024a). También se alinea con la idea de construir capacidad antes de exigir formalización más amplia, pero debe evitar presentarse como modelo de madurez completo.

## Alternativa 4: adopción directa de un marco existente

Esta alternativa consistiría en adoptar directamente un marco existente, como ISO/IEC 29110, Scrum, GitHub Flow o prácticas de CMMI, seleccionando sus recomendaciones relevantes para PRX. Su fortaleza es que reduce incertidumbre conceptual y se apoya en cuerpos de conocimiento reconocidos.

Su debilidad es metodológicamente grave: si la tesis se limita a implantar un marco existente, la contribución de Design Science queda debilitada. Además, ISO/IEC 29110 o CMMI exceden el alcance temporal si se los interpreta como adopción formal; Scrum no resuelve por sí solo trazabilidad técnica y pruebas unitarias; GitHub Flow no cubre diagnóstico, ruta de adopción ni articulación con evidencia de entregables. Por tanto, esta alternativa funciona mejor como fuente de componentes, no como solución completa.

## Matriz de decisión

Escala: Alto = favorable para la tesis; Medio = aceptable con riesgos; Bajo = débil o riesgoso. En “riesgo de sobrealcance”, Alto significa bajo riesgo; Bajo significa riesgo alto.

| Alternativa | Coherencia con el problema | Factibilidad en PRX | Ligereza de adopción | Sustento teórico y técnico | Novedad relativa | Riesgo de sobrealcance | Evaluación global |
|:--|:--|:--|:--|:--|:--|:--|:--|
| 1. Marco mínimo de gestión técnica inicial | Alto | Alto | Alto | Alto | Medio | Alto | Fuerte, pero debe formularse como marco con principios de diseño, no como lista de prácticas. |
| 2. Método operativo por flujo de trabajo | Alto | Medio | Medio | Medio | Medio | Medio | Útil como componente operativo, pero demasiado procedimental si se adopta como artefacto principal. |
| 3. Marco de adopción progresiva basado en niveles | Alto | Medio | Alto | Alto | Alto | Medio | Conceptualmente fuerte, aunque exige controlar el tiempo de evaluación y evitar apariencia de modelo de madurez. |
| 4. Adopción directa de un marco existente | Medio | Medio | Bajo | Alto | Bajo | Bajo | Débil como tesis de Design Science; útil solo como fuente de elementos de diseño. |

## Decisión final para el hito del 5 de octubre de 2026

La alternativa seleccionada es una **composición entre la alternativa 1 y la alternativa 3**: un marco ligero de gestión técnica inicial, organizado como ruta progresiva de adopción. La alternativa 1 aporta foco, factibilidad y trazabilidad directa con los indicadores; la alternativa 3 aporta gradualidad y una lógica de adopción más defendible para equipos pequeños de desarrollo con baja estandarización.

La alternativa 2 no se descarta completamente; debe incorporarse como componente operativo del marco, porque cada práctica necesita pasos mínimos, entradas, salidas y criterios de verificación. La alternativa 4 se descarta como solución principal, pero se conserva como base de conocimiento: ISO/IEC 29110, Scrum, GitHub Flow, SWEBOK, CMMI y literatura sobre mejora de procesos en pequeñas organizaciones seguirán justificando decisiones de diseño específicas.

La decisión se formula así: **diseñar un Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización**, compuesto por precondiciones y gobernanza mínima, gestión visible del trabajo, gestión y trazabilidad del código, integración y revisión de cambios, verificación técnica básica, entrega y configuración básica, y seguimiento y mejora del marco.

El componente de integración y revisión no asumirá que la revisión independiente ya existe en PRX. La línea base muestra solicitudes de integración fusionadas, pero no una práctica institucional observable de revisión por una persona distinta del autor. Por ello, el marco deberá introducir la revisión de forma progresiva: primero solicitud trazable, luego plantilla y evidencia, después validación documentada, y finalmente revisión por tercero cuando exista disponibilidad real. En componentes de un solo desarrollador, la auto-validación documentada podrá aceptarse como excepción explícita, no como sustituto silencioso de revisión.

Esta decisión se adopta después de contrastar la línea base real: repositorios dispersos, ausencia de convención documentada, solicitudes de integración sin evidencia de verificación, tickets con granularidad excesiva y prácticas locales introducidas por el tesista que todavía no constituyen estándar institucional. Por tanto, el artefacto no será una guía de GitHub ni una capacitación operativa, sino un marco evaluable con reglas mínimas, plantillas, roles, niveles de adopción e indicadores.

## Alternativas descartadas y razón

No se adopta CMMI como solución porque excede el alcance de la tesis, no corresponde a una certificación ni puede evaluarse responsablemente en dos semanas. CMMI permanece solo como referencia conceptual para distinguir prácticas ad hoc de prácticas gestionadas.

No se adopta Scrum completo porque la tesis no busca transformar la gestión ágil del equipo ni introducir todos sus eventos, roles y artefactos. Se aprovecha su fundamento de transparencia, inspección y adaptación, pero el marco se concentra en prácticas mínimas de Ingeniería de Software.

No se adopta GitHub Flow como solución completa porque resuelve solo una parte del problema: control de cambios mediante ramas y solicitudes de integración. El problema también incluye visibilidad de tareas, evidencia de verificación, pruebas unitarias iniciales y ruta de adopción.

No se adopta GitFlow como flujo de ramificación principal porque introduce ramas permanentes y reglas de liberación más pesadas que las necesarias para la primera aplicación en Central. El marco tomará como referencia un flujo basado en tronco inspirado en *Trunk-Based Development* —desarrollo basado en tronco—, usando ramas cortas por tarea, solicitudes de integración, `squash merge` y eliminación de ramas después de fusionar.

No se adopta ISO/IEC 29110 completo porque el estudio no busca implementar una norma, sino diseñar un marco ligero sustentado en la idea de adaptar procesos a entidades pequeñas y muy pequeñas.

## Implicaciones para E7b

La alternativa seleccionada obliga a que los requisitos del artefacto cubran al menos seis propiedades:

1. Aplicabilidad por desarrolladores con experiencia desigual en Git y prácticas de verificación.
2. Trazabilidad entre tarea, rama, commit, solicitud de integración y evidencia mínima.
3. Ligereza operacional, para evitar capacitación extensa o dependencia permanente del investigador.
4. Verificabilidad mediante criterios observables en Odoo, GitHub y repositorios.
5. Gradualidad de adopción, para no exigir todas las prácticas con la misma intensidad desde el primer día.
6. Transferibilidad analítica hacia equipos pequeños de desarrollo con baja estandarización.

## Estado del gate E7a

E7a queda **cerrada para el hito del 5 de octubre de 2026**. Existen alternativas reales, trade-offs explícitos y una decisión coherente con la línea base real y con la tipología declarada del artefacto. La construcción detallada pasa a E7b, E7c y E7d.

## Referencias

Aniche, M. (2022). *Effective software testing: A developer's guide*. Manning Publications. https://www.manning.com/books/effective-software-testing

GitHub Docs. (s. f.). *GitHub flow*. Recuperado el 22 de septiembre de 2026, de https://docs.github.com/en/get-started/using-github/github-flow

International Organization for Standardization, & International Electrotechnical Commission. (2024a). *ISO/IEC 29110-1-1:2024: Systems and software engineering — Lifecycle profiles for very small entities (VSEs) — Part 1-1: Overview*. https://www.iso.org/standard/85337.html

Laporte, C. Y., Munoz, M., Mejia Miranda, J., & OConnor, R. V. (2018). Applying software engineering standards in very small entities: From startups to grownups. *IEEE Software, 35*(1), 99–103. https://doi.org/10.1109/MS.2017.4541041

Pino, F. J., García, F., & Piattini, M. (2008). Software process improvement in small and medium software enterprises: A systematic review. *Software Quality Journal, 16*(2), 237–261. https://doi.org/10.1007/s11219-007-9038-z

Schwaber, K., & Sutherland, J. (2020). *The Scrum Guide: The definitive guide to Scrum: The rules of the game*. https://scrumguides.org/scrum-guide.html
