# Registros de entrevistas y revisión conjunta del diagnóstico — actualización del 29 de octubre de 2026

## Instrucción de uso

Este archivo se completa inmediatamente después de cada entrevista real. No contiene resultados anticipados. Cada síntesis debe separar lo declarado por el participante de lo observado documentalmente y debe usar únicamente los códigos `DEV-001`, `DEV-002`, `DEV-003` y `DEV-004`.

## Ficha de registro — DEV-001

| Campo | Registro a completar después de la entrevista |
|:--|:--|
| Fecha y hora real | 29 de octubre de 2026, 08:30. |
| Modalidad | Videollamada remota. |
| Autorización de notas | Sí, autorizada. |
| Autorización de grabación | No realizada. |
| Ventana del hecho informado | Prácticas habituales anteriores a la publicación de los estándares del marco; la fecha exacta de inicio de esa ventana deberá recuperarse del registro de publicación. |
| Componente tratado | Central Odoo Backend. |
| Código de evidencia asociado | `E-INT-BASE-01`. |
| Respuestas factuales P1–P5 | Registradas en la tabla de respuestas. |
| Indicadores informados | I2, I3, I4, I5, I6 y aplicabilidad del marco. |
| Evidencia documental que coincide o contradice | `E-GH-BASE-02`, `E-GH-BASE-03` y `E-GH-BASE-04` respaldan ramas con códigos de tarea, solicitudes fusionadas y mensajes de *commit* previos; no acreditan revisión independiente ni verificación técnica. |
| Clasificación temporal | Línea base retrospectiva declarada por participante. |
| Limitación o dato no verificable | La entrevista no prueba por sí misma creación de ramas, solicitudes de integración, revisiones o verificación; la revisión propia no equivale a revisión independiente. |

## Ficha de registro — DEV-002

| Campo | Registro a completar después de la entrevista |
|:--|:--|
| Fecha y hora real | 29 de octubre de 2026, 09:00. |
| Modalidad | Videollamada remota. |
| Autorización de notas | Sí, autorizada. |
| Autorización de grabación | No realizada. |
| Ventana del hecho informado | Prácticas habituales anteriores a la publicación de los estándares del marco; la fecha exacta de inicio de esa ventana deberá recuperarse del registro de publicación. |
| Componente tratado | Central API. |
| Código de evidencia asociado | `E-INT-BASE-02`. |
| Respuestas factuales P1–P5 | Registradas en la tabla de respuestas. |
| Indicadores informados | I2, I3, I4, I5, I6 y aplicabilidad del marco. |
| Evidencia documental que coincide o contradice | Pendiente de contraste con GitHub institucional, historial del repositorio y evidencia de migración. |
| Clasificación temporal | Línea base retrospectiva declarada por participante. |
| Limitación o dato no verificable | La entrevista no prueba por sí misma ausencia total de Git ni los cambios posteriores; el aprendizaje informado no demuestra adopción sostenida. |

## Ficha de registro — DEV-004

| Campo | Registro a completar después de la entrevista |
|:--|:--|
| Fecha y hora real |  |
| Modalidad |  |
| Autorización de notas |  |
| Autorización de grabación |  |
| Ventana del hecho informado |  |
| Componente tratado |  |
| Código de evidencia asociado |  |
| Respuestas factuales P1–P5 |  |

## Registro breve de respuestas por pregunta

Use esta tabla después de cada entrevista. Registre una síntesis factual, no interpretaciones del tesista. Si una respuesta no incluye fecha, ejemplo o práctica verificable, señálela como percepción contextual.

| Código | Pregunta | Síntesis factual | Indicador | Evidencia o contraste posterior |
|:--|:--|:--|:--|:--|
| `DEV-001` / P1 | Práctica habitual de ramas y *commits* antes del estándar. | Declaró que creaba ramas con el código de la tarea, sin utilizar una convención escrita. | I3, I4 | `E-GH-BASE-02` muestra ramas activas `CCC-5253`, `CCC-5295` y `CCC-5267`; `E-GH-BASE-04` muestra la rama `CCC-5253`. Los mensajes observados usan tipo y alcance técnico, sin código de tarea visible. |
| `DEV-001` / P2 | Integración de cambios y validación habitual. | Declaró que, para pruebas en `Stage`, trabajaba directamente en una rama de prueba y creaba solicitudes de integración; al ser el único desarrollador, revisaba sus propios cambios. | I5, I6 | `E-GH-BASE-03` muestra 10 solicitudes cerradas y fusionadas. No muestra aprobaciones de otra persona ni evidencia de revisión independiente. |
| `DEV-001` / P3 | Pruebas o comprobaciones previas y registro de evidencia. | Declaró realizar pruebas manuales de funcionalidad en ambiente de pruebas; indicó que la revisión posterior de gerencia no siempre ocurría. No declaró un registro técnico persistente de esa evidencia. | I6, I7 | Las tres capturas recibidas no muestran resultados de pruebas, construcción ni comentarios de validación; la declaración continúa sin contraste técnico. |
| `DEV-001` / P4 | Restricción para repositorios institucionales, Git o solicitudes. | No identificó una restricción técnica personal para usar Git. Atribuyó la heterogeneidad de nombres de repositorios a creaciones en Odoo.sh realizadas por responsables no programadores y a la ausencia de estándar. | I2, I3, I5 | `E-GH-BASE-02` muestra `main`, `Stage` y `Production`, pero no permite atribuir sus nombres a una causa organizativa concreta. |
| `DEV-001` / P5 | Claridad, excepción o ajuste requerido después de conocer el marco. | Declaró que crear ramas y *commits* conforme a las reglas le resulta claro; señaló que usa una herramienta de asistencia al desarrollo. No informó una excepción requerida. | Aplicabilidad y rediseño | Percepción de aplicabilidad; no prueba uso sostenido ni adopción organizacional. |
| `DEV-002` / P1 | Práctica habitual de ramas y *commits* antes del estándar. | Declaró ser nuevo en Git y que, para realizar cambios, duplicaba carpetas o proyectos; no reportó una convención escrita. | I3, I4 | `E-GH-BASE-06` muestra que Central API ya tenía historial Git desde 2025 y eventos en 2026. La captura no confirma ni contradice la práctica personal declarada de `DEV-002`; impide presentar el proyecto como totalmente ajeno a Git. |
| `DEV-002` / P2 | Integración de cambios y validación habitual. | Declaró que no utilizaba Git ni solicitudes de integración; revisaba sus propios cambios y realizaba el despliegue. | I5, I6 | `E-GH-BASE-06` acredita historial de *commits*, pero no muestra solicitudes de integración, autores codificados ni despliegues. La declaración personal continúa sin contraste directo. |
| `DEV-002` / P3 | Pruebas o comprobaciones previas y registro de evidencia. | Declaró que efectuaba pruebas manuales y que no existía evidencia registrada. | I6, I7 | Pendiente de contraste con pruebas y solicitudes históricas. |
| `DEV-002` / P4 | Restricción para repositorios institucionales, Git o solicitudes. | No identificó una restricción formal; relacionó la ausencia previa de Git con trabajo individual en proyectos legados. Declaró que los proyectos se están organizando y subiendo al GitHub de la organización. | I2, I3, I5 | La migración declarada requiere contraste con GitHub; no debe asumirse como adopción consolidada. |
| `DEV-002` / P5 | Claridad, excepción o ajuste requerido después de conocer el marco. | Declaró encontrarse en aprendizaje y crear ramas y *commits* con apoyo de `DEV-003`; cuando requiere guía, solicita una reunión. | Aplicabilidad y rediseño | Percepción de aprendizaje asistido; no demuestra aplicación autónoma ni sostenida. |

## Matriz de triangulación posterior a las entrevistas

| Participante | Hecho declarado | Indicador | Evidencia documental | Resultado de contraste | Uso autorizado en diagnóstico |
|:--|:--|:--|:--|:--|:--|
| `DEV-001` | Ausencia de convención escrita; ramas con códigos de tarea; auto-revisión y pruebas manuales en ambiente de pruebas. | I3, I4, I5, I6, I7 | `E-GH-BASE-02` a `E-GH-BASE-04`, capturadas el 29 de octubre de 2026 a las 09:30, respaldan ramas, *commits* y solicitudes previas. Falta evidencia de pruebas y revisión independiente. | Coincidencia parcial: las ramas contienen códigos de tarea y existen solicitudes fusionadas; los mensajes de *commit* observados no incluyen el código de tarea. | Sí, como declaración retrospectiva y contraste parcial; no como adopción del marco. |
| `DEV-002` | Práctica personal declarada sin Git ni solicitudes de integración; pruebas manuales sin evidencia registrada; migración organizacional en curso declarada. | I2, I3, I4, I5, I6, I7 | `E-GH-BASE-06` confirma que Central API tenía historial Git desde 2025, pero no identifica prácticas de `DEV-002`. Faltan solicitudes, pruebas y evidencia de migración. | Contraste parcial: existe historial Git previo, por lo que no se afirmará ausencia total de Git en el proyecto; la práctica personal sigue siendo declaración retrospectiva. | Sí, como declaración retrospectiva y contraste parcial; no como adopción del marco. |
| `DEV-004` |  |  |  |  |  |
