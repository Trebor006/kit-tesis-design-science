# E4. Marco teórico: sustentación del objeto de estudio

## Alcance y estado de verificación

Este marco teórico sustenta el objeto de estudio definido en la delimitación: el **marco ligero de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de empresas emergentes de software**. La búsqueda inicial se orientó a fuentes primarias, normas y documentación técnica verificable sobre entidades muy pequeñas, mejora de procesos, conocimiento aceptado en Ingeniería de Software, gestión visible del trabajo, control de cambios, solicitudes de integración de cambios y pruebas unitarias.

Las búsquedas web generales ejecutadas durante esta etapa fueron canceladas por la herramienta disponible; por ello, se usaron fuentes verificadas mediante acceso directo a sitios oficiales o editoriales. No se incluyen referencias no verificadas como si estuvieran confirmadas. Las fuentes verificadas en esta iteración son ISO/IEC 29110-1-1:2024, ISO/IEC 29110-1-2:2024, SWEBOK Guide V4.0, Scrum Guide 2020, documentación oficial de GitHub Flow, *Effective Software Testing* y la página oficial del CMMI Model Viewer.

## Pregunta de búsqueda teórica

La pregunta de búsqueda teórica fue: ¿qué cuerpos de conocimiento sustentan el diseño de un marco ligero de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños con baja formalización, y cómo se traducen en decisiones concretas de diseño del artefacto?

Se incluyeron fuentes que cumplen al menos uno de estos criterios: a) definen o justifican procesos para entidades muy pequeñas; b) sintetizan conocimiento aceptado de Ingeniería de Software; c) sustentan prácticas de transparencia, inspección y adaptación; d) fundamentan el uso de ramas, commits y solicitudes de integración de cambios; e) justifican la incorporación inicial de pruebas unitarias. Se excluyeron fuentes que solo describen herramientas sin conexión con una decisión de diseño del marco, fuentes no verificables y referencias sobre certificación CMMI que no aportan directamente a una adopción ligera y evaluable.

## Fundamentos para el diseño del marco

### Mejora de procesos para entidades muy pequeñas

La serie ISO/IEC 29110 es el anclaje más directo para el contexto de PRX, porque fue concebida para entidades muy pequeñas y no para organizaciones grandes con estructuras maduras. La versión ISO/IEC 29110-1-1:2024 establece los conceptos mayores de la serie, las características y requisitos de una entidad muy pequeña, y la razón de perfiles, documentos y guías específicos para este tipo de organizaciones (International Organization for Standardization [ISO] & International Electrotechnical Commission [IEC], 2024a). Esta fuente justifica que el artefacto no adopte un modelo pesado de mejora de procesos, sino una versión mínima, situada y gradual.

La decisión de diseñar un marco ligero, con prácticas iniciales y criterios de verificación, deriva de esta lógica: una entidad pequeña requiere perfiles y guías adaptados a su capacidad real de adopción, no una traslación completa de marcos organizacionales complejos. Para PRX, esto implica que el marco debe limitarse a prácticas de alto impacto y baja fricción inicial: tareas visibles, repositorio institucional, ramas y commits, solicitudes de integración de cambios y pruebas unitarias en componentes críticos. Si el marco exigiera una implantación completa de madurez organizacional, dejaría de ser coherente con el tipo de entidad que pretende apoyar.

### Conocimiento generalmente aceptado en Ingeniería de Software

SWEBOK Guide V4.0 proporciona una referencia amplia y actual del cuerpo de conocimiento de Ingeniería de Software. Su valor para esta tesis no está en usarlo como lista enciclopédica, sino en ubicar el artefacto dentro de áreas reconocidas: gestión de configuración, proceso de software, gestión de Ingeniería de Software, pruebas, calidad y operaciones (Washizaki, 2024). Esta fuente impide que el marco se reduzca a preferencias personales del tesista; las prácticas seleccionadas deben corresponder a áreas disciplinarias reconocidas.

La relación con el diseño es concreta. La precondición de repositorio institucional se sustenta en gestión de configuración; la gestión visible de tareas se relaciona con gestión de Ingeniería de Software; las solicitudes de integración de cambios se apoyan en control de cambios y revisión; y las pruebas unitarias pertenecen al área de pruebas y calidad. Por tanto, el marco debe mostrar trazabilidad entre cada práctica y un área aceptada de la disciplina, evitando una fundamentación decorativa.

### Transparencia, inspección y adaptación como principios de gestión visible

La Scrum Guide define Scrum como un marco ligero para generar valor mediante soluciones adaptativas a problemas complejos, basado en empirismo y pensamiento lean. Sus pilares de transparencia, inspección y adaptación son particularmente relevantes para equipos pequeños que hoy gestionan trabajo parcialmente invisible (Schwaber & Sutherland, 2020). Aunque la tesis no implantará Scrum completo, sí puede usar estos principios para fundamentar la decisión de hacer visible el trabajo en Odoo.

La decisión de diseño no es “usar Scrum”, porque eso sería una afirmación metodológica más amplia que la evidencia prevista. La decisión es más acotada: toda práctica del marco debe aumentar la transparencia operacional del equipo y permitir inspección frecuente. En PRX, esto se traduce en exigir que las tareas activas estén registradas y visibles, que los cambios relevantes puedan rastrearse en GitHub y que las pruebas unitarias proporcionen una señal mínima antes de integrar cambios.

### Flujo de cambios basado en ramas y solicitudes de integración

La documentación oficial de GitHub Flow describe un flujo ligero basado en ramas, cambios confirmados mediante commits, solicitudes de integración de cambios y revisión antes de fusionar hacia la rama principal (GitHub Docs, s. f.). Esta fuente es pertinente porque PRX usa GitHub como repositorio institucional, y el marco propuesto no necesita introducir una herramienta adicional para controlar cambios. El diseño debe aprovechar la infraestructura existente para reducir fricción de adopción.

De esta fuente se derivan varias decisiones de diseño. Primero, cada proyecto piloto debe estar en el GitHub institucional de PRX antes de aplicar el marco. Segundo, cada cambio no trivial debe ocurrir en una rama con nombre descriptivo. Tercero, la integración a la rama principal debe realizarse mediante solicitud de integración de cambios, con una descripción mínima del problema resuelto y evidencia de verificación. Estas reglas son simples, pero convierten el trabajo individual en trabajo inspeccionable por el equipo.

### Pruebas unitarias iniciales y verificación mínima

Aniche (2022) sostiene una aproximación sistemática a las pruebas de software, con énfasis en diseñar pruebas que tengan mayor probabilidad de encontrar defectos, usar métricas de cobertura con criterio y distinguir entre pruebas unitarias, de integración y de sistema. Esta fuente sustenta la decisión de no exigir una estrategia completa de pruebas en la primera versión del marco. Para un equipo con baja formalización, la adopción inicial debe comenzar por pruebas unitarias en componentes críticos, no por una pirámide completa de pruebas imposible de sostener en dos semanas.

La implicación de diseño es que el marco debe incluir una regla mínima de selección de componentes críticos. Un componente será crítico si concentra lógica de negocio, transforma datos relevantes, participa en integraciones con Odoo o ha sido fuente reciente de defectos. La métrica inicial no será cobertura total, sino existencia de pruebas unitarias ejecutables en al menos un componente crítico por proyecto piloto. Esta decisión es deliberadamente modesta, porque busca generar una práctica sostenible antes que un indicador cosmético.

### Modelos de madurez y riesgo de sobrealcance

La página oficial del CMMI Model Viewer muestra que CMMI ofrece áreas de práctica, prácticas, materiales suplementarios y vistas personalizables del modelo para adopción según necesidades y objetivos de negocio (CMMI Institute, s. f.). Esta fuente confirma que CMMI puede servir como referencia conceptual de mejora de capacidades, pero no justifica prometer una subida de nivel de madurez en esta tesis. El acceso completo al contenido del modelo requiere suscripción, por lo que cualquier uso detallado de prácticas específicas deberá verificarse posteriormente contra el material oficial disponible para el tesista.

La decisión de diseño es usar CMMI solo como antecedente de mejora de procesos, no como núcleo evaluativo. El marco no medirá si PRX alcanza un nivel CMMI, ni afirmará equivalencias de madurez. Su evaluación se limitará a criterios observables: tareas visibles, conformidad de ramas y commits, uso de solicitudes de integración de cambios y pruebas unitarias iniciales. Esta restricción protege la tesis de un sobrealcance metodológico.

## Trazabilidad entre teoría y decisiones de diseño

| Decisión de diseño del marco | Fuente que la sustenta | Implicación concreta para el artefacto |
|:--|:--|:--|
| Diseñar un marco ligero y gradual, no un modelo completo de madurez | ISO/IEC 29110-1-1:2024 | El artefacto se estructura como ruta mínima de adopción para equipos pequeños. |
| Declarar prácticas pertenecientes a áreas reconocidas de Ingeniería de Software | SWEBOK Guide V4.0 | Cada práctica se vincula con gestión de configuración, proceso, gestión, pruebas o calidad. |
| Hacer visible el trabajo activo | Scrum Guide 2020 | Las tareas deben registrarse en Odoo y ser inspeccionables por el equipo. |
| Exigir repositorio institucional, ramas, commits y solicitudes de integración de cambios | GitHub Flow | Todo cambio relevante debe ser trazable y revisable en GitHub. |
| Incorporar pruebas unitarias iniciales en componentes críticos | Aniche (2022) | La adopción inicial se limita a pruebas ejecutables en componentes de alto riesgo. |
| No prometer certificación ni subida de nivel CMMI | CMMI Model Viewer | CMMI queda como antecedente, no como criterio de evaluación de la tesis. |

## Prueba de eliminación

Este marco teórico pasa parcialmente la prueba de eliminación. Si se eliminan ISO/IEC 29110 y SWEBOK, el artefacto perdería su justificación como marco ligero para entidades pequeñas y su conexión con áreas reconocidas de Ingeniería de Software. Si se elimina Scrum Guide, la decisión de exigir visibilidad de tareas quedaría como preferencia local y no como principio de transparencia e inspección. Si se elimina GitHub Flow, las reglas de ramas, commits y solicitudes de integración quedarían sin fundamento operativo alineado con la herramienta real de PRX. Si se elimina Aniche (2022), la decisión de comenzar con pruebas unitarias en componentes críticos quedaría menos defendida.

La búsqueda académica adicional sobre mejora de procesos en pequeñas organizaciones fue reforzada con Pino et al. (2008), Laporte et al. (2018), Buchalcevova (2021) y Vives et al. (2022). Para el perfil, el marco teórico es suficiente; para la tesis completa conviene ampliar la revisión sistemática y separar con mayor detalle la base teórica del estado del arte de soluciones existentes.

## Referencias

Aniche, M. (2022). *Effective software testing: A developer's guide*. Manning Publications. https://www.manning.com/books/effective-software-testing

CMMI Institute. (s. f.). *CMMI Model Viewer*. ISACA. Recuperado el 22 de septiembre de 2026, de https://cmmiinstitute.com/cmmi/model-viewer/

GitHub Docs. (s. f.). *GitHub flow*. Recuperado el 22 de septiembre de 2026, de https://docs.github.com/en/get-started/using-github/github-flow

International Organization for Standardization, & International Electrotechnical Commission. (2024a). *ISO/IEC 29110-1-1:2024: Systems and software engineering — Lifecycle profiles for very small entities (VSEs) — Part 1-1: Overview*. https://www.iso.org/standard/85337.html

International Organization for Standardization, & International Electrotechnical Commission. (2024b). *ISO/IEC 29110-1-2:2024: Systems and software engineering — Lifecycle profiles for Very Small Entities (VSEs) — Part 1-2: Vocabulary*. https://www.iso.org/standard/85338.html

Schwaber, K., & Sutherland, J. (2020). *The Scrum Guide: The definitive guide to Scrum: The rules of the game*. https://scrumguides.org/scrum-guide.html

Washizaki, H. (Ed.). (2024). *Guide to the Software Engineering Body of Knowledge (SWEBOK Guide), Version 4.0*. IEEE Computer Society. https://www.computer.org/education/bodies-of-knowledge/software-engineering

## Refuerzo bibliográfico validado sobre mejora de procesos en organizaciones pequeñas

La revisión adicional permitió verificar literatura académica específica sobre mejora de procesos en pequeñas y medianas empresas de software, entidades muy pequeñas y adopción de estándares ligeros. Pino et al. (2008) realizaron una revisión sistemática sobre mejora de procesos de software en pequeñas y medianas empresas, y su trabajo confirma que esta clase de organizaciones requiere enfoques ajustados a su tamaño, recursos y restricciones. Aunque no es una fuente reciente, se mantiene como fuente primaria relevante porque aborda directamente la clase de problema de la tesis.

Laporte et al. (2018) conectan la aplicación de estándares de Ingeniería de Software en entidades muy pequeñas con el recorrido desde empresas emergentes hasta organizaciones más maduras. Esta fuente fortalece la decisión de no plantear una implantación pesada desde el inicio, sino una ruta de adopción progresiva. Buchalcevova (2021) muestra, además, que incluso el perfil básico de ISO/IEC 29110 puede requerir refuerzos específicos en calidad y pruebas; esto respalda que el marco propuesto incluya pruebas unitarias iniciales como práctica explícita y no como una consecuencia informal de la mejora de procesos.

Vives et al. (2022) realizaron un mapeo sistemático sobre ISO/IEC 29110 y educación en Ingeniería de Software. Aunque su foco principal es educativo, el estudio confirma la vigencia investigativa de ISO/IEC 29110 y muestra que el perfil básico y sus procesos continúan siendo objeto de análisis. Para esta tesis, la fuente no sustituye la evidencia de campo en PRX, pero sí ayuda a justificar que ISO/IEC 29110 sigue siendo un referente activo cuando se trabaja con entidades muy pequeñas.

Este refuerzo mejora la sustentación del problema de investigación, que en el formato institucional se registrará como problema científico: la literatura ofrece modelos y estándares para entidades pequeñas, pero el estudio se concentra en el diseño y evaluación de un marco ligero de adopción inicial, ajustado a herramientas reales y a prácticas mínimas observables en un equipo pequeño con baja formalización.

## Fuentes metodológicas de Design Science verificadas

Para el perfil se verificaron dos fuentes metodológicas centrales. Hevner et al. (2004) fundamentan la investigación Design Science como creación y evaluación rigurosa de artefactos para extender capacidades humanas u organizacionales. Peffers et al. (2007) proponen DSRM como metodología de investigación para sistemas de información, con actividades de identificación del problema, objetivos de solución, diseño y desarrollo, demostración, evaluación y comunicación. Estas fuentes sustentan el diseño metodológico declarado en el perfil.

Buchalcevova, A. (2021). Towards higher software quality in very small entities: ISO/IEC 29110 software basic profile mapping to testing standards. *International Journal of Information Technologies and Systems Approach, 14*(1), 79–96. https://doi.org/10.4018/IJITSA.2021010105

Hevner, A. R., March, S. T., Park, J., & Ram, S. (2004). Design science in information systems research. *MIS Quarterly, 28*(1), 75–106. https://doi.org/10.2307/25148625

Laporte, C. Y., Munoz, M., Mejia Miranda, J., & OConnor, R. V. (2018). Applying software engineering standards in very small entities: From startups to grownups. *IEEE Software, 35*(1), 99–103. https://doi.org/10.1109/MS.2017.4541041

Peffers, K., Tuunanen, T., Rothenberger, M. A., & Chatterjee, S. (2007). A design science research methodology for information systems research. *Journal of Management Information Systems, 24*(3), 45–77. https://doi.org/10.2753/MIS0742-1222240302

Pino, F. J., García, F., & Piattini, M. (2008). Software process improvement in small and medium software enterprises: A systematic review. *Software Quality Journal, 16*(2), 237–261. https://doi.org/10.1007/s11219-007-9038-z

Vives, L., Melendez, K., & Dávila, A. (2022). ISO/IEC 29110 and software engineering education: A systematic mapping study. *Programming and Computer Software, 48*(8), 745–755. https://doi.org/10.1134/S0361768822080229

