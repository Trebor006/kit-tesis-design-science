# Protocolo de entrevistas y revisión conjunta del diagnóstico — 30 de octubre de 2026

## Propósito

Este protocolo complementa la revisión documental y la observación estructurada realizadas sobre Odoo, GitHub, repositorios y pruebas. Las entrevistas no buscan evaluar rendimiento individual ni confirmar por cortesía el marco propuesto. Su función es triangular hechos no visibles en los registros, especialmente trabajo no registrado, razones de repositorios externos, integración de cambios, verificación y fricciones de uso.

Las respuestas solo se utilizarán con participantes codificados. La tesis pública no incluirá nombres, enlaces privados, nombres de clientes, código, credenciales ni grabaciones.

## Diseño de la técnica

| Elemento | Decisión |
|:--|:--|
| Técnica | Entrevista semiestructurada breve y revisión conjunta de evidencias. |
| Fecha prevista | 30 de octubre de 2026. |
| Duración prevista | 10 a 15 minutos por participante. |
| Participantes | `DEV-001`, `DEV-002` y `DEV-004`; incorporar `DEV-003` únicamente como declaración del tesista y no como fuente independiente de evaluación. |
| Periodo principal consultado | 21 de septiembre al 4 de octubre de 2026, correspondiente a la línea base. |
| Periodo secundario | 17 al 30 de octubre de 2026, solo para contextualizar aplicaciones posteriores; no sustituye la línea base. |
| Medio | Reunión presencial o virtual; grabación únicamente con autorización expresa. |
| Unidad de análisis | Prácticas de gestión técnica y evidencia de cambios, no desempeño de personas. |
| Análisis | Codificación factual por indicador y triangulación con registros documentales y observación. |

## Apertura obligatoria

Antes de iniciar, el tesista debe leer o comunicar lo siguiente:

> Esta entrevista forma parte del diagnóstico de una tesis de maestría. No evalúa su desempeño ni se publicará su nombre. Se consultarán prácticas de registro de tareas, repositorios, ramas, solicitudes de integración y pruebas durante una ventana definida. Puede abstenerse de responder aspectos sensibles. ¿Autoriza que tome notas? Si la reunión se graba, ¿autoriza usar únicamente una síntesis anonimizada y no divulgar el archivo?

El registro debe consignar de forma separada la autorización de notas y la autorización de grabación. Si no existe autorización de grabación, se usarán notas contemporáneas; no se debe grabar ni transcribir material sin consentimiento.

## Guion de preguntas y relación con indicadores

| Código | Pregunta | Indicadores | Evidencia complementaria requerida |
|:--|:--|:--|:--|
| P1 | Durante la ventana del 21 de septiembre al 4 de octubre, ¿qué trabajo técnico realizó o conoció que no estuvo registrado en Odoo? | I1, I9 | Tarea, mensaje, bitácora o declaración fechada. |
| P2 | ¿Qué repositorio se utilizó para ese componente y por qué su ubicación era institucional, externa o una excepción? | I2 | Vista de repositorio, configuración o declaración de restricción. |
| P3 | ¿Cómo se nombraban ramas y *commits* antes del estándar? ¿Existía una regla documentada? | I3, I4 | Historial Git o solicitud de integración. |
| P4 | ¿Los cambios se integraban mediante solicitud de integración, fusión directa u otro mecanismo? ¿Qué razón práctica lo explica? | I5 | Solicitud, historial de fusión o declaración contrastable. |
| P5 | ¿Qué evidencia de prueba o verificación se registraba antes de integrar cambios? | I6, I7 | Resultado de prueba, construcción, comentario o ausencia verificable. |
| P6 | ¿Qué dificultad concreta encontraba al registrar tareas, usar ramas, crear solicitudes o adjuntar evidencias? | I1, I3, I4, I5, I6 | Ejemplo factual; no solicitar valoración personal genérica. |
| P7 | ¿Hubo corrección urgente, defecto o entrega difícil de respaldar durante la ventana? | I8, I9 | Ticket, solicitud, mensaje o declaración codificada. |
| P8 | Después de conocer el marco, ¿qué regla resulta clara, ambigua o inaplicable en su componente? | Aplicabilidad y rediseño | Ejemplo de aplicación o excepción; clasificarlo como evidencia posterior, no como línea base. |

## Guion recomendado para la conversación

No se debe pedir a los desarrolladores que reconstruyan capturas, enumeren tareas antiguas ni “produzcan evidencia” durante la entrevista. La revisión documental ya cubre Odoo, GitHub, ramas, *commits*, solicitudes y pruebas. La entrevista debe recuperar la práctica habitual y explicar las causas de los hallazgos observados.

1. **Antes de los estándares publicados, cuando iniciaba un cambio, ¿cómo acostumbraba crear una rama y escribir los *commits*? ¿Existía alguna convención escrita que todos debían seguir?**
2. **Cuando terminaba un cambio, ¿cómo acostumbraba integrarlo: solicitud de integración, fusión directa u otro mecanismo? ¿Quién verificaba el cambio?**
3. **Antes de integrar, ¿qué prueba o comprobación solía realizar y dónde quedaba registrada esa evidencia?**
4. **¿Qué restricción técnica u organizativa dificultaba aplicar una práctica común de Git, solicitudes de integración o repositorios institucionales?**
5. **Después de conocer las reglas del marco, ¿qué parte pudo aplicar con claridad y qué parte requeriría una excepción o ajuste?**

Si un participante menciona una tarea, solicitud o cambio específico espontáneamente, se podrá pedir su código o fecha para contrastarlo; no se debe exigir que busque evidencias en la reunión.

## Regla de registro temporal

Cada respuesta debe diferenciar tres fechas:

1. **Fecha de entrevista:** 30 de octubre de 2026 o fecha real de ejecución.
2. **Fecha del hecho informado:** fecha o ventana a la que se refiere la respuesta.
3. **Momento metodológico:** línea base, intervención, evaluación formativa o evaluación posterior.

Una entrevista posterior puede informar un hecho de línea base, pero no transforma la entrevista en evidencia generada antes de la intervención. Esta distinción debe aparecer en la ficha de cada participante.

## Criterio de triangulación

| Resultado de contraste | Tratamiento en la tesis |
|:--|:--|
| La entrevista coincide con Odoo o GitHub | Registrar como hallazgo triangulado. |
| La entrevista describe trabajo no visible en herramientas | Registrar como hallazgo de trazabilidad incompleta, con fuente codificada. |
| La entrevista contradice un registro documental | Declarar discrepancia y analizar su causa; no escoger una versión por intuición. |
| La respuesta no aporta fecha, ejemplo ni evidencia contrastable | Conservarla solo como percepción contextual; no usarla para calcular indicadores. |

## Productos esperados después de cada entrevista

1. Una ficha codificada en `06_registros_entrevistas_diagnostico_2026-10-30.md`.
2. Un código de evidencia `E-INT-BASE-*` o `E-INT-POST-*`, según el momento del hecho informado.
3. Una síntesis factual de máximo 150 palabras por participante.
4. Una matriz de triangulación que relacione respuesta, indicador y evidencia documental.

## Criterio de cierre

La técnica se considerará aplicada cuando existan al menos dos fichas codificadas con fecha, consentimiento de notas, respuestas factuales y relación explícita con indicadores. La ausencia de respuestas o evidencia adicional será un resultado metodológico que debe declararse, no una razón para inventar hallazgos.
