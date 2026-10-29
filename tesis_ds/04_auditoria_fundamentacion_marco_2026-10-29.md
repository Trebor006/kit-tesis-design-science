# Auditoría de fundamentación bibliográfica del marco de trabajo

## Propósito y criterio de revisión

Esta auditoría revisa el **Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización**, documentado en `07b_requisitos.md`, `07c_diseno_artefacto.md` y `07f_ficha_artefacto.md`. No verifica si el marco fue adoptado ni si sus resultados fueron efectivos; verifica si cada decisión relevante cuenta con una justificación bibliográfica que influya en el diseño, conforme al criterio de trazabilidad de Design Science (Wieringa, 2014).

Los estados empleados son: **suficiente**, cuando existe sustento explícito y pertinente; **parcial**, cuando la fuente sustenta el principio general pero no la regla concreta; y **brecha**, cuando no existe aún una fuente integrada que justifique la decisión. Una brecha no implica que la decisión sea incorrecta: puede ser una adaptación contextual válida, pero debe documentarse como tal o recibir fundamentación adicional antes de presentarla como principio transferible.

## Matriz de cobertura bibliográfica

| Elemento definido del marco | Decisión o función | Sustento disponible y uso real | Estado | Vacío identificado o límite | Acción requerida | Prioridad |
|:--|:--|:--|:--|:--|:--|:--:|
| Tipología: marco con método, reglas, productos e indicadores | Declarar que la propuesta no es solo una configuración de GitHub. | La tipología de artefactos y Essence sustentan un marco compuesto por prácticas y elementos relacionados (March & Smith, 1995; Jacobson et al., 2012, 2013; Object Management Group, 2018). | Suficiente | Ninguno para declarar la tipología. | Mantener la definición y evitar denominarlo software o metodología cerrada. | Alta |
| Ligereza y adopción gradual | Empezar con prácticas mínimas de alto impacto, sin certificación ni proceso pesado. | ISO/IEC 29110 y estudios de entidades muy pequeñas justifican adaptación a capacidad y recursos (ISO & IEC, 2024a; Pino et al., 2008; Laporte et al., 2018). | Suficiente | No permite afirmar que cualquier conjunto mínimo producirá mejora. | Mantener condiciones de contorno y limitar conclusiones al caso evaluado. | Alta |
| C0. Precondiciones y gobernanza mínima | Identificar responsable, mecanismo de tareas y repositorio o excepción. | SWEBOK fundamenta gestión de configuración; ISO/IEC 29110 fundamenta el contexto de entidad pequeña (Washizaki, 2024; ISO & IEC, 2024a). | Parcial | Las categorías de excepción —cliente, tercero, cuenta personal— y su tratamiento no tienen fuente específica integrada. | Buscar literatura o norma sobre gobierno de repositorios y documentar que la clasificación inicial fue una adaptación derivada del diagnóstico. | Media |
| C1. Tarea válida | Exigir descripción, responsable, componente, criterios de aceptación, estado y criterio de terminado. | Calidad de requisitos y elementos ágiles: Cao y Ramesh (2008), Lucassen et al. (2016) e IEEE 29148 (2018). | Parcial | Las fuentes no prescriben exactamente estos seis campos ni el criterio local de tarea válida. | Declarar la lista como operacionalización contextual y contrastar aplicabilidad y carga con practicantes. | Alta |
| C1. División de tareas | Dividir tareas con objetivos, componentes o verificaciones independientes. | Liskin et al. (2014) sustentan la necesidad de un concepto explícito de granularidad; el diagnóstico de PConst muestra el problema local. | Parcial | No fundamenta el umbral de “excede el ciclo acordado”. | Mantener ese umbral como heurística contextual y contrastarlo con practicantes. | Media |
| C2. Ramas temporales | Usar `<tipo>/<codigo-tarea>-<descripcion-corta>` y eliminar ramas después de integrar. | GitHub Flow respalda ramas separadas por cambios no relacionados y su eliminación tras la integración (GitHub Docs, s. f.-c). | Suficiente | El código de tarea y los tipos son adaptación PRX. | Mantener explícita la adaptación a Odoo; no presentar el formato completo como prescripción universal. | Alta |
| C2. Commits trazables | Usar `<tipo>(<codigo-tarea>): <descripcion breve>`. | Angular y Conventional Commits sustentan la estructura tipo–alcance–descripción legible y analizable (Angular, s. f.; Conventional Commits, s. f.). | Suficiente | El código de tarea sustituye al alcance técnico. | Conservar la explicación de que es adaptación contextual, no adopción literal. | Alta |
| C2. Tipos iniciales limitados | Restringir inicialmente los tipos a `feat`, `fix`, `hotfix`, `config`, `test`, `docs` y `refactor`. | Angular y Conventional Commits respaldan el uso de tipos; la reducción a siete tipos responde a la tensión de adopción. | Parcial | `hotfix` y `config` no son tipos centrales de la especificación, y no hay evidencia específica de que siete sea el número adecuado. | Declarar los tipos como vocabulario mínimo V1.0 y evaluar claridad/aplicabilidad en entrevistas; no generalizar el conjunto. | Media |
| C2. Ramas permanentes | Usar `main` como tronco; `Stage` y `Production` solo cuando correspondan a ambientes reales. | Desarrollo basado en tronco sustenta la rama central y ramas de liberación solo cuando son necesarias (Hammant, s. f.-a, s. f.-b). | Parcial | Los nombres `Stage` y `Production` proceden de la configuración observada, no de un estándar general. | Documentar su origen contextual y mantener la condición “cuando aplique”. | Alta |
| C2. Flujo de ramificación | Preferir flujo inspirado en desarrollo basado en tronco y descartar GitFlow completo. | GitFlow expone ramas `master` y `develop` de larga duración; desarrollo basado en tronco privilegia una rama central y ramas breves (Driessen, 2010; Hammant, s. f.-a, s. f.-b). | Suficiente | No equivale a una implementación pura de desarrollo basado en tronco. | Mantener el término “inspirado en desarrollo basado en tronco”. | Alta |
| C3. Solicitud de integración válida | Exigir plantilla con tarea, cambios, riesgo, prueba, evidencia y validación. | GitHub documenta solicitudes de integración; Bacchelli y Bird (2013), Gousios et al. (2015), Rigby y Bird (2013) y Sadowski et al. (2018) sustentan sus funciones técnicas y de coordinación. | Parcial | Las secciones exactas de la plantilla, especialmente riesgo y archivos modificados, aún no tienen sustento individual. | Justificar los campos como respuesta al diagnóstico y evaluar su claridad y carga con entrevistas. | Alta |
| C3. Validación progresiva | Distinguir solicitud trazable, plantilla completa, auto-validación, validación automática y revisión por tercero. | La literatura de revisión de código respalda que la revisión tiene funciones relevantes (Bacchelli & Bird, 2013). | Parcial | Falta evidencia integrada que justifique la escala de cinco estados y la equivalencia o diferencia entre ellos. | Declarar la escala como constructo del marco y evaluar comprensión, cobertura y consistencia con practicantes. | Alta |
| C3. Auto-validación como excepción | Aceptarla cuando no existe revisor independiente. | GitHub diferencia aprobación de una persona y comprobaciones de estado; la literatura sobre revisión contemporánea confirma funciones y prácticas de revisión, pero no equipara auto-validación con revisión por tercero (Rigby & Bird, 2013; Sadowski et al., 2018). | Parcial | No existe evidencia que valide la excepción o defina controles compensatorios para equipos pequeños. | Mantenerla como excepción registrada, no como práctica equivalente a revisión por pares; evaluar su comprensión y fricción. | Alta |
| C3. Fusión por compresión | Recomendar `squash merge` cuando corresponda y conservar el código de tarea. | GitHub documenta que consolida commits y simplifica historial, junto con pérdida de detalle de commits originales (GitHub Docs, s. f.-a). | Suficiente como opción | No demuestra que sea superior para PRX. | Mantenerla opcional y conservar detalles en la solicitud de integración. | Media |
| C4. Verificación técnica mínima | Exigir qué se verificó, cómo y con qué evidencia. | Pruebas y verificación temprana se sustentan en Aniche (2022), Buchalcevova (2021), Duvall et al. (2007) y Humble y Farley (2010). | Suficiente | La lista de evidencias permitidas no tiene igual fuerza probatoria. | Diferenciar en la evaluación prueba ejecutable, construcción, prueba manual y justificación; no tratarlas como equivalentes. | Alta |
| C4. Prueba unitaria o equivalente en componente crítico | Exigir una señal ejecutable en al menos un componente crítico. | Aniche (2022) y Buchalcevova (2021) justifican atención explícita a pruebas en adopción inicial. | Parcial | La definición de “componente crítico” y la sustitución por evidencia equivalente son locales. | Conservar la definición explícita y marcar la equivalencia como decisión contextual de V1.0. | Media |
| C5. Registro mínimo de entrega | Registrar ambiente, rama o versión, fecha, responsable y mecanismo de despliegue. | Entrega continua relaciona construcción, pruebas y despliegue; IEEE 828 fundamenta información de configuración controlada y Semantic Versioning ilustra identificación de versiones cuando existe API pública (IEEE, 2012; Humble & Farley, 2010; Duvall et al., 2007; Semantic Versioning, s. f.). | Parcial | La fuente no prescribe el conjunto exacto de campos y C5 no fue aplicado. | Mantener los campos como adaptación mínima y no formular C5 como principio validado sin aplicación. | Alta |
| C6. Seguimiento y mejora | Registrar indicadores, excepciones, fricciones y rediseños. | DSRM y FEDS sustentan evaluación, aprendizaje iterativo y rediseño (Peffers et al., 2007; Venable et al., 2016). | Parcial | La estructura de informe de adopción e indicadores es propia; falta validar que sea utilizable para practicantes. | Vincular cada indicador con requisito y conservar la bitácora de rediseño; contrastar usabilidad en entrevistas. | Alta |
| Niveles de adopción 0–5 | Ordenar visibilidad, trazabilidad, integración, verificación y entrega. | La secuencia refleja los componentes C1–C5 y no se presenta como CMMI. | Brecha | No hay fuente que fundamente la escala, sus umbrales o que pruebe que los niveles son ordinales. | Declararla como constructo exploratorio derivado del diseño; no usarla para clasificar madurez ni afirmar progreso organizacional sin evaluación adicional. | Alta |
| Trazabilidad bidireccional | Recorrer tarea → rama → commit → solicitud → evidencia y en sentido inverso. | La literatura de trazabilidad sustenta gestionar relaciones entre artefactos; GitHub Flow y las convenciones cubren la cadena mínima propuesta (Cleland-Huang et al., 2014; GitHub Docs, s. f.-c). | Parcial | La fuente no prescribe los cinco eslabones ni los criterios de completitud de PRX. | Definir I9 como trazabilidad mínima contextual y no como implementación completa de trazabilidad de requisitos. | Muy alta |
| Agnosticismo de herramienta | Definir productos de trabajo equivalentes, no imponer Odoo o GitHub. | Essence distingue prácticas de sus instanciaciones; el marco fue declarado como artefacto compuesto (Jacobson et al., 2012, 2013; Object Management Group, 2018). | Suficiente | La equivalencia concreta entre herramientas no fue evaluada. | Mantener transferencia analítica como pretensión, no como validación multi-herramienta. | Alta |
| Responsabilidad mínima | Asociar responsables a tarea, repositorio, excepción, validación y entrega. | Scrum sustenta responsabilidades explícitas; ISO/IEC 29110 y SWEBOK dan contexto de gestión (Schwaber & Sutherland, 2020; ISO & IEC, 2024a; Washizaki, 2024). | Parcial | No existe una fuente integrada que justifique la asignación de responsabilidad por cada elemento de la cadena. | Sustentar con gestión de configuración o presentar la asignación detallada como decisión de gobernanza contextual. | Media |
| Productos documentales en SharePoint y plantilla `.github` | Publicar y distribuir las reglas en las herramientas disponibles. | El agnosticismo de herramienta distingue el marco de su instanciación; la evidencia interna demuestra publicación. | Suficiente como instanciación | No debe presentarse como una práctica universal ni como evidencia de adopción. | Mantenerlo como decisión local de implementación y separar publicación de uso efectivo. | Media |
| Indicadores I1–I9 | Medir antes y después visibilidad, repositorios, trazabilidad, integración, evidencia y entrega. | Design Science exige criterios previos a la evaluación; DSRM y FEDS respaldan evaluación del artefacto (Peffers et al., 2007; Venable et al., 2016). | Parcial | Algunos indicadores son aplicables a una sola aplicación; I8 es contextual y C5 no cuenta con resultado. | No agregar indicadores nuevos después de la evaluación; declarar qué indicadores no pueden concluirse con la evidencia disponible. | Alta |

## Diagnóstico consolidado

La fundamentación del marco es **suficiente** para sus decisiones centrales: tipología de marco, ligereza para equipos pequeños, ramas y commits trazables, flujo inspirado en desarrollo basado en tronco, solicitudes de integración y verificación técnica mínima. No existe base para presentar todos sus detalles operativos como estándares universales; varios son adaptaciones necesarias al contexto de PRX.

Las brechas que deben atenderse antes de formular principios de diseño finales son, en este orden: (1) escala de validación progresiva y excepción de auto-validación; (2) niveles de adopción 0–5; (3) registro de entrega y configuración; y (4) granularidad de tareas y campos de la plantilla. La trazabilidad bidireccional ya cuenta con fundamento general, pero debe continuar declarada como cadena mínima contextual; la fusión por compresión quedó respaldada solo como opción de la instanciación PRX. Las reglas de tarea válida, división de tareas y campos de la plantilla no requieren necesariamente una nueva teoría, pero deben documentarse explícitamente como operacionalizaciones derivadas del diagnóstico y someterse a evaluación de aplicabilidad.

La consecuencia metodológica es clara: una fuente bibliográfica no debe usarse para “validar” retrospectivamente cada detalle. Cuando una decisión surgió del diagnóstico o de una restricción del contexto, debe declararse como adaptación contextual, conservar su evidencia de origen y limitar el alcance de la contribución. La entrevista pendiente puede aportar evidencia de aplicabilidad y fricción; no reemplaza la búsqueda bibliográfica para las decisiones que se pretenden transferir a otros equipos.

## Plan bibliográfico derivado de la auditoría

| Orden | Tema de búsqueda | Producto que debe sustentar | Decisión posterior posible |
|:--:|:--|:--|:--|
| 1 | Revisión de código y auto-revisión en equipos pequeños | Excepción de auto-validación y controles compensatorios. | Distinguir con rigor auto-validación, revisión independiente y validación automática. |
| 2 | Gestión de liberaciones, configuración y trazabilidad de despliegues | C5 y registro mínimo de entrega. | Precisar qué evidencia es suficiente para una entrega trazable. |
| 3 | Granularidad y calidad de elementos de trabajo | C1, tarea válida y criterio de división. | Confirmar o ajustar campos y regla de división. |
| 4 | Campos mínimos de una solicitud de integración | Plantilla de solicitud de integración. | Justificar o simplificar los campos de riesgo, prueba y validación. |

## Referencias

Angular. (s. f.). *Commit message format*. Recuperado el 29 de octubre de 2026, de https://github.com/angular/angular/blob/main/contributing-docs/commit-message-guidelines.md

Aniche, M. (2022). *Effective software testing: A developer's guide*. Manning Publications. https://www.manning.com/books/effective-software-testing

Bacchelli, A., & Bird, C. (2013). Expectations, outcomes, and challenges of modern code review. In *2013 35th International Conference on Software Engineering (ICSE)* (pp. 712–721). IEEE. https://doi.org/10.1109/ICSE.2013.6606617

Buchalcevova, A. (2021). Towards higher software quality in very small entities: ISO/IEC 29110 software basic profile mapping to testing standards. *International Journal of Information Technologies and Systems Approach, 14*(1), 79–96. https://doi.org/10.4018/IJITSA.2021010105

Conventional Commits. (s. f.). *Conventional Commits 1.0.0*. Recuperado el 29 de octubre de 2026, de https://www.conventionalcommits.org/en/v1.0.0/

Driessen, V. (2010, 5 de enero). *A successful Git branching model*. https://nvie.com/posts/a-successful-git-branching-model/

Duvall, P. M., Matyas, S., & Glover, A. (2007). *Continuous integration: Improving software quality and reducing risk*. Addison-Wesley Professional. https://www.informit.com/store/continuous-integration-improving-software-quality-9780321336385

GitHub Docs. (s. f.-a). *About merge methods on GitHub*. Recuperado el 29 de octubre de 2026, de https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/about-merge-methods-on-github

GitHub Docs. (s. f.-b). *About protected branches*. Recuperado el 29 de octubre de 2026, de https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches

GitHub Docs. (s. f.-c). *GitHub flow*. Recuperado el 29 de octubre de 2026, de https://docs.github.com/en/get-started/using-github/github-flow

Hammant, P. (s. f.-a). *Branch for release*. Recuperado el 29 de octubre de 2026, de https://trunkbaseddevelopment.com/branch-for-release/

Hammant, P. (s. f.-b). *Trunk Based Development: Introduction*. Recuperado el 29 de octubre de 2026, de https://trunkbaseddevelopment.com/

Humble, J., & Farley, D. (2010). *Continuous delivery: Reliable software releases through build, test, and deployment automation*. Addison-Wesley Professional. https://martinfowler.com/books/continuousDelivery.html

International Organization for Standardization, & International Electrotechnical Commission. (2024a). *ISO/IEC 29110-1-1:2024: Systems and software engineering — Lifecycle profiles for very small entities (VSEs) — Part 1-1: Overview*. https://www.iso.org/standard/85337.html

Jacobson, I., Ng, P.-W., McMahon, P. E., Spence, I., & Lidman, S. (2012). The essence of software engineering. *Communications of the ACM, 55*(12), 42–49. https://doi.org/10.1145/2380656.2380670

Jacobson, I., Ng, P.-W., McMahon, P. E., Spence, I., & Lidman, S. (2013). *The essence of software engineering: Applying the SEMAT kernel*. Addison-Wesley Professional. https://www.informit.com/store/essence-of-software-engineering-applying-the-semat-9780321885951

Laporte, C. Y., Munoz, M., Mejia Miranda, J., & OConnor, R. V. (2018). Applying software engineering standards in very small entities: From startups to grownups. *IEEE Software, 35*(1), 99–103. https://doi.org/10.1109/MS.2017.4541041

March, S. T., & Smith, G. F. (1995). Design and natural science research on information technology. *Decision Support Systems, 15*(4), 251–266. https://doi.org/10.1016/0167-9236(94)00041-2

Object Management Group. (2018). *Essence, Version 1.2*. https://www.omg.org/spec/Essence/1.2/About-Essence/

Peffers, K., Tuunanen, T., Rothenberger, M. A., & Chatterjee, S. (2007). A design science research methodology for information systems research. *Journal of Management Information Systems, 24*(3), 45–77. https://doi.org/10.2753/MIS0742-1222240302

Pino, F. J., García, F., & Piattini, M. (2008). Software process improvement in small and medium software enterprises: A systematic review. *Software Quality Journal, 16*(2), 237–261. https://doi.org/10.1007/s11219-007-9038-z

Schwaber, K., & Sutherland, J. (2020). *The Scrum Guide: The definitive guide to Scrum: The rules of the game*. https://scrumguides.org/scrum-guide.html

Semantic Versioning. (s. f.). *Semantic Versioning 2.0.0*. Recuperado el 29 de octubre de 2026, de https://semver.org/

Venable, J., Pries-Heje, J., & Baskerville, R. (2016). FEDS: A framework for evaluation in design science research. *European Journal of Information Systems, 25*(1), 77–89. https://doi.org/10.1057/ejis.2014.36

Washizaki, H. (Ed.). (2024). *Guide to the Software Engineering Body of Knowledge (SWEBOK Guide), Version 4.0*. IEEE Computer Society. https://www.computer.org/education/bodies-of-knowledge/software-engineering

Wieringa, R. J. (2014). *Design science methodology for information systems and software engineering*. Springer. https://doi.org/10.1007/978-3-662-43839-8

Barnett, M., Bird, C., Brunet, J., & Lahiri, S. K. (2015). Helping developers help themselves: Automatic decomposition of code review changesets. In *2015 IEEE/ACM 37th IEEE International Conference on Software Engineering* (pp. 134–144). IEEE. https://doi.org/10.1109/ICSE.2015.35

Cao, L., & Ramesh, B. (2008). Agile requirements engineering practices: An empirical study. *IEEE Software, 25*(1), 60–67. https://doi.org/10.1109/MS.2008.1

Gousios, G., Zaidman, A., Storey, M.-A., & van Deursen, A. (2015). Work practices and challenges in pull-based development: The integrator's perspective. In *2015 IEEE/ACM 37th IEEE International Conference on Software Engineering* (pp. 358–368). IEEE. https://doi.org/10.1109/ICSE.2015.55

Institute of Electrical and Electronics Engineers. (2012). *IEEE standard for configuration management in systems and software engineering* (IEEE Std 828-2012). https://doi.org/10.1109/IEEESTD.2012.6170935

Institute of Electrical and Electronics Engineers. (2018). *ISO/IEC/IEEE international standard—Systems and software engineering—Life cycle processes—Requirements engineering* (ISO/IEC/IEEE 29148:2018). https://doi.org/10.1109/IEEESTD.2018.8559686

Liskin, O., Pham, R., Kiesling, S., & Schneider, K. (2014). Why we need a granularity concept for user stories. In *Agile processes in software engineering and extreme programming* (pp. 110–125). Springer. https://doi.org/10.1007/978-3-319-06862-6_8

Lucassen, G., Dalpiaz, F., van der Werf, J. M. E. M., & Brinkkemper, S. (2016). Improving agile requirements: The Quality User Story framework and tool. *Requirements Engineering, 21*(3), 383–403. https://doi.org/10.1007/s00766-016-0250-x

Rigby, P. C., & Bird, C. (2013). Convergent contemporary software peer review practices. In *Proceedings of the 2013 9th Joint Meeting on Foundations of Software Engineering* (pp. 202–212). ACM. https://doi.org/10.1145/2491411.2491444

Sadowski, C., Söderberg, E., Church, L., Sipko, M., & Bacchelli, A. (2018). Modern code review: A case study at Google. In *Proceedings of the 40th International Conference on Software Engineering: Software Engineering in Practice* (pp. 181–190). ACM. https://doi.org/10.1145/3183519.3183525
