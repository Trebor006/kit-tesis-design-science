# E1. Áreas y temas

## Área de experiencia mayor

El área de experiencia mayor de Robert Cabrera es el desarrollo de software empresarial, con énfasis en desarrollo backend, integración de sistemas y participación en proyectos de software para clientes internacionales. La experiencia declarada incluye Java, Spring, Spring Boot, APIs REST, SQL, PostgreSQL, SQL Server, diseño de bases de datos, Angular, TypeScript y desarrollo full stack.

La experiencia complementaria se concentra en arquitectura e integración de sistemas, DevOps, automatización, infraestructura, calidad de software, pruebas, monitoreo, observabilidad, seguridad y gestión técnica de procesos de desarrollo. Esta combinación permite abordar problemas de Ingeniería de Software situados en equipos pequeños que necesitan pasar de prácticas artesanales a prácticas mínimas disciplinadas.

## Contexto real disponible

El contexto real preliminar es PRX, una empresa pequeña y familiar que originalmente se orientaba a venta de servidores y que actualmente ofrece servicios de desarrollo de software. Según la observación inicial del tesista, la organización está en proceso de capacitación y profesionalización, con debilidades visibles en procesos de desarrollo, gestión de proyectos, calidad, pruebas, documentación, estándares, seguimiento, repositorios, arquitectura, infraestructura, despliegues, monitoreo y seguridad.

El acceso exacto al contexto todavía debe precisarse: número de participantes, roles, autorización para entrevistas, acceso a repositorios, acceso a tareas o incidencias, posibilidad de observar reuniones, posibilidad de aplicar un artefacto y posibilidad de realizar evaluación formativa y sumativa.

## Riesgo metodológico inicial

La idea inicial no debe formularse como “subir a PRX de nivel CMMI”, porque esa formulación tiene tres debilidades: puede convertirse en consultoría de mejora de procesos, puede prometer un cambio organizacional no demostrable en el tiempo disponible y puede usar CMMI como etiqueta diagnóstica sin evidencia suficiente. En Design Science, el problema debe conducir a un artefacto evaluable y a conocimiento transferible; por tanto, PRX debe tratarse como contexto de aplicación y no como objeto de estudio.

El problema de investigación, que en el formato institucional se registrará como problema científico, deberá formularse más adelante como brecha de conocimiento sobre cómo diseñar artefactos ligeros de adopción inicial de prácticas de Ingeniería de Software para organizaciones pequeñas o emergentes.

## Temas candidatos preliminares

| Tema candidato | Relevancia práctica | Sustentación teórica inicial | Problema de diseño tentativo | Tipo probable de artefacto | Clase de contextos | Contribución potencial de maestría | Base teórica a verificar |
|:--|:--|:--|:--|:--|:--|:--|:--|
| Marco ligero de adopción inicial de prácticas de Ingeniería de Software para microempresas y empresas emergentes | Alta, porque PRX parece necesitar prácticas mínimas antes de escalar formalmente procesos | Mejora de procesos de software, modelos de madurez, adopción incremental de prácticas | Equipos pequeños que desarrollan software de forma artesanal necesitan ordenar prácticas mínimas sin adoptar modelos pesados | Marco o método | Empresas pequeñas, familiares o emergentes que ofrecen software sin proceso definido | Principios para diseñar rutas ligeras de profesionalización técnica en organizaciones de baja madurez | CMMI Institute, CMMI Model [por verificar]; ISO/IEC 330xx [por verificar]; estudios sobre Software Process Improvement en pymes [por verificar] |
| Método mínimo de gestión técnica para proyectos de software en equipos pequeños | Alta, porque conecta gestión de requerimientos, seguimiento, repositorios, revisión y entrega | Gestión de proyectos de software, prácticas ágiles, control técnico del trabajo | Equipos pequeños carecen de un flujo mínimo para transformar requerimientos en entregables verificables | Método | Equipos de 3 a 10 personas con baja formalización | Principios para diseñar métodos mínimos de coordinación técnica sin burocratizar equipos pequeños | Scrum Guide [por verificar]; literatura de métodos ágiles y equipos pequeños [por verificar] |
| Método de adopción inicial de calidad y pruebas en organizaciones de baja madurez | Alta si PRX tiene defectos, retrabajo o ausencia de pruebas | Calidad de software, pruebas automatizadas, pirámide de pruebas, integración continua | Equipos pequeños no saben qué prácticas de calidad introducir primero ni cómo medir mejora | Método o composición método más plantilla de indicadores | Equipos pequeños con poca automatización de pruebas | Principios para priorizar prácticas de calidad en contextos con recursos limitados | ISO/IEC 25010 [por verificar]; literatura sobre pruebas automatizadas, calidad y CI/CD [por verificar] |
| Modelo de diagnóstico y priorización de prácticas DevOps para empresas pequeñas de software | Media-alta, si PRX tiene problemas de despliegue, monitoreo o operación | DevOps, CI/CD, capacidades de entrega, métricas de desempeño | Equipos pequeños adoptan herramientas de despliegue sin una secuencia clara de capacidades | Modelo o método | Organizaciones pequeñas con despliegues manuales o poco controlados | Principios para secuenciar capacidades DevOps iniciales según restricciones reales | DORA/Accelerate [por verificar]; literatura de DevOps en pymes [por verificar] |
| Marco inicial de seguridad, respaldo y monitoreo para equipos pequeños que desarrollan software | Media, porque depende de que seguridad sea el dolor principal de PRX | DevSecOps, gestión de riesgos, observabilidad, continuidad operativa | Equipos pequeños exponen software sin prácticas mínimas de protección, monitoreo y recuperación | Marco o método | Empresas pequeñas que operan aplicaciones para clientes | Principios para diseñar controles mínimos de seguridad y observabilidad sin equipo especializado | OWASP SAMM [por verificar]; OWASP ASVS [por verificar]; literatura DevSecOps [por verificar] |

## Lectura inicial de conveniencia

Por la experiencia del tesista y el contexto disponible, los candidatos más naturales son el primero y el segundo. El primero tiene mayor alineación con la intuición original de mejora de procesos y CMMI, pero debe acotarse para no convertirse en una promesa de certificación o madurez organizacional amplia. El segundo es más operacional y posiblemente más fácil de evaluar en PRX, porque puede medir cambios concretos en flujo de trabajo, trazabilidad, revisión, control de versiones y entrega.

El tercer tema es defendible si el dolor principal de PRX se expresa en defectos, retrabajo, regresiones o ausencia de pruebas. El cuarto y el quinto son técnicamente atractivos, pero deben elegirse solo si existe evidencia de que despliegues, operación, monitoreo o seguridad son el problema prioritario; de lo contrario, serían desvíos hacia áreas de interés del tesista y no hacia el problema real del contexto.

## Estado del gate E1

E1 no está cerrada. Falta seleccionar uno o dos temas candidatos y verificar que el contexto real permita construir y evaluar el artefacto.


## Actualización de contexto y selección del tema

El tesista corrigió el nombre del contexto organizacional: la empresa se denomina PRX, no PRC. PRX cuenta con dos equipos de desarrollo: uno orientado a WordPress y otro a software a medida. Participan aproximadamente siete desarrolladores; antes eran cuatro. La composición del equipo combina profesionales formados en Ingeniería de Software, Ingeniería Informática o Ingeniería de Sistemas, una persona con grado de maestría en software y miembros que aprendieron programación desde la práctica sin provenir originalmente del área.

El tesista indicó que dispone de autorización para entrevistar participantes y revisar repositorios y documentos. El problema más doloroso observado es la gestión técnica inicial: la empresa recién se está organizando, no seguía procesos de desarrollo, no existen buenas prácticas suficientemente estabilizadas, las pruebas son manuales, hay poca documentación y los despliegues son manuales.

El tema elegido para continuar es: **marco ligero de adopción inicial de prácticas de Ingeniería de Software para microempresas y empresas emergentes**. Este tema se selecciona porque representa mejor la clase de problema observada en PRX y permite construir un artefacto de tipo marco o método evaluable en un contexto real.

## Cierre de E1

E1 queda cerrada el 2026-09-22. El gate se considera satisfecho porque el tesista eligió un tema base, el contexto real existe, hay acceso declarado para entrevistas y revisión documental, y el problema práctico inicial está suficientemente localizado para pasar a delimitación. El avance a E2 no implica que el problema de diseño ni el problema de investigación estén aceptados todavía; ambos deben formularse con precisión en la siguiente etapa.
