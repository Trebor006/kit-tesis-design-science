# E5. Estado del arte: soluciones y artefactos existentes

## Propósito de la revisión

Esta revisión no describe el fenómeno general de la baja formalización en PRX. Su función en Design Science es comparar soluciones, marcos, normas y prácticas existentes que abordan la misma clase de problema: adopción inicial de prácticas de Ingeniería de Software en equipos pequeños con baja formalización. El resultado debe justificar por qué el artefacto propuesto —un marco ligero— no duplica una solución existente y qué limitaciones debe superar en el contexto de PRX.

La pregunta de revisión es: ¿qué soluciones o artefactos existentes orientan la adopción inicial de prácticas de Ingeniería de Software en equipos pequeños, qué ofrecen, cómo se limitan para el contexto de PRX y qué implicaciones tienen para el diseño del marco propuesto?

## Alcance y criterios de inclusión

Se incluyeron fuentes verificadas que cumplen al menos uno de estos criterios: a) proponen normas o marcos para entidades pequeñas o muy pequeñas; b) ofrecen prácticas operativas ligeras para visibilidad del trabajo, control de cambios, revisión de cambios o verificación básica; c) sirven como antecedente de mejora de capacidades; d) aportan evidencia académica sobre mejora de procesos en pequeñas organizaciones de software. Se excluyeron herramientas o metodologías que exigirían una transformación organizacional completa, certificación formal o adopción de prácticas que no pueden evaluarse en el periodo previsto.

La revisión se apoya en fuentes normativas, documentación oficial, libros técnicos y artículos académicos verificados. No se presentan referencias no verificadas como si estuvieran confirmadas. Cuando una fuente es un antecedente conceptual, no se la convierte en criterio de éxito; esta regla es especialmente importante para CMMI.

## Matriz de soluciones y artefactos existentes

| Solución o artefacto existente | Qué ofrece | Limitación para esta tesis | Implicación para el marco propuesto |
|:--|:--|:--|:--|
| ISO/IEC 29110 para entidades muy pequeñas | Conceptos, perfiles y justificación para adaptar procesos a entidades muy pequeñas (ISO & IEC, 2024). | Es una norma amplia; no entrega directamente una ruta operativa mínima ajustada a las herramientas concretas de PRX. | Usarla como anclaje principal para justificar ligereza, gradualidad y adecuación al tamaño del equipo. |
| CMMI | Referencia conceptual de mejora de capacidades y madurez organizacional mediante áreas de práctica y vistas del modelo (CMMI Institute, s. f.). | Su uso formal exige alcance, interpretación y evaluación que exceden el perfil; no debe usarse para prometer subida de nivel. | Mantenerlo como antecedente conceptual, no como objetivo, instrumento de evaluación ni criterio de éxito. |
| Scrum | Marco ligero basado en transparencia, inspección y adaptación; define artefactos y eventos que favorecen visibilidad del trabajo (Schwaber & Sutherland, 2020). | Implantar Scrum completo no es el objetivo ni sería evaluable en dos semanas; PRX ya tiene una forma de gestión interna que no debe sustituirse sin evidencia. | Tomar los principios de transparencia, inspección y adaptación para justificar tareas visibles y revisión periódica, sin declarar adopción Scrum. |
| GitHub Flow | Flujo ligero de trabajo con ramas, commits y solicitudes de integración de cambios sobre GitHub (GitHub Docs, s. f.-a). | No cubre por sí solo gestión visible de tareas ni adopción de pruebas unitarias; presupone disciplina mínima del equipo. | Usarlo como base operativa para reglas mínimas de ramas, commits y solicitudes de integración. |
| Solicitudes de integración de cambios de GitHub | Mecanismo de colaboración para proponer, revisar y fusionar cambios, con conversación, commits, verificaciones y diferencias de archivos (GitHub Docs, s. f.-b). | La herramienta no garantiza revisión útil ni evidencia de verificación; puede usarse de forma superficial. | Definir evidencia mínima obligatoria dentro de cada solicitud: descripción del cambio, referencia a tarea, verificación realizada y resultado. |
| Pruebas unitarias iniciales | Práctica de verificación técnica para componentes específicos; ayuda a detectar defectos y sostener cambios con menor riesgo (Aniche, 2022). | Exigir cobertura amplia desde el inicio puede ser inviable y conducir a cumplimiento cosmético. | Limitar la primera adopción a al menos un componente crítico por proyecto piloto con pruebas unitarias ejecutables. |
| Mejora de procesos en pequeñas y medianas empresas | La literatura muestra que la mejora de procesos en organizaciones pequeñas requiere adaptación a recursos, tamaño y restricciones reales (Pino et al., 2008). | La revisión sistemática no entrega directamente un marco listo para PRX; además, debe complementarse con evidencia actual y contextual. | Justificar que el artefacto no sea una implantación pesada, sino un marco adaptado y evaluable en un equipo pequeño. |
| Estándares en entidades muy pequeñas desde empresas emergentes | Se reconoce la utilidad de estándares de Ingeniería de Software para trayectorias desde empresas emergentes hacia organizaciones más maduras (Laporte et al., 2018). | La trayectoria de maduración no equivale a demostrar madurez formal ni certificación en esta tesis. | Plantear el marco como paso inicial de profesionalización técnica, no como programa completo de madurez. |
| Refuerzo de calidad y pruebas en ISO/IEC 29110 | La literatura evidencia que el perfil básico puede requerir refuerzos en calidad y pruebas (Buchalcevova, 2021). | El estudio no resuelve toda la gestión de calidad de PRX; solo introduce verificación básica. | Mantener pruebas unitarias iniciales como práctica explícita del marco. |

## Brecha identificada

Las soluciones existentes ofrecen piezas relevantes, pero no resuelven completamente la clase de problema formulada para esta tesis. ISO/IEC 29110 aporta el marco normativo más cercano a entidades muy pequeñas, pero no define una ruta mínima ajustada a las herramientas reales de PRX. CMMI ayuda a comprender mejora de capacidades, aunque su adopción formal excede el alcance del estudio. Scrum ofrece principios útiles de transparencia e inspección, pero implantar Scrum completo cambiaría el objeto de investigación. GitHub Flow y las solicitudes de integración de cambios proporcionan mecanismos operativos para trazabilidad y revisión, aunque no aseguran por sí mismos gestión visible ni verificación técnica suficiente.

La brecha, por tanto, no es que falten normas, marcos o herramientas. La brecha es que un equipo pequeño con baja formalización necesita una composición ligera, gradual y verificable de prácticas iniciales, conectada con sus herramientas reales y evaluable mediante criterios previos. En términos de investigación, el problema de investigación —que en el formato institucional se registrará como problema científico— es cómo diseñar principios para marcos ligeros de adopción inicial que integren esas piezas sin convertirse en una implantación pesada de madurez o en una simple lista de buenas prácticas.

## Novedad relativa del artefacto propuesto

El marco propuesto no será novedoso porque invente prácticas desconocidas. Esa sería una afirmación falsa. Su novedad relativa estará en la composición y adaptación de prácticas existentes para una clase específica de contexto: equipos pequeños de empresas emergentes de software con baja formalización, repositorio institucional en GitHub y una herramienta interna de gestión de tareas ya disponible.

La contribución esperada no es “usar GitHub”, “hacer tareas visibles” o “agregar pruebas unitarias”. La contribución será formular y evaluar principios de diseño sobre cómo ordenar esas prácticas, con qué precondiciones, con qué mínima evidencia verificable y con qué condiciones de contorno. Esta distinción protege el estudio de convertirse en consultoría operativa para PRX.

## Criterios de superioridad que deberá demostrar la evaluación

La evaluación no debe demostrar que el marco es mejor que ISO/IEC 29110, CMMI, Scrum o GitHub Flow. Esa comparación sería metodológicamente incorrecta, porque esas soluciones tienen alcance y propósito distintos. Lo que debe demostrar es que el marco propuesto mejora la situación inicial del contexto evaluado respecto a criterios previamente definidos.

Los criterios de superioridad contextual serán: mayor proporción de tareas activas visibles, mayor conformidad de ramas y commits con una convención mínima, mayor proporción de cambios integrados mediante solicitudes de integración, mayor presencia de evidencia mínima de verificación y existencia de pruebas unitarias ejecutables en componentes críticos. Estos criterios ya fueron fijados antes de la construcción para evitar evaluación a posteriori.

## Gate de E5

E5 queda preliminarmente satisfecho para fines del perfil porque ya se puede responder por qué las soluciones existentes son insuficientes para el problema de PRX y qué aportará el marco propuesto: una composición ligera, contextualizada y evaluable de prácticas iniciales. No obstante, para la tesis completa deberá ampliarse esta revisión con una búsqueda sistemática más exhaustiva en bases académicas y, si el tiempo lo permite, con análisis de marcos ligeros adicionales usados en empresas pequeñas.

## Referencias

Aniche, M. (2022). *Effective software testing: A developer's guide*. Manning Publications. https://www.manning.com/books/effective-software-testing

Buchalcevova, A. (2021). Towards higher software quality in very small entities: ISO/IEC 29110 software basic profile mapping to testing standards. *International Journal of Information Technologies and Systems Approach, 14*(1), 79–96. https://doi.org/10.4018/IJITSA.2021010105

CMMI Institute. (s. f.). *CMMI Model Viewer*. ISACA. Recuperado el 22 de septiembre de 2026, de https://cmmiinstitute.com/cmmi/model-viewer/

GitHub Docs. (s. f.-a). *GitHub flow*. Recuperado el 22 de septiembre de 2026, de https://docs.github.com/en/get-started/using-github/github-flow

GitHub Docs. (s. f.-b). *Pull requests*. Recuperado el 25 de septiembre de 2026, de https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests

International Organization for Standardization, & International Electrotechnical Commission. (2024). *ISO/IEC 29110-1-1:2024: Systems and software engineering — Lifecycle profiles for very small entities (VSEs) — Part 1-1: Overview*. https://www.iso.org/standard/85337.html

Laporte, C. Y., Munoz, M., Mejia Miranda, J., & OConnor, R. V. (2018). Applying software engineering standards in very small entities: From startups to grownups. *IEEE Software, 35*(1), 99–103. https://doi.org/10.1109/MS.2017.4541041

Pino, F. J., García, F., & Piattini, M. (2008). Software process improvement in small and medium software enterprises: A systematic review. *Software Quality Journal, 16*(2), 237–261. https://doi.org/10.1007/s11219-007-9038-z

Schwaber, K., & Sutherland, J. (2020). *The Scrum Guide: The definitive guide to Scrum: The rules of the game*. https://scrumguides.org/scrum-guide.html
