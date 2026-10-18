# Registro de evaluación formativa — CCC-7336

## Identificación del ciclo

| Campo | Registro |
|:--|:--|
| Código de evaluación formativa | `E-FORM-01` |
| Fecha del ciclo | 2026-10-17 |
| Proyecto | Central |
| Componente | Central API |
| Tarea | `CCC-7336` — Validar pruebas unitarias en API de CCC. |
| Participante codificado | `DEV-003` |
| Versión aplicada | V1.0-Central; ajuste de contexto formalizado como V1.1. |

## Pregunta formativa

¿Puede el marco aplicarse en una tarea real de Central y producir una cadena verificable tarea → rama → commit → solicitud de integración → verificación → fusión, sin fricción operativa desproporcionada?

## Evidencia de aplicación

| Eslabón | Evidencia | Hallazgo factual |
|:--|:--|:--|
| Tarea | `E-ODOO-INT-01` | Existe tarea real `CCC-7336` para validar pruebas unitarias en la API de Central. |
| Rama, título y plantilla | `E-GH-INT-01` | Se creó una solicitud de integración desde `test/CCC-7336-validar-tests-unitarios-api` hacia `main`, con título conforme y plantilla completada. |
| Commits y cierre | `E-GH-INT-02` | La solicitud fue fusionada y la rama temporal fue eliminada después de la integración. |
| Verificación técnica | `E-TEST-INT-01` | Se ejecutaron 169 pruebas unitarias con resultado exitoso en la API. |
| Configuración de ramas permanentes | `E-GH-INT-04` | Se configuraron `main`, `Stage` y `Production`; la rama heredada `master` fue retirada del repositorio intervenido. |

## Resultado formativo

No se reportaron fricciones operativas durante la aplicación de `CCC-7336`: la rama, el commit, la solicitud de integración y la verificación técnica pudieron ejecutarse conforme a las reglas previstas. La captura de la solicitud de integración debe interpretarse como evidencia de creación y llenado de la plantilla; la evidencia final de ejecución de pruebas se respalda específicamente con `E-TEST-INT-01`.

La evaluación detectó un ajuste de contexto, no una falla de uso: la formulación inicial de ramas permanentes en `STD-GIT-001` usaba `stage` y `production` en minúscula, mientras que la configuración histórica predominante revisada por el tesista en repositorios Odoo emplea `Stage` y `Production`. Esta diferencia fue formalizada en `STD-GIT-001` V1.1. La decisión no atribuye la existencia histórica de dichas ramas al artefacto; convierte una práctica previa no institucionalizada en una convención explícita.

## Rediseño V1.1

| Elemento | V1.0 | V1.1 | Justificación |
|:--|:--|:--|:--|
| Rama de validación | `stage` | `Stage` | Alinear el estándar con la configuración histórica predominante observada en repositorios Odoo. |
| Rama de producción | `production` | `Production` | Alinear el estándar con la configuración histórica predominante observada en repositorios Odoo. |
| Tratamiento de ramas heredadas | No explicitado con suficiente precisión. | `master` se declara heredada y se retira solo cuando sea técnicamente seguro. | Evitar renombramientos que rompan automatizaciones o despliegues. |

La evidencia de publicación del rediseño es `E-ORG-INT-06`. La enmienda y sus condiciones de aplicación están documentadas en `07e_STD-GIT-001_enmienda_v1_1.md`.

## Interpretación y límite

El ciclo muestra aplicabilidad inicial del marco en una tarea real de Central y demuestra que es posible producir evidencia de trazabilidad y verificación técnica. No demuestra adopción institucional completa, efectividad sostenida ni mejora sumativa frente a la línea base. Esas afirmaciones requieren `E-SUM-01` y deben limitarse al contexto de Central.

## Decisión de avance

La V1.1 queda lista para evaluación sumativa inicial. La medición posterior deberá usar un periodo definido y comparable con la línea base, registrar denominadores de cada indicador y distinguir cambios observables en GitHub de trabajo no trazado.
