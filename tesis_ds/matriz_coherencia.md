# Matriz de coherencia de la tesis

> Esta matriz se mantiene viva durante todo el proceso. Ningún eslabón debe contradecir a otro.

| Eslabón | Formulación actual | Estado | Observación |
|:--|:--|:--|:--|
| Problema de diseño | La línea de software a medida de PRX carece de una ruta ligera, común y verificable para adoptar prácticas mínimas de gestión técnica desde el inicio de los proyectos y producir evidencia verificable del trabajo realizado. | Formulado | Incluye contexto histórico, problema actual, solución conceptual y criterios preliminares de éxito; el cambio estructural se acota a prácticas mínimas de gestión técnica, no a transformación total de PRX. |
| Problema de investigación | Existe una brecha sobre cómo diseñar marcos ligeros de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de desarrollo con baja estandarización. En el formato institucional se registrará como problema científico. | Formulado | Reforzado con literatura académica verificada sobre mejora de procesos en pequeñas empresas, entidades muy pequeñas e ISO/IEC 29110. |
| Objeto de estudio | Marco ligero de adopción inicial de prácticas de Ingeniería de Software para equipos pequeños de desarrollo con baja estandarización. | Formulado | En Design Science el objeto es el artefacto propuesto, no PRX ni su proceso actual. |
| Campo de acción | Adopción inicial de prácticas mínimas de Ingeniería de Software en equipos pequeños de desarrollo con baja estandarización; contexto inicial: línea de software a medida de PRX. | Ajustado para evaluación inicial | La evaluación inicial se concentrará en el proyecto Central por contener tres componentes —Odoo, API y frontend— y permitir observar coordinación entre tres desarrolladores. Ansular y PConst quedan como evidencia diagnóstica y contexto comparativo, no como foco principal de aplicación inicial. |
| Objetivo | Diseñar, construir y evaluar un marco ligero de adopción inicial de prácticas de Ingeniería de Software para mejorar visibilidad, trazabilidad, evidencia verificable del avance y verificación básica, y derivar principios de diseño aplicables a contextos similares. | Formulado | Incluye construcción y contribución al conocimiento. |
| Pregunta de investigación | ¿Qué principios de diseño debe incorporar un marco ligero de adopción inicial de prácticas de Ingeniería de Software para mejorar la visibilidad del trabajo, la trazabilidad de cambios, la evidencia verificable del avance y la verificación básica del código en equipos pequeños de desarrollo con baja estandarización? | Formulada | Es prescriptiva, exige construcción y evaluación. |
| Artefacto | Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización. Incluye precondiciones y gobernanza mínima, gestión visible del trabajo, trazabilidad del código, integración y revisión de cambios, verificación técnica básica, entrega/configuración básica, y seguimiento y mejora del marco. | Construido documentalmente e instanciado parcialmente | Tipología principal: marco, con componentes de método, plantillas operativas, reglas mínimas, indicadores y niveles de adopción. El diseño está en `07c_diseno_artefacto.md`; la construcción inicial está en `07e_construccion_verificacion.md`; la ficha reproducible está en `07f_ficha_artefacto.md`. Odoo, GitHub, SharePoint y el repositorio organizacional `.github` son instanciaciones de PRX, no la definición formal del artefacto. |
| Método de evaluación | Línea base previa, construcción/aplicación de V1.0-Central, evaluación formativa con rediseño documentado y evaluación sumativa inicial en contexto real. | Formativa ejecutada; sumativa inicial de caso registrada | `CCC-7336` aporta aplicación real y verificación técnica; V1.1 formaliza el ajuste contextual de ramas. `08_resultado_sumativo_inicial_CCC-7336.md` compara un caso; falta medición por periodo comparable para afirmar mejora sostenida. |
| Criterios | 80 % de tareas activas visibles; 80 % de ramas y commits conformes; 70 % de cambios por solicitudes de integración; 70 % de solicitudes con evidencia mínima; al menos un componente crítico de Central con prueba, construcción, prueba de API o verificación técnica documentada. | Ajustados antes de evaluación | El ajuste responde a la delimitación posterior de la primera aplicación en Central y debe documentarse como decisión metodológica previa a la evaluación, no como ajuste post-hoc de resultados. |
| Evidencia | Línea base GitHub documentada en `06_linea_base_github.md`; línea base de tareas Odoo documentada en `06_linea_base_odoo_tareas.md`; indicadores I1 a I9 consolidados en `06_consolidacion_indicadores.md`; evidencias de intervención `E-ORG-INT-01` a `E-ORG-INT-05` y `E-GH-ORG-01`; plan de evidencias en `06_plan_evidencias_privadas.md`. | Parcialmente consolidada | La línea base y la construcción inicial están respaldadas. Falta evidencia de aplicación real y evaluación: `E-GH-INT-01`, `E-TEST-INT-01`, `E-FORM-01` y `E-SUM-01`. |
| Contribución | Principios de diseño para marcos ligeros de adopción inicial de prácticas de Ingeniería de Software en equipos pequeños de desarrollo con baja estandarización. | Formulada preliminarmente | `10_contribucion_conclusiones.md` contiene principios candidatos, no validados todavía. La contribución no debe presentarse como final hasta completar evaluación formativa, rediseño y sumativa inicial. |











