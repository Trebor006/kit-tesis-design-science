# E7b. Requisitos del artefacto

## Propósito

Este documento define los requisitos del **Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización**. Los requisitos se derivan de la línea base consolidada en E6 y delimitan qué debe contener el artefacto para ser aplicable inicialmente en el proyecto Central de PRX.

## Alcance de aplicación inicial

La primera versión del marco se aplicará inicialmente en el proyecto **Central**, porque permite observar coordinación entre tres componentes y tres responsables técnicos diferenciados.

| Componente | Tecnología | Responsable codificado | Rol en la evaluación inicial |
|:--|:--|:--|:--|
| Central Odoo Backend | Python - Odoo | DEV-001 | Componente backend Odoo. |
| Central API | C# | DEV-002 | Componente API. |
| Central Frontend | Angular - TypeScript | DEV-003 | Componente frontend. |

Ansular y PConst se conservarán como evidencia diagnóstica y contexto comparativo, pero no serán el foco principal de la primera aplicación del marco.

## Requisitos del artefacto

| Código | Propiedad requerida | Tipo | Métrica o criterio de cumplimiento | Fuente en el problema | Prioridad |
|:--|:--|:--|:--|:--|:--|
| RQ1 | Definir precondiciones y gobernanza mínima. | Contextual | El marco debe identificar repositorio oficial o excepción documentada, mecanismo de gestión de tareas, responsable técnico y mecanismo de excepción. | Repositorios dispersos, componentes fuera de PRX y responsabilidades implícitas. | Alta |
| RQ2 | Definir tarea válida. | Funcional | Una tarea válida debe tener descripción, responsable, componente afectado, criterio de aceptación, estado y criterio de terminado. | Tickets demasiado grandes y visibilidad parcial en Odoo. | Alta |
| RQ3 | Definir criterio de división de tareas. | Funcional | Una tarea debe dividirse cuando agrupa objetivos independientes, afecta componentes distintos, no puede verificarse como unidad o excede el ciclo acordado. | Caso PConst con un ticket amplio que agrupó backend, frontend, AWS S3, pruebas y configuración. | Alta |
| RQ4 | Definir repositorio oficial o excepción documentada. | Contextual | Cada componente debe clasificarse como institucional, cliente, tercero o excepción documentada. | Solo 3 de 7 componentes estaban en GitHub institucional durante la línea base. | Alta |
| RQ5 | Definir convención mínima de ramas. | Funcional | Toda rama de trabajo debe seguir el formato `<tipo>/<codigo-tarea>-<descripcion-corta>`, por ejemplo `feat/CCC-4407-operador-contrato`. | 0 % de convención documentada de ramas. | Alta |
| RQ5.1 | Definir ramas permanentes oficiales por repositorio. | Contextual | Cada repositorio debe declarar rama por defecto, rama de validación y rama de producción si aplica. Estándar objetivo PRX: `main`, `stage` y `production` solo cuando corresponda. | Evidencia de nombres heterogéneos, ausencia de `stage` o `production` en algunos repositorios y variación de rama por defecto entre `main` y `Production`. | Alta |
| RQ6 | Definir convención mínima de commits. | Funcional | Todo commit relevante debe seguir el formato `<tipo>(<codigo-tarea>): <descripcion breve>`, por ejemplo `feat(CCC-4407): agregar datos del operador en contratos`. | 0 % de convención documentada de commits. | Alta |
| RQ6.1 | Definir flujo de ramificación ligero. | Funcional | El marco debe adoptar un flujo basado en tronco inspirado en *Trunk-Based Development*, con ramas cortas por tarea y sin ramas de larga duración innecesarias. | Equipos pequeños, baja estandarización y riesgo de sobrecarga si se adopta GitFlow. | Alta |
| RQ7 | Definir solicitud de integración válida. | Funcional | Una solicitud válida debe incluir tarea relacionada, descripción del cambio, componentes afectados, tipo de cambio, riesgo, evidencia mínima y estado de validación. | Solicitudes fusionadas sin evidencia mínima de verificación. | Alta |
| RQ8 | Distinguir integración trazable de revisión independiente. | Funcional | El marco debe registrar si la solicitud fue auto-validada, validada automáticamente o revisada por una persona distinta del autor. | No existe revisión independiente como práctica institucional observable. | Alta |
| RQ9 | Definir validación progresiva. | Funcional | El marco debe permitir solicitud trazable, plantilla completa, evidencia mínima, validación documentada y revisión por tercero cuando sea factible. | Componentes con un solo desarrollador y ausencia de revisión por pares. | Alta |
| RQ10 | Diferenciar método de verificación y evidencia de verificación. | Funcional | Cada cambio funcional debe declarar qué se verificó, cómo se verificó y qué evidencia lo respalda. | 0 de 5 solicitudes con evidencia mínima de verificación. | Alta |
| RQ11 | Definir prueba mínima para componentes críticos. | Funcional | Al menos un componente crítico del proyecto Central debe tener prueba unitaria ejecutable o evidencia técnica equivalente justificada. | Pruebas unitarias parciales y no institucionalizadas. | Media |
| RQ12 | Registrar entrega y configuración básica. | Contextual | Cada entrega relevante debe registrar ambiente, rama o versión, responsable, fecha y mecanismo de despliegue. | Diferencias entre `test`, `Stage`, producción y despliegues no homogéneos. | Media |
| RQ13 | Medir adopción del marco. | Evaluación | El marco debe incluir indicadores para visibilidad, trazabilidad, solicitudes válidas, verificación y entrega trazable. | Necesidad de comparar línea base con evaluación posterior. | Alta |
| RQ14 | Mantener agnosticismo de herramienta. | Contextual | El marco debe definir qué debe existir, no imponer Odoo o GitHub como única herramienta posible. | Odoo y GitHub son instanciaciones de PRX, no definición formal del artefacto. | Alta |

## Tensiones y decisiones de priorización

| Tensión | Decisión de diseño |
|:--|:--|
| Ligereza frente a control. | La primera versión exigirá evidencia mínima verificable, no automatización completa ni proceso pesado. |
| Revisión independiente frente a disponibilidad real. | La revisión por tercero se incorporará progresivamente; si solo hay un desarrollador, se permitirá auto-validación documentada como excepción explícita. |
| Estandarización frente a agnosticismo de herramienta. | Se documentará la regla general y luego su instanciación en PRX con Odoo y GitHub. |
| Alcance amplio frente a factibilidad. | La primera aplicación se concentrará en Central; Ansular y PConst quedan como evidencia diagnóstica y contexto comparativo. |
| Pruebas unitarias frente a evidencia mínima. | Las pruebas unitarias serán exigidas en componentes críticos, pero la verificación básica también podrá admitir prueba manual documentada, registro de ejecución o evidencia técnica justificada según tipo de cambio. |

## Trazabilidad requisito → evidencia de línea base

| Requisito | Evidencia que lo justifica |
|:--|:--|
| RQ1, RQ4 | Componentes fuera de GitHub institucional y casos de repositorios en cuenta personal u otra organización. |
| RQ2, RQ3 | Ticket amplio de PConst y visibilidad incompleta en componentes Odoo. |
| RQ5, RQ6 | Ausencia de convención documentada de ramas y commits. |
| RQ5.1 | Variación observada en nombres de ramas permanentes y de validación; ausencia de `stage` o `production` en algunos repositorios; rama por defecto no homogénea. |
| RQ6.1 | Necesidad de evitar ramas largas y sobrecarga operativa en equipos pequeños; diferencias actuales entre `test`, `Stage` y ramas históricas de proyecto. |
| RQ7, RQ10 | 5 solicitudes fusionadas y 0 con evidencia mínima de verificación. |
| RQ8, RQ9 | Solicitudes creadas/fusionadas sin práctica institucional de revisión independiente. |
| RQ11 | Evidencia parcial de pruebas en PConst y necesidad de verificar componentes críticos en Central. |
| RQ12 | Diferencias entre ramas o ambientes `test`, `Stage` y `Production`. |
| RQ13 | Necesidad de comparar línea base con evaluación posterior. |
| RQ14 | Decisión de separar definición formal del marco e instanciación PRX. |

## Definiciones operativas iniciales para trazabilidad técnica

La convención de ramas y commits se inspira en Angular y Conventional Commits, pero se adapta a PRX para priorizar trazabilidad con la tarea. La decisión no se justifica por estética del historial, sino porque permite seguir la relación entre tarea, rama, commit y solicitud de integración.

El flujo de ramificación del marco será un **flujo basado en tronco**, inspirado en *Trunk-Based Development* —desarrollo basado en tronco—. Esta decisión significa que el marco evitará ramas largas y modelos de ramificación pesados como GitFlow. Para equipos pequeños con baja estandarización, el principio operativo será trabajar con ramas cortas vinculadas a tareas, integrarlas mediante solicitud de integración y eliminarlas después de la fusión. Las ramas permanentes se limitarán a las necesarias para estabilidad y validación, como `main` y `stage` o `test`, según la instanciación de cada proyecto.

### Convención de ramas

El marco distinguirá entre **ramas permanentes** y **ramas temporales de trabajo**. Las ramas permanentes representan estados del producto o ambientes de validación; las ramas temporales representan trabajo asociado a una tarea.

Para ramas permanentes, cada repositorio deberá declarar cuáles son sus ramas oficiales y qué significa cada una. En la instanciación PRX se propone como estándar objetivo: `main` como rama por defecto y tronco de integración; `stage` como rama de validación cuando exista ambiente de pruebas; y `production` como rama de producción solo cuando el mecanismo de despliegue lo requiera. La primera versión del marco no exigirá renombrar de inmediato ramas históricas si eso genera riesgo técnico. En cambio, exigirá documentar la equivalencia y planificar la normalización.

Ejemplo:

| Rama existente | Significado declarado | Acción |
|:--|:--|:--|
| `Production` | Producción | Mantener temporalmente y documentar. |
| `Stage` | Validación | Mantener temporalmente y documentar. |
| `test` | Validación del frontend | Documentar como equivalente de validación. |

Para ramas temporales de trabajo se usará la siguiente convención.

Formato:

```text
<tipo>/<codigo-tarea>-<descripcion-corta>
```

Ejemplos:

```text
feat/CCC-4407-operador-contrato
fix/CCC-4900-aviso-cancelacion
hotfix/CCC-4912-error-produccion
config/CCC-4420-ajustar-variables-entorno
test/CCC-4430-pruebas-contratos
docs/CCC-4431-actualizar-readme
refactor/CCC-4432-separar-servicio-contratos
```

Tipos permitidos inicialmente:

| Tipo | Uso |
|:--|:--|
| `feat` | Nueva funcionalidad. |
| `fix` | Corrección normal. |
| `hotfix` | Corrección urgente en producción. |
| `config` | Configuración, variables o ajustes de despliegue. |
| `test` | Pruebas. |
| `docs` | Documentación. |
| `refactor` | Mejora interna sin cambio funcional esperado. |

### Convención de commits

Formato:

```text
<tipo>(<codigo-tarea>): <descripcion breve>
```

Ejemplos:

```text
feat(CCC-4407): agregar datos del operador en contratos
fix(CCC-4900): corregir creación de avisos de cancelación
test(CCC-4430): agregar pruebas de validación de contrato
config(CCC-4420): ajustar variables de entorno para stage
```

El código de tarea debe aparecer en la rama, en los commits relevantes y en la solicitud de integración. Al fusionar una solicitud de integración, se recomienda usar `squash merge` para conservar un historial integrado más limpio, siempre que el mensaje final del `squash` conserve el código de tarea. Después de fusionar, la rama de trabajo debe eliminarse para evitar ramas obsoletas.

### Regla de trazabilidad mínima

Una cadena de trazabilidad técnica mínima queda completa cuando puede observarse:

```text
tarea → rama → commit → solicitud de integración → evidencia de verificación
```

Si alguno de estos eslabones no aplica o no existe, debe registrarse la excepción de forma explícita.

## Estado del gate E7b

E7b queda **suficiente para el hito**. Los requisitos son trazables a la línea base y al problema de diseño, cada propiedad tiene criterio de cumplimiento, fuente y prioridad, y las tensiones principales están declaradas. Como primer producto operativo del artefacto se creó `tesis_ds/07c_plantilla_solicitud_integracion.md`, que se referencia en el diseño del marco y se presentará completa como anexo operativo. Para la tesis completa, los requisitos deberán contrastarse con la evaluación formativa y ajustarse si el uso real en Central revela fricciones no previstas.

