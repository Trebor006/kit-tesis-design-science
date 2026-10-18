# E8. Evaluación

## Propósito

Este documento planifica la evaluación del **Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización**. La evaluación distingue dos funciones: demostrar utilidad práctica del artefacto en el contexto de Central y generar evidencia suficiente para formular principios de diseño con alcance analítico prudente.

En el estado actual, E8 se redacta como **plan de evaluación y estructura de resultados pendientes**. No se declara evaluación ejecutada todavía, porque aún faltan dos evidencias críticas: una solicitud de integración real posterior al marco (`E-GH-INT-01`) y una verificación técnica en un componente crítico (`E-TEST-INT-01`). Esta distinción protege la tesis contra el error de presentar construcción documental como evaluación de campo.

## Enfoque metodológico de evaluación

La evaluación seguirá una estrategia alineada con FEDS: evaluación de campo formativa seguida de rediseño, y evaluación de campo sumativa inicial. La primera busca aprender si V1.0-Central puede usarse en trabajo real sin fricción excesiva; la segunda busca comparar resultados posteriores contra la línea base.

| Ciclo | Tipo FEDS | Propósito | Estado |
|:--|:--|:--|:--|
| Evaluación formativa | Campo formativa | Observar uso real inicial, fricciones, incumplimientos y necesidad de ajuste del marco. | Ejecutada en `CCC-7336`; ver `08_registro_formativo_CCC-7336.md`. |
| Rediseño | Iteración de diseño | Ajustar reglas, plantilla o comunicación del marco según evidencia formativa. | Ejecutado: V1.1 alinea ramas permanentes con la práctica histórica del contexto. |
| Evaluación sumativa inicial | Campo sumativa | Comparar resultados posteriores contra línea base con criterios definidos antes de construir. | Pendiente. |

La evaluación no se diseñará como encuesta genérica de satisfacción. El artefacto es un marco con reglas, plantillas y estándares; por tanto, debe evaluarse por aplicabilidad, cobertura, coherencia, adopción observable y evidencia producida.

## Contexto y muestra de evaluación

La evaluación inicial se concentra en el proyecto **Central**, porque contiene tres componentes técnicos y tres responsables diferenciados.

| Componente | Responsable codificado | Rol esperado en evaluación |
|:--|:--|:--|
| Central Odoo Backend | DEV-001 | Aplicación del marco en componente Odoo si existe cambio disponible. |
| Central API | DEV-002 | Aplicación del marco en cambio de API o verificación técnica. |
| Central Frontend | DEV-003 | Aplicación del marco en cambio frontend y registro de fricciones. |

Ansular y PConst quedan como evidencia diagnóstica y contexto comparativo, no como foco principal de evaluación. Esta delimitación evita sobrealcance y mantiene coherencia con la matriz de la tesis.

## Criterios de éxito definidos antes de evaluación

Los criterios se derivan de E6 y E7b, no de resultados observados después. Cualquier ajuste posterior deberá documentarse como rediseño y no como corrección retroactiva de la línea base.

| Dimensión | Indicador | Criterio esperado | Evidencia principal |
|:--|:--|:--|:--|
| Visibilidad del trabajo | I1. Tareas activas visibles y válidas. | ≥ 80 % de tareas activas visibles y válidas. | Odoo o herramienta equivalente. |
| Repositorio y gobernanza | I2. Componentes críticos con repositorio institucional o excepción. | 100 % de componentes críticos con repositorio o excepción documentada. | GitHub; ficha de componente. |
| Trazabilidad de ramas | I3. Ramas conformes. | ≥ 80 % de ramas conformes con la convención. | GitHub. |
| Trazabilidad de commits | I4. Commits conformes. | ≥ 80 % de commits conformes con la convención. | GitHub. |
| Integración de cambios | I5. Cambios mediante solicitud de integración. | ≥ 70 % de cambios integrados por solicitud. | GitHub. |
| Evidencia de verificación | I6. Solicitudes con evidencia mínima. | ≥ 70 % de solicitudes con evidencia mínima de verificación. | Plantilla PR; capturas; resultados. |
| Verificación técnica | I7. Componente crítico con prueba o evidencia técnica. | Al menos un componente crítico con evidencia técnica ejecutada o equivalente justificada. | `E-TEST-INT-01`. |
| Trazabilidad de entregables | I9. Cadena trazable de evidencia. | Mejora cualitativa documentada en tarea → rama → commit → PR → evidencia. | Matriz de trazabilidad. |

## Evidencias necesarias para ejecutar E8

| Código | Estado | Función en la evaluación |
|:--|:--|:--|
| `E-ORG-INT-01` | Disponible. | Evidencia construcción de estándar de ramas. |
| `E-ORG-INT-02` | Disponible. | Evidencia construcción de plantilla operativa PR. |
| `E-ORG-INT-03` | Disponible. | Evidencia construcción de estándar de solicitudes de integración. |
| `E-ORG-INT-04` | Disponible. | Evidencia construcción de estándar de commits. |
| `E-ORG-INT-05` | Disponible. | Evidencia organización documental de productos operativos. |
| `E-GH-ORG-01` | Disponible. | Evidencia instanciación técnica inicial en repositorio `.github`. |
| `E-GH-INT-01` | Pendiente. | Evidencia de primera solicitud real posterior al marco. |
| `E-GH-INT-02` | Pendiente opcional. | Evidencia de plantilla PR completada en un cambio real. |
| `E-GH-INT-03` | Pendiente opcional. | Evidencia de commits con convención en cambio real. |
| `E-TEST-INT-01` | Pendiente. | Evidencia de verificación técnica en componente crítico. |
| `E-FORM-01` | Pendiente. | Evidencia de fricciones y ajustes formativos. |
| `E-SUM-01` | Pendiente. | Evidencia de medición posterior comparada contra línea base. |

## Resultado de evaluación formativa ejecutada

La primera aplicación se ejecutó en la tarea real `CCC-7336` de Central API. La evidencia muestra tarea registrada, rama temporal conforme, commit con código de tarea, solicitud de integración con plantilla, fusión, eliminación de rama y 169 pruebas unitarias exitosas. No se reportaron fricciones operativas durante el uso del flujo.

El rediseño V1.1 no responde a una falla de la tarea, sino a un ajuste contextual identificado al contrastar el estándar V1.0 con la configuración histórica de repositorios Odoo: `Stage` y `Production` se formalizaron con mayúscula como convención institucional vigente. El registro completo y sus límites se encuentran en `08_registro_formativo_CCC-7336.md`.

## Evaluación formativa planificada

### Pregunta formativa

¿Puede V1.0-Central aplicarse en un cambio real de Central y producir evidencia mínima de trazabilidad y verificación sin introducir una carga operativa desproporcionada?

### Procedimiento

1. Seleccionar una tarea pequeña y verificable de Central.
2. Crear una rama temporal siguiendo `STD-GIT-001`.
3. Realizar uno o más commits siguiendo `STD-GIT-003`.
4. Crear una solicitud de integración con título según `STD-GIT-002`.
5. Completar la plantilla operativa de solicitud de integración.
6. Registrar verificación técnica mínima.
7. Registrar validación o excepción.
8. Documentar fricciones, desviaciones y ajustes necesarios.

### Evidencias esperadas

| Evidencia | Qué debe mostrar |
|:--|:--|
| `E-GH-INT-01` | Rama, solicitud de integración y relación con tarea real de Central. |
| `E-GH-INT-02` | Plantilla PR completada con tarea, resumen, riesgo, verificación y validación. |
| `E-GH-INT-03` | Commits con formato y código de tarea. |
| `E-TEST-INT-01` | Resultado de prueba, construcción, prueba de API o verificación manual documentada. |
| `E-FORM-01` | Fricciones observadas y cambios propuestos. |

### Criterio de rediseño

Se debe generar V1.1-Central si aparece cualquiera de estas situaciones:

- el formato de rama o commit se comprende parcialmente;
- la plantilla PR resulta demasiado extensa o ambigua;
- el responsable no sabe qué evidencia de verificación adjuntar;
- la auto-validación se confunde con revisión independiente;
- el flujo requiere una excepción no prevista.

La fricción ya observada en `E-GH-ORG-01`, donde la rama `config/ADM-4940_config_pr_template` usó guion bajo en la descripción, anticipa un ajuste comunicacional: reforzar que la descripción corta debe separarse con guiones.

## Evaluación sumativa inicial planificada

### Pregunta sumativa

Después del rediseño formativo, ¿V1.1-Central mejora la trazabilidad técnica y la evidencia mínima de verificación frente a la línea base del 21 de septiembre al 4 de octubre de 2026?

### Comparación esperada

| Indicador | Línea base | Resultado posterior | Estado |
|:--|:--|:--|:--|
| I1. Tareas activas visibles | Parcial. | Pendiente. | Pendiente. |
| I3. Convención documentada de ramas | 0 %. | Pendiente. | Pendiente. |
| I4. Convención documentada de commits | 0 %. | Pendiente. | Pendiente. |
| I5. Solicitudes de integración | 5/5 observables en GitHub, con advertencia de trabajo no subido. | Pendiente. | Pendiente. |
| I6. Evidencia mínima de verificación | 0/5. | Pendiente. | Pendiente. |
| I7. Verificación técnica en componente crítico | Parcial. | Pendiente. | Pendiente. |
| I9. Evidencia trazable de entregables | Parcial. | Pendiente. | Pendiente. |

La evaluación sumativa inicial no reclamará transformación completa de PRX. Su alcance será demostrar mejora observable en Central y derivar principios de diseño proporcionales a esa evidencia.

## Amenazas a la validez

| Amenaza | Riesgo | Mitigación | Impacto residual |
|:--|:--|:--|:--|
| Validez de constructo | Confundir publicación de estándares con adopción real. | Separar evidencias de construcción (`E-ORG-INT-*`) de evidencias de uso real (`E-GH-INT-*`). | Medio hasta obtener PR real. |
| Validez interna | El tesista influye directamente en el diseño y aplicación. | Documentar decisiones, fricciones y excepciones; usar responsables codificados. | Medio. |
| Validez externa | Evaluación inicial concentrada en Central. | Declarar generalización analítica solo a contextos similares. | Alto si se intenta generalizar demasiado. |
| Validez de conclusión | Pocos casos de uso pueden producir conclusiones débiles. | No usar afirmaciones estadísticas; usar evidencia trazable y análisis cualitativo. | Medio. |
| Sesgo post-hoc | Ajustar criterios después de ver resultados. | Mantener criterios definidos en E6 y E7b; documentar ajustes como rediseño. | Bajo si se respeta la trazabilidad. |
| Confidencialidad | Evidencias contienen datos internos. | Mantener capturas privadas y usar códigos en tesis pública. | Bajo si se anonimiza. |

## Estado actual de E8

E8 tiene **evaluación formativa ejecutada y rediseño V1.1 documentado**. No queda cerrada porque falta la evaluación sumativa inicial `E-SUM-01`: una comparación posterior predefinida contra la línea base. Hasta contar con esa comparación, no se deben declarar mejora sostenida ni principios de diseño validados.
