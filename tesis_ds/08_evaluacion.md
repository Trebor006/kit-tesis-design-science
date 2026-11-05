# E8. Evaluación

## Propósito

Este documento registra el plan y la ejecución de la evaluación del **Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización**. La evaluación distingue dos funciones: demostrar utilidad práctica del artefacto en el contexto de Central y generar evidencia para formular principios de diseño con alcance analítico prudente.

El plan original previó una comparación por período posterior equivalente a la línea base. La ejecución disponible se cerró como una serie acotada de tres cambios, documentada en `08_resultado_sumativo_serie_casos_central.md`. Por tanto, E8 no afirma mejora sostenida ni adopción institucional: afirma aplicabilidad inicial y utilidad trazable en los casos observados.

## Enfoque metodológico de evaluación

La evaluación seguirá una estrategia alineada con FEDS: evaluación de campo formativa seguida de rediseño, y evaluación de campo sumativa inicial. La primera busca aprender si V1.0-Central puede usarse en trabajo real sin fricción excesiva; la segunda busca comparar resultados posteriores contra la línea base.

| Ciclo | Tipo FEDS | Propósito | Estado |
|:--|:--|:--|:--|
| Evaluación formativa | Campo formativa | Observar uso real inicial, fricciones, incumplimientos y necesidad de ajuste del marco. | Ejecutada en `CCC-7336`; ver `08_registro_formativo_CCC-7336.md`. |
| Rediseño | Iteración de diseño | Ajustar reglas, plantilla o comunicación del marco según evidencia formativa. | Ejecutado: V1.1 alinea ramas permanentes con la práctica histórica del contexto. |
| Evaluación sumativa inicial | Campo sumativa | Valorar la utilidad de la iteración V1.0–V1.1 frente a criterios definidos antes de construir. | Ejecutada como serie acotada de tres casos cerrados; ver `08_resultado_sumativo_serie_casos_central.md`. |

La evaluación no se diseñará como encuesta genérica de satisfacción. El artefacto es un marco con reglas, plantillas y estándares; por tanto, debe evaluarse por aplicabilidad, cobertura, coherencia, adopción observable y evidencia producida. La estrategia de un caso instrumental requiere explicitar la unidad de análisis, las fuentes de evidencia y las limitaciones de generalización; Runeson y Höst (2009) respaldan esta disciplina de reporte. Por ello, los registros de Odoo, GitHub, pruebas y entrevistas se triangulan, pero no se interpretan como una muestra estadística de equipos pequeños.

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
| `E-GH-INT-01` | Disponible. | Evidencia de primera solicitud real posterior al marco en `CCC-7336`. |
| `E-GH-INT-02` | Disponible. | Evidencia de fusión y eliminación de rama en `CCC-7336`. |
| `E-GH-INT-03` | Disponible parcialmente. | Evidencia de rama y tres commits conformes de `CCC-7480` en Central API; falta captura del cuarto commit declarado por la solicitud para afirmar conformidad completa. |
| `E-GH-INT-05` | Disponible parcialmente. | Solicitud `CCC-7480` abierta hacia `main` con plantilla completada; `E-TEST-INT-02` acredita pruebas unitarias. Faltan evidencia de construcción, fusión y eliminación de rama. |
| `E-GH-INT-06` | Disponible. | Aplicación posterior en Central Frontend para `CCC-7480`: rama, *commit*, solicitud #27 hacia `main`, fusión y eliminación de rama. La plantilla y verificación se registran en `E-GH-INT-08` y `E-TEST-INT-03`. |
| `E-GH-INT-07` | Disponible. | Aplicación posterior en Central Frontend para `CCC-7477`: *commit*, solicitud #26 fusionada hacia `main` desde rama conforme y eliminación posterior de rama. La plantilla y excepción de verificación se registran en `E-GH-INT-09`. |
| `E-GH-INT-08` | Disponible. | Plantilla completa de `CCC-7480` en Frontend, con método, evidencia de verificación y validación documentada. |
| `E-GH-INT-09` | Disponible. | Plantilla completa de `CCC-7477` en Frontend, con comprobaciones exitosas y excepción técnica explícita de Karma y construcción por permisos de entorno. |
| `E-ODOO-INT-02` | Disponible. | Tarea real posterior `CCC-7480` para implementar pólizas provisionales. |
| `E-ODOO-INT-03` | Disponible. | Tarea real posterior `CCC-7477` para actualizar filtros de la pantalla de contratos. |
| `E-TEST-INT-02` | Disponible. | Ejecución satisfactoria de 182 pruebas unitarias en Central API para el cambio `CCC-7480`; no acredita por sí sola construcción ni despliegue. |
| `E-TEST-INT-03` | Disponible. | Ejecución satisfactoria visible de pruebas Karma de `ContractsComponent`, incluidas pruebas vinculadas con pólizas provisionales de `CCC-7480` en Central Frontend. |
| `E-TEST-INT-01` | Disponible. | Evidencia de verificación técnica en componente crítico para `CCC-7336`. |
| `E-FORM-01` | Disponible. | Evidencia de aplicación formativa y ajuste V1.1. |
| `E-SUM-01` | Disponible como antecedente. | Comparación inicial de caso para `CCC-7336`, posteriormente integrada y acotada por `E-SUM-02`. |

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

## Plan sumativo original y desviación ejecutada

### Pregunta sumativa original

Después del rediseño formativo, ¿V1.1-Central mejora la trazabilidad técnica y la evidencia mínima de verificación frente a la línea base del 21 de septiembre al 4 de octubre de 2026?

### Comparación originalmente esperada

| Indicador | Línea base | Resultado posterior | Estado |
|:--|:--|:--|:--|
| I1. Tareas activas visibles | Parcial. | Tres tareas visibles; validez completa no calculable. | Resultado de caso; ver `E-SUM-02`. |
| I3. Convención documentada de ramas | 0 %. | Tres ramas observables conformes. | Resultado de caso; no tasa de período. |
| I4. Convención documentada de commits | 0 %. | Al menos un commit conforme por caso. | Porcentaje no calculable. |
| I5. Solicitudes de integración | 5/5 observables en GitHub, con advertencia de trabajo no subido. | 3/3 cambios cerrados integrados mediante solicitud. | Alcanzado solo en la serie acotada. |
| I6. Evidencia mínima de verificación | 0/5. | 3/3 solicitudes cerradas con plantilla y evidencia o excepción. | Alcanzado solo en la serie acotada. |
| I7. Verificación técnica en componente crítico | Parcial. | Pruebas API y Frontend documentadas. | Alcanzado. |
| I9. Evidencia trazable de entregables | Parcial. | Cadena trazable en tres casos. | Mejora cualitativa por caso. |

La desviación se documentó antes de formular conclusiones finales: la evidencia no permitió reconstruir un período posterior completo ni denominadores exhaustivos. Por ello, el resultado se reporta como serie de casos y no como comparación de tasas organizacionales.

## Amenazas a la validez

| Amenaza | Riesgo | Mitigación | Impacto residual |
|:--|:--|:--|:--|
| Validez de constructo | Confundir publicación de estándares con adopción real. | Separar evidencias de construcción (`E-ORG-INT-*`) de evidencias de uso real (`E-GH-INT-*`). | Medio: hay tres casos de uso, no adopción sostenida. |
| Validez interna | El tesista influye directamente en el diseño y aplicación. | Documentar decisiones, fricciones y excepciones; usar responsables codificados. | Medio. |
| Validez externa | Evaluación inicial concentrada en Central. | Declarar generalización analítica solo a contextos similares. | Alto si se intenta generalizar demasiado. |
| Validez de conclusión | Pocos casos de uso pueden producir conclusiones débiles. | No usar afirmaciones estadísticas; usar evidencia trazable y análisis cualitativo. | Alto para eficacia sostenida; medio para aplicabilidad inicial. |
| Sesgo post-hoc | Ajustar criterios después de ver resultados. | Mantener criterios definidos en E6 y E7b; documentar ajustes como rediseño. | Bajo si se respeta la trazabilidad. |
| Confidencialidad | Evidencias contienen datos internos. | Mantener capturas privadas y usar códigos en tesis pública. | Bajo si se anonimiza. |

## Estado actual de E8

E8 tiene **evaluación formativa ejecutada y rediseño V1.1 documentado**, seguida por la evaluación de campo sumativa `E-SUM-02`, realizada como serie acotada de tres cambios cerrados de Central. La evaluación conserva los criterios definidos antes de construir; cuando la evidencia no permite calcular un porcentaje completo, el resultado se declara no calculable y no se reemplaza por una estimación favorable.

E8 queda **cerrada con limitación metodológica documentada**. El cambio frente al plan original —medición por período comparable— se explica en `08_resultado_sumativo_serie_casos_central.md`. La evidencia permite afirmar utilidad inicial y aplicabilidad de la cadena de trazabilidad en tres cambios reales, pero no mejora sostenida, adopción institucional ni tasas organizacionales.

## Registro posterior de E-SUM-01

Se registró `08_resultado_sumativo_inicial_CCC-7336.md` como comparación inicial de un caso entre la línea base de Central API y la tarea posterior `CCC-7336`. Posteriormente, las evidencias de `CCC-7480` y `CCC-7477` permitieron consolidar `E-SUM-02` como serie acotada. Este resultado sustituye el estado de “abierto” previo, sin borrar el registro de la desviación respecto al período comparable originalmente planificado.

## Referencias

Runeson, P., & Höst, M. (2009). Guidelines for conducting and reporting case study research in software engineering. *Empirical Software Engineering, 14*(2), 131–164. https://doi.org/10.1007/s10664-008-9102-8
