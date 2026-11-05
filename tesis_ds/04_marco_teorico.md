# E4. Marco teórico: sustentación del objeto de estudio

## Alcance y estado de verificación

Este marco teórico sustenta el objeto de estudio definido en la delimitación: el **marco ligero de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños o áreas de software en profesionalización**. La búsqueda inicial se orientó a fuentes primarias, normas y documentación técnica verificable sobre entidades muy pequeñas, mejora de procesos, conocimiento aceptado en Ingeniería de Software, gestión visible del trabajo, control de cambios, solicitudes de integración de cambios y pruebas unitarias.

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

La relación con el diseño es concreta. La precondición de repositorio oficial o excepción documentada se sustenta en gestión de configuración; la gestión visible de tareas se relaciona con gestión de Ingeniería de Software; las solicitudes de integración de cambios se apoyan en control de cambios y revisión; y las pruebas unitarias pertenecen al área de pruebas y calidad. Por tanto, el marco debe mostrar trazabilidad entre cada práctica y un área aceptada de la disciplina, evitando una fundamentación decorativa.

### Transparencia, inspección y adaptación como principios de gestión visible

La Scrum Guide define Scrum como un marco ligero para generar valor mediante soluciones adaptativas a problemas complejos, basado en empirismo y pensamiento lean. Sus pilares de transparencia, inspección y adaptación son particularmente relevantes para equipos pequeños que hoy gestionan trabajo parcialmente invisible (Schwaber & Sutherland, 2020). Aunque la tesis no implantará Scrum completo, sí puede usar estos principios para fundamentar la decisión de hacer visible el trabajo en Odoo.

La decisión de diseño no es “usar Scrum”, porque eso sería una afirmación metodológica más amplia que la evidencia prevista. La decisión es más acotada: toda práctica del marco debe aumentar la transparencia operacional del equipo y permitir inspección frecuente. En PRX, esto se traduce en exigir que las tareas activas estén registradas y visibles, que los cambios relevantes puedan rastrearse en GitHub y que las pruebas unitarias proporcionen una señal mínima antes de integrar cambios.

### Calidad y granularidad de las tareas

La calidad de una tarea no se reduce a que exista un registro en una herramienta. La ingeniería de requisitos ágil trata la claridad, la completitud y la posibilidad de evaluar los elementos de trabajo como propiedades que condicionan su uso posterior (Cao & Ramesh, 2008; Lucassen et al., 2016). ISO/IEC/IEEE 29148:2018 sitúa la ingeniería de requisitos dentro de los procesos de ciclo de vida, sin prescribir la plantilla ligera de una organización particular (IEEE, 2018). De manera complementaria, Liskin et al. (2014) muestran la necesidad de tratar explícitamente la granularidad de las historias de usuario. Estas fuentes sustentan que el marco exija información mínima y que una tarea se divida cuando no pueda verificarse como una unidad; no justifican, por sí solas, los seis campos exactos definidos para PRX.

En consecuencia, descripción, responsable, componente, criterio de aceptación, estado y criterio de terminado se conservan como una operacionalización contextual de la tarea válida. La regla no debe presentarse como un estándar universal ni los umbrales de división como una medida de madurez. Su aplicabilidad y carga deberán contrastarse con los participantes durante la evaluación, antes de considerarla un principio transferible.

### Flujo de cambios basado en ramas y solicitudes de integración

La documentación oficial de GitHub Flow describe un flujo ligero basado en ramas, cambios confirmados mediante commits, solicitudes de integración de cambios y revisión antes de fusionar hacia la rama principal (GitHub Docs, s. f.-c). Esta fuente es pertinente porque PRX usa GitHub como repositorio institucional, y el marco propuesto no necesita introducir una herramienta adicional para controlar cambios. El diseño debe aprovechar la infraestructura existente para reducir fricción de adopción.

GitFlow propone dos ramas principales de larga duración, `master` y `develop`, además de ramas de características, liberación y corrección urgente (Driessen, 2010). En contraste, el desarrollo basado en tronco privilegia una rama central y evita ramas de desarrollo de larga duración, aunque admite ramas breves por tarea y ramas temporales de liberación cuando el contexto lo requiere (Hammant, s. f.-a, s. f.-b). La tesis no afirma que GitFlow sea incorrecto; se descarta para la aplicación inicial porque añadir `develop` como segunda rama permanente habría creado una carga de coordinación que la línea base no demostró que PRX pueda sostener.

El diseño se inspira en *Trunk-Based Development* —desarrollo basado en tronco—, pero no pretende una implementación pura. `main` es el tronco de integración y las ramas temporales se vinculan con tareas concretas; `Stage` y `Production` solo se mantienen cuando existe el ambiente o mecanismo de promoción correspondiente. Estos nombres proceden de configuraciones observadas en PRX y no constituyen una prescripción universal.

La cadena tarea → rama → commit → solicitud de integración → evidencia se define como una forma mínima de trazabilidad de cambios. La literatura de trazabilidad estudia la creación, gestión y uso de relaciones entre artefactos de software (Cleland-Huang et al., 2014); no obstante, el marco no pretende cubrir toda la trazabilidad entre requisitos, diseño, código, pruebas y liberaciones. Su función es acotada: permitir reconstruir un cambio técnico desde una tarea visible hasta la evidencia de su verificación, y recorrer la relación también en sentido inverso.

Para hacer visible esa cadena en el historial, la convención de commits adapta el encabezado `<tipo>(<alcance>): <resumen breve>` de Angular y la estructura tipo–alcance opcional–descripción de Conventional Commits (Angular, s. f.; Conventional Commits, s. f.). En PRX, el campo entre paréntesis representa el código de tarea y no el alcance técnico, porque el objetivo de diseño es conservar el vínculo con Odoo incluso si se elimina la rama temporal. Esta adaptación no debe atribuirse a Google ni presentarse como adopción literal de una especificación externa.

De estas fuentes se derivan varias decisiones de diseño. Cada componente debe contar con repositorio institucional **o una excepción documentada**, pues la migración inmediata puede ser inviable o riesgosa. Cada cambio no trivial debe ocurrir en una rama con nombre descriptivo y código de tarea; la integración a la rama principal debe realizarse mediante solicitud de integración con descripción, evidencia de verificación y estado de validación. Estas reglas convierten el trabajo individual en trabajo inspeccionable sin imponer una segunda rama de desarrollo permanente.

Las solicitudes de integración cumplen funciones técnicas y de coordinación que exceden la detección de defectos (Bacchelli & Bird, 2013). Por esta razón, la plantilla del marco exige declarar cambio, componentes afectados, riesgo, prueba, evidencia y validación. GitHub diferencia revisiones humanas de comprobaciones de estado automatizadas antes de la fusión; en consecuencia, el marco separa auto-validación documentada, validación automática y revisión por tercero, y no presenta la primera como equivalente de una revisión independiente (GitHub Docs, s. f.-b).

La investigación empírica sobre revisión contemporánea confirma que el proceso de revisión incluye coordinación, comunicación y control técnico, además de la búsqueda de defectos (Gousios et al., 2015; Rigby & Bird, 2013; Sadowski et al., 2018). McIntosh et al. (2014) estudian la relación entre cobertura de revisión, participación y calidad en tres proyectos, mientras que Barnett et al. (2015) abordan la descomposición de conjuntos de cambios para facilitar su revisión. Estas fuentes respaldan dos límites de diseño: una solicitud de integración debe mantener un cambio comprensible y la evidencia de una solicitud no acredita por sí sola una revisión independiente ni una mejora de calidad en PRX.

La fusión por compresión se propone solo como opción de la instanciación PRX. Este mecanismo consolida los commits de una rama temporal en un solo commit y puede simplificar el historial, pero también pierde detalle sobre los commits originales y sus autores (GitHub Docs, s. f.-a). Por ello, solo es adecuada cuando la solicitud de integración conserva el contexto y el mensaje final mantiene el código de tarea.

### Pruebas unitarias iniciales y verificación mínima

Aniche (2022) sostiene una aproximación sistemática a las pruebas de software, con énfasis en diseñar pruebas que tengan mayor probabilidad de encontrar defectos, usar métricas de cobertura con criterio y distinguir entre pruebas unitarias, de integración y de sistema. Esta fuente sustenta la decisión de no exigir una estrategia completa de pruebas en la primera versión del marco. Para un equipo con baja formalización, la adopción inicial debe comenzar por pruebas unitarias en componentes críticos, no por una pirámide completa de pruebas imposible de sostener en dos semanas.

La implicación de diseño es que el marco debe incluir una regla mínima de selección de componentes críticos. Un componente será crítico si concentra lógica de negocio, transforma datos relevantes, participa en integraciones con Odoo o ha sido fuente reciente de defectos. La métrica inicial no será cobertura total, sino existencia de prueba, construcción, prueba de API o verificación técnica documentada en al menos un componente crítico de Central. Esta decisión es deliberadamente modesta, porque busca generar una práctica sostenible antes que un indicador cosmético.

### Entrega, configuración e identificación de versiones

La trazabilidad de un cambio no termina necesariamente con su fusión. La entrega continua relaciona construcción, pruebas y despliegue, por lo que el marco incorpora un registro mínimo de ambiente, rama o versión, fecha, responsable y mecanismo de despliegue (Duvall et al., 2007; Humble & Farley, 2010). La primera versión no impone automatización de CI/CD ni una herramienta de despliegue particular; exige que, cuando haya una entrega relevante, exista evidencia que permita identificar qué cambio llegó a qué ambiente.

Semantic Versioning ofrece una referencia para comunicar compatibilidad mediante números de versión cuando un componente expone una interfaz pública (Semantic Versioning, s. f.). No se adopta como obligación para todos los repositorios de PRX, porque no todos distribuyen bibliotecas o exponen contratos versionados. En consecuencia, la versión es una evidencia aceptable junto con rama, etiqueta o registro de despliegue, y C5 se mantiene como componente diseñado pero aún no evaluado en la aplicación inicial.

IEEE Std 828-2012 sitúa la gestión de configuración como una disciplina para identificar y controlar la información y los elementos sujetos a cambio (Institute of Electrical and Electronics Engineers [IEEE], 2012). Su función aquí no es imponer un plan formal de configuración propio de un proyecto grande, sino reforzar que el registro de entrega no debe depender únicamente de memoria individual. La selección exacta de ambiente, rama o versión, fecha, responsable y mecanismo de despliegue continúa siendo una adaptación mínima de PRX que C5 deberá evaluar.

### Modelos de madurez y riesgo de sobrealcance

La página oficial del CMMI Model Viewer muestra que CMMI ofrece áreas de práctica, prácticas, materiales suplementarios y vistas personalizables del modelo para adopción según necesidades y objetivos de negocio (CMMI Institute, s. f.). Esta fuente confirma que CMMI puede servir como referencia conceptual de mejora de capacidades, pero no justifica prometer una subida de nivel de madurez en esta tesis. El acceso completo al contenido del modelo requiere suscripción, por lo que cualquier uso detallado de prácticas específicas deberá verificarse posteriormente contra el material oficial disponible para el tesista.

La decisión de diseño es usar CMMI solo como antecedente de mejora de procesos, no como núcleo evaluativo. El marco no medirá si PRX alcanza un nivel CMMI, ni afirmará equivalencias de madurez. Su evaluación se limitará a criterios observables: tareas visibles, conformidad de ramas y commits, uso de solicitudes de integración de cambios y pruebas unitarias iniciales. Esta restricción protege la tesis de un sobrealcance metodológico.

## Trazabilidad entre teoría y decisiones de diseño

| Decisión de diseño del marco | Fuente que la sustenta | Implicación concreta para el artefacto |
|:--|:--|:--|
| Diseñar un marco ligero y gradual, no un modelo completo de madurez | ISO/IEC 29110-1-1:2024 | El artefacto se estructura como ruta mínima de adopción para equipos pequeños. |
| Declarar prácticas pertenecientes a áreas reconocidas de Ingeniería de Software | SWEBOK Guide V4.0 | Cada práctica se vincula con gestión de configuración, proceso, gestión, pruebas o calidad. |
| Hacer visible el trabajo activo | Scrum Guide 2020 | Las tareas deben registrarse en Odoo y ser inspeccionables por el equipo. |
| Exigir información mínima y verificabilidad de las tareas | Cao y Ramesh (2008); Lucassen et al. (2016); Liskin et al. (2014) | RQ2 y RQ3 se presentan como operacionalizaciones contextuales, sujetas a evaluación de aplicabilidad. |
| Exigir repositorio institucional o excepción documentada, ramas, commits y solicitudes de integración de cambios | GitHub Flow | Todo cambio relevante debe ser trazable y revisable en GitHub sin forzar migraciones riesgosas. |
| Preferir `main` y ramas temporales breves sobre GitFlow completo | Driessen (2010); Hammant (s. f.-a, s. f.-b) | El flujo se declara inspirado en desarrollo basado en tronco y evita `develop` como rama permanente. |
| Adaptar el formato de commit al código de tarea | Angular (s. f.); Conventional Commits (s. f.) | Rama, commit y solicitud conservan el identificador de Odoo. |
| Distinguir auto-validación, comprobaciones y revisión independiente | Bacchelli y Bird (2013); GitHub Docs (s. f.-b) | La plantilla registra el estado real de validación sin fingir revisión por pares. |
| Mantener solicitudes de integración acotadas y no confundirlas con calidad o revisión independiente | Gousios et al. (2015); Rigby y Bird (2013); Sadowski et al. (2018); McIntosh et al. (2014); Barnett et al. (2015) | La solicitud conserva contexto y evidencia, pero la auto-validación se registra como excepción. |
| Usar fusión por compresión solo cuando convenga | GitHub Docs (s. f.-a) | La fusión es opcional y debe preservar la trazabilidad de la tarea. |
| Incorporar pruebas unitarias iniciales en componentes críticos | Aniche (2022) | La adopción inicial se limita a pruebas ejecutables en componentes de alto riesgo. |
| Registrar entrega y configuración mínimas | Duvall et al. (2007); Humble y Farley (2010); Semantic Versioning (s. f.) | C5 registra ambiente, rama o versión, responsable, fecha y mecanismo sin imponer CI/CD. |
| Tratar la entrega como información de configuración controlada | IEEE Std 828-2012 | C5 conserva un registro mínimo y no se equipara con un proceso formal de gestión de configuración. |
| No prometer certificación ni subida de nivel CMMI | CMMI Model Viewer | CMMI queda como antecedente, no como criterio de evaluación de la tesis. |

## Prueba de eliminación

Este marco teórico pasa parcialmente la prueba de eliminación. Si se eliminan ISO/IEC 29110 y SWEBOK, el artefacto perdería su justificación como marco ligero para entidades pequeñas y su conexión con áreas reconocidas de Ingeniería de Software. Si se elimina Scrum Guide, la decisión de exigir visibilidad de tareas quedaría como preferencia local y no como principio de transparencia e inspección. Si se elimina GitHub Flow, las reglas de ramas, commits y solicitudes de integración quedarían sin fundamento operativo alineado con la herramienta real de PRX. Si se elimina Aniche (2022), la decisión de comenzar con pruebas unitarias en componentes críticos quedaría menos defendida.

Si se eliminan Cleland-Huang et al. (2014), Angular, Conventional Commits, Driessen, Hammant y GitHub Docs, el diseño conservaría sus reglas internas, pero perdería su justificación para distinguir trazabilidad mínima, formatos de commits, alternativas de ramificación, estados de validación y límites de la fusión por compresión. Del mismo modo, sin Duvall et al. (2007), Humble y Farley (2010) y Semantic Versioning, C5 quedaría como una lista local de campos sin conexión explícita con entrega e identificación de versiones.

La búsqueda académica adicional sobre mejora de procesos en pequeñas organizaciones fue reforzada con Pino et al. (2008), Laporte et al. (2018), Buchalcevova (2021) y Vives et al. (2022). La base de conocimiento se complementó posteriormente con fuentes sobre trazabilidad, revisión, granularidad de tareas, gestión de configuración y reporte de casos, registradas en `04_plan_ampliacion_bibliografica.md` y `referencias.md`. E4 queda cerrada como fundamentación del objeto de estudio: las adaptaciones específicamente locales —campos exactos de plantilla, niveles 0–5 y auto-validación— se declaran como decisiones contextuales, no como teoría general.

## Referencias

Aniche, M. (2022). *Effective software testing: A developer's guide*. Manning Publications. https://www.manning.com/books/effective-software-testing

CMMI Institute. (s. f.). *CMMI Model Viewer*. ISACA. Recuperado el 22 de septiembre de 2026, de https://cmmiinstitute.com/cmmi/model-viewer/

GitHub Docs. (s. f.-c). *GitHub flow*. Recuperado el 22 de septiembre de 2026, de https://docs.github.com/en/get-started/using-github/github-flow

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

Angular. (s. f.). *Commit message format*. Recuperado el 29 de octubre de 2026, de https://github.com/angular/angular/blob/main/contributing-docs/commit-message-guidelines.md

Bacchelli, A., & Bird, C. (2013). Expectations, outcomes, and challenges of modern code review. In *2013 35th International Conference on Software Engineering (ICSE)* (pp. 712–721). IEEE. https://doi.org/10.1109/ICSE.2013.6606617

Cleland-Huang, J., Gotel, O. C. Z., Huffman Hayes, J., Mäder, P., & Zisman, A. (2014). Software traceability: Trends and future directions. *Future of Software Engineering Proceedings*, 55–69. https://doi.org/10.1145/2593882.2593891

Conventional Commits. (s. f.). *Conventional Commits 1.0.0*. Recuperado el 29 de octubre de 2026, de https://www.conventionalcommits.org/en/v1.0.0/

Driessen, V. (2010, 5 de enero). *A successful Git branching model*. https://nvie.com/posts/a-successful-git-branching-model/

Duvall, P. M., Matyas, S., & Glover, A. (2007). *Continuous integration: Improving software quality and reducing risk*. Addison-Wesley Professional. https://www.informit.com/store/continuous-integration-improving-software-quality-9780321336385

GitHub Docs. (s. f.-a). *About merge methods on GitHub*. Recuperado el 29 de octubre de 2026, de https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/about-merge-methods-on-github

GitHub Docs. (s. f.-b). *About protected branches*. Recuperado el 29 de octubre de 2026, de https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches

Hammant, P. (s. f.-a). *Branch for release*. Recuperado el 29 de octubre de 2026, de https://trunkbaseddevelopment.com/branch-for-release/

Hammant, P. (s. f.-b). *Trunk Based Development: Introduction*. Recuperado el 29 de octubre de 2026, de https://trunkbaseddevelopment.com/

Humble, J., & Farley, D. (2010). *Continuous delivery: Reliable software releases through build, test, and deployment automation*. Addison-Wesley Professional. https://martinfowler.com/books/continuousDelivery.html

Semantic Versioning. (s. f.). *Semantic Versioning 2.0.0*. Recuperado el 29 de octubre de 2026, de https://semver.org/

Barnett, M., Bird, C., Brunet, J., & Lahiri, S. K. (2015). Helping developers help themselves: Automatic decomposition of code review changesets. In *2015 IEEE/ACM 37th IEEE International Conference on Software Engineering* (pp. 134–144). IEEE. https://doi.org/10.1109/ICSE.2015.35

Cao, L., & Ramesh, B. (2008). Agile requirements engineering practices: An empirical study. *IEEE Software, 25*(1), 60–67. https://doi.org/10.1109/MS.2008.1

Gousios, G., Zaidman, A., Storey, M.-A., & van Deursen, A. (2015). Work practices and challenges in pull-based development: The integrator's perspective. In *2015 IEEE/ACM 37th IEEE International Conference on Software Engineering* (pp. 358–368). IEEE. https://doi.org/10.1109/ICSE.2015.55

Institute of Electrical and Electronics Engineers. (2012). *IEEE standard for configuration management in systems and software engineering* (IEEE Std 828-2012). https://doi.org/10.1109/IEEESTD.2012.6170935

Institute of Electrical and Electronics Engineers. (2018). *ISO/IEC/IEEE international standard—Systems and software engineering—Life cycle processes—Requirements engineering* (ISO/IEC/IEEE 29148:2018). https://doi.org/10.1109/IEEESTD.2018.8559686

Liskin, O., Pham, R., Kiesling, S., & Schneider, K. (2014). Why we need a granularity concept for user stories. In *Agile processes in software engineering and extreme programming* (pp. 110–125). Springer. https://doi.org/10.1007/978-3-319-06862-6_8

Lucassen, G., Dalpiaz, F., van der Werf, J. M. E. M., & Brinkkemper, S. (2016). Improving agile requirements: The Quality User Story framework and tool. *Requirements Engineering, 21*(3), 383–403. https://doi.org/10.1007/s00766-016-0250-x

McIntosh, S., Kamei, Y., Adams, B., & Hassan, A. E. (2014). The impact of code review coverage and code review participation on software quality: A case study of the Qt, VTK, and ITK projects. In *Proceedings of the 11th Working Conference on Mining Software Repositories* (pp. 192–201). ACM. https://doi.org/10.1145/2597073.2597076

Rigby, P. C., & Bird, C. (2013). Convergent contemporary software peer review practices. In *Proceedings of the 2013 9th Joint Meeting on Foundations of Software Engineering* (pp. 202–212). ACM. https://doi.org/10.1145/2491411.2491444

Sadowski, C., Söderberg, E., Church, L., Sipko, M., & Bacchelli, A. (2018). Modern code review: A case study at Google. In *Proceedings of the 40th International Conference on Software Engineering: Software Engineering in Practice* (pp. 181–190). ACM. https://doi.org/10.1145/3183519.3183525






