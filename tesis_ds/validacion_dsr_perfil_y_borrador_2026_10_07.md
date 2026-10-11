# Validación DSRM del perfil y borrador del hito

## Propósito

Este documento revisa si el perfil y el borrador del hito están alineados con Design Science Research Methodology (DSRM) y con el estándar de tesis de maestría en Ingeniería de Software. La revisión distingue lo que ya está suficiente para el hito, lo que está en progreso y lo que no debe presentarse como cerrado todavía.

## Veredicto ejecutivo

El trabajo está **alineado con DSRM** y es defendible como tesis de maestría en Design Science si mantiene tres controles metodológicos: no mezclar línea base con intervención, ejecutar al menos un ciclo formativo con rediseño documentado y no reclamar una contribución más amplia que la evidencia obtenida en Central. El perfil ya cumple las condiciones estructurales principales; el borrador del hito queda fuerte en diagnóstico, decisión de artefacto, requisitos, diseño preliminar y plan de construcción. Lo pendiente crítico es evidenciar la intervención y preparar la evaluación formativa.

## Alineación con DSRM

| Actividad DSRM | Evidencia actual en la tesis | Estado | Observación |
|:--|:--|:--|:--|
| 1. Identificación del problema y motivación | `02_delimitacion.md`, `06_linea_base_github.md`, `06_linea_base_odoo_tareas.md`, `06_consolidacion_indicadores.md`, `borrador_hito_2026_10_05.md`. | Suficiente para hito | El problema ya no es genérico: se formuló como falta de ruta ligera, común y verificable para gestión técnica trazable. |
| 2. Objetivos de la solución | `matriz_coherencia.md`, `07b_requisitos.md`, indicadores I1-I9 y criterios fijados antes de construir. | Suficiente para hito | Los criterios están definidos antes de la intervención, lo que protege contra criterios definidos a posteriori. |
| 3. Diseño y desarrollo | `07a_alternativas.md`, `07b_requisitos.md`, `07c_diseno_artefacto.md`, `07c_plantilla_solicitud_integracion.md`, `07d_plan_construccion.md`. | En construcción | Ya existe diseño preliminar y plan V1.0-Central. Falta registrar construcción/verificación interna en E7e. |
| 4. Demostración | Repositorio organizacional `.github` creado y plantilla visible; aplicación prevista en Central. | Iniciada | Debe guardarse evidencia `E-GH-ORG-01` y luego al menos una solicitud de integración real usando la plantilla. |
| 5. Evaluación | Línea base y plan de evaluación formativa/sumativa. | Planificada | Falta ejecutar evaluación formativa, rediseño y evaluación sumativa. No debe presentarse como cerrada. |
| 6. Comunicación | Perfil limpio, borrador de hito, matriz de coherencia y archivos E7. | En progreso | La tesis aún debe integrar resultados, contribución y conclusiones después de evaluación. |

## Validación del perfil de investigación DS

| Requisito del perfil DS | Estado actual | Evaluación |
|:--|:--|:--|
| Problema de diseño y problema de investigación diferenciados | Cumplido | El problema de investigación —que en el formato institucional se registrará como problema científico— está formulado como brecha de diseño de marcos ligeros, no como simple necesidad de PRX. |
| Objeto de estudio como artefacto | Cumplido | El objeto es el marco ligero progresivo, no PRX ni su proceso actual. |
| Tipología del artefacto declarada | Cumplido | Marco con componentes de método, plantillas, reglas, indicadores y niveles de adopción. |
| Pregunta prescriptiva y de clase | Cumplido | La pregunta exige construir y evaluar; no puede responderse sin artefacto. |
| Objetivo con construcción y contribución al conocimiento | Cumplido | Diseñar, construir y evaluar el marco, y derivar principios de diseño. |
| Base de conocimiento conectada al diseño | Parcial suficiente | Existen referencias a ISO/IEC 29110, mejora de procesos en pequeñas organizaciones, Scrum, GitHub Flow, pruebas y DS. Para tesis completa debe fortalecerse E4/E5. |
| Estrategia de evaluación formativa y sumativa | Planificada | Está declarada, pero falta ejecutarla. No debe redactarse en pasado. |
| Criterios de éxito definidos antes de construir | Cumplido | Indicadores y metas están en matriz de coherencia y diagnóstico. |
| Cronograma con rediseño | Parcial | E7d reconoce V1.1-Central como rediseño formativo; debe protegerse tiempo real para ejecutarlo. |
| Contribución calibrada a maestría | Cumplido si se mantiene el alcance | La contribución debe formularse como principios de diseño con generalización analítica, no como teoría general. |

## Validación del borrador del hito

| Componente del borrador | Estado | Comentario |
|:--|:--|:--|
| Diagnóstico con línea base | Fuerte | Hay GitHub, Odoo, indicadores y evidencia contextual. Falta resguardar capturas privadas. |
| Artefacto decidido | Fuerte | La alternativa seleccionada está justificada y no se reduce a GitHub/Odoo. |
| Requisitos E7b | Suficiente para hito | Los requisitos tienen criterio, fuente y prioridad. |
| Diseño E7c | Suficiente para hito | Incluye componentes C0-C6, reglas, niveles, plantilla y diagrama. |
| Plan E7d | Suficiente para hito | Define V1.0-Central, criterio de inclusión, versiones y riesgos. |
| Evidencias privadas | Pendiente operativo | Ya existe plan de evidencias, pero faltan capturas y códigos reales. |
| Verificación técnica I7 | Débil | Debe resolverse con prueba ejecutable o evidencia técnica equivalente en al menos un componente crítico de Central. |
| Evaluación formativa | Pendiente | Debe ejecutarse y producir rediseño documentado. |

## Riesgos metodológicos vigentes

1. **Mezclar línea base e intervención.** El repositorio `.github` y la plantilla ya son intervención; no deben presentarse como línea base.
2. **Confundir instanciación con artefacto.** GitHub, Odoo, `.github` y GitHub Actions son instanciaciones PRX; el artefacto es el marco.
3. **Cerrar evaluación sin rediseño.** Para nivel de maestría se necesita evaluación formativa con ajuste documentado antes de la evaluación sumativa.
4. **Sobreafirmar transferibilidad.** Una evaluación inicial en Central permite generalización analítica prudente, no teoría universal.
5. **Debilidad de I7.** Sin evidencia de verificación técnica, el componente de calidad básica queda vulnerable.

## Plan inmediato recomendado

| Orden | Acción | Archivo o evidencia | Resultado esperado |
|:--|:--|:--|:--|
| 1 | Guardar evidencias privadas prioritarias. | `06_plan_evidencias_privadas.md` y capturas `E-GH-ORG-01`, `E-GH-BASE-*`, `E-ODOO-BASE-*`. | Separación clara entre línea base e intervención. |
| 2 | Completar E7e. | `07e_construccion_verificacion.md`. | Registro de construcción, configuración `.github`, plantilla, aplicación inicial y verificación interna. |
| 3 | Resolver I7. | `E-TEST-BASE-01` y/o `E-TEST-INT-01`. | Evidencia de prueba ejecutable o verificación técnica equivalente. |
| 4 | Preparar E8 formativa. | `08_evaluacion.md`. | Pregunta de evaluación formativa, muestra, criterios y registro de fricciones. |
| 5 | Ejecutar rediseño V1.1-Central. | Actualización de E7c/E7d o bitácora E7e. | Evidencia de aprendizaje, no solo implementación. |
| 6 | Ejecutar evaluación sumativa inicial. | `E-SUM-01` y `08_evaluacion.md`. | Comparación contra línea base. |

## Conclusión de validación

El perfil cumple los requisitos estructurales de una investigación Design Science de maestría: problema de diseño y problema de investigación diferenciados, artefacto como objeto de estudio, tipología declarada, pregunta prescriptiva, criterios definidos antes de construir y contribución prevista como principios de diseño. El borrador del hito también está alineado con DSRM hasta la actividad 3 y con inicio de actividad 4. La tesis todavía no puede reclamar evaluación ni contribución validada; esa afirmación dependerá de ejecutar V1.0-Central, documentar evaluación formativa con rediseño y realizar una evaluación sumativa inicial proporcionada al alcance.
