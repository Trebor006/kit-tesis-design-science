# E7e. Construcción y verificación interna

## Propósito

Este documento registra la construcción y verificación interna de la versión **V1.0-Central** del **Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización**. En esta etapa, “construir” no significa desarrollar una aplicación de software completa, sino formalizar y aplicar los productos operativos del marco: estándares mínimos, plantilla de solicitud de integración, repositorio organizacional `.github`, evidencias institucionales y primeras fricciones de adopción.

La construcción se documenta como intervención posterior a la línea base. Por tanto, las evidencias registradas en este archivo no deben confundirse con diagnóstico previo. Su función es demostrar que el artefacto comenzó a existir como práctica formalizable y verificable en PRX, y preparar la evaluación formativa posterior.

## Alcance de V1.0-Central construido hasta el momento

| Elemento de V1.0-Central | Estado | Evidencia asociada | Observación |
|:--|:--|:--|:--|
| Convención mínima de ramas | Construida y publicada. | `E-ORG-INT-01`; `E-ORG-INT-05`. | Formalizada como `STD-GIT-001 — Convención mínima de ramas`. |
| Plantilla operativa de solicitud de integración | Construida y publicada. | `E-ORG-INT-02`; `E-GH-ORG-01`. | La plantilla opera como instrumento para completar la descripción de la solicitud de integración. |
| Estándar de solicitudes de integración | Construido y publicado. | `E-ORG-INT-03`; `E-ORG-INT-05`. | Formalizado como `STD-GIT-002 — Convención mínima de solicitudes de integración`; diferencia título, descripción, validación y excepciones. |
| Convención mínima de commits | Construida y publicada. | `E-ORG-INT-04`; `E-ORG-INT-05`. | Formalizada como `STD-GIT-003 — Convención mínima de commits`. |
| Organización documental de estándares técnicos | Construida. | `E-ORG-INT-05`. | Los estándares quedaron organizados en carpetas técnicas diferenciadas para Git y solicitudes de integración. |
| Repositorio organizacional `.github` | Iniciado. | `E-GH-ORG-01`. | Permite instanciar la plantilla de solicitudes de integración en GitHub. |
| Aplicación en solicitud de integración real de Central | Pendiente. | `E-GH-INT-01` pendiente. | Se requiere al menos una solicitud posterior usando rama, commits, título, plantilla y evidencia mínima. |
| Verificación técnica en componente crítico | Pendiente. | `E-TEST-INT-01` pendiente. | Se requiere prueba, construcción, prueba de API o verificación manual documentada. |

## Productos construidos

### STD-GIT-001 — Convención mínima de ramas

Se construyó y publicó el estándar `STD-GIT-001 — Convención mínima de ramas`. El estándar define ramas permanentes mínimas (`main`, `stage` y `production` cuando aplique), formato de ramas temporales y tipos iniciales permitidos. La regla central es que toda rama temporal de trabajo debe seguir el formato:

```text
<tipo>/<codigo-tarea>-<descripcion-corta>
```

Este producto operacionaliza los requisitos RQ5 y RQ5.1 del artefacto, porque convierte la trazabilidad de ramas en una regla institucional verificable. La evidencia está registrada como `E-ORG-INT-01`, dividida en tres capturas, y como parte de la estructura documental general en `E-ORG-INT-05`.

### Plantilla operativa de solicitud de integración

Se construyó una plantilla operativa de solicitud de integración, documentada como instrumento que debe completarse en la descripción de cada solicitud. La plantilla contiene secciones para tarea relacionada, resumen, cambios principales, componentes afectados, archivos modificados, comportamiento esperado, riesgo, plan de prueba, verificación realizada, evidencia, validación y lista mínima de control.

Esta plantilla operacionaliza los requisitos RQ7, RQ8, RQ9 y RQ10. No se trata de una formalidad documental: obliga a declarar qué se cambió, por qué se cambió, qué componentes afecta, qué verificación se realizó y qué evidencia respalda el cambio. La evidencia está registrada como `E-ORG-INT-02`.

### STD-GIT-002 — Convención mínima de solicitudes de integración

Después de distinguir entre plantilla y estándar, se construyó `STD-GIT-002 — Convención mínima de solicitudes de integración`. Este estándar define el formato del título de la solicitud, el uso obligatorio de la plantilla, los criterios mínimos para que una solicitud sea válida, la validación aceptada y las excepciones.

El título de la solicitud debe seguir el formato:

```text
<tipo>(<codigo-tarea>): <descripcion breve>
```

Esta decisión evita una debilidad observada durante el diseño: una plantilla puede mejorar la descripción, pero no controla el título de la solicitud. Al formalizar ambos elementos, el marco fortalece la trazabilidad entre tarea, rama, commit y solicitud de integración. La evidencia está registrada como `E-ORG-INT-03`.

### STD-GIT-003 — Convención mínima de commits

Se construyó y publicó `STD-GIT-003 — Convención mínima de commits`. El estándar define que la primera línea del mensaje de commit debe seguir el formato:

```text
<tipo>(<codigo-tarea>): <descripcion-breve>
```

El estándar toma como referencia Conventional Commits 1.0.0, pero adapta el campo entre paréntesis para representar el código de tarea, no el componente técnico. Esta adaptación es explícita y responde al problema de trazabilidad observado en PRX. La evidencia está registrada como `E-ORG-INT-04`.

### Organización documental de estándares técnicos

Los estándares se organizaron en SharePoint bajo una estructura documental separada por familia técnica. La evidencia `E-ORG-INT-05` muestra la carpeta de estándares Git, con `STD-GIT-001-convencion-de-ramas.md` y `STD-GIT-003-convencion-de-commits.md`, y la carpeta de solicitudes de integración, con `STD-GIT-002-convencion-de-pull-requests.md` y `STD-GIT-002-pull_request_template.md`.

Esta organización no es un componente conceptual separado del marco, pero sí evidencia gobernanza mínima y disponibilidad de los productos operativos para el equipo. Por ello, se relaciona con C2, C3 e I9.

### Repositorio organizacional `.github`

Se inició la instanciación técnica en GitHub mediante el repositorio organizacional `.github`. La evidencia `E-GH-ORG-01` muestra la existencia de la rama `main` y una rama temporal de configuración de la plantilla de solicitud de integración.

La rama temporal observada fue:

```text
config/ADM-4940_config_pr_template
```

Esta rama evidencia aplicación inicial de la convención, porque incluye tipo (`config`) y código de tarea (`ADM-4940`). No obstante, también revela una fricción: la descripción usa guion bajo en lugar de guiones, mientras que la convención definida exige `<tipo>/<codigo-tarea>-<descripcion-corta>`. El formato esperado habría sido:

```text
config/ADM-4940-config-pr-template
```

Esta diferencia se registra como fricción formativa, no como incumplimiento oculto. Es evidencia útil porque muestra que la primera aplicación del marco requiere ajuste de comunicación y seguimiento.

## Verificación interna de productos construidos

| Producto | Verificación realizada | Resultado | Evidencia |
|:--|:--|:--|:--|
| `STD-GIT-001` | Revisión de contenido contra requisitos de ramas permanentes y temporales. | Cumple con convención mínima, progresiva y extensible. | `E-ORG-INT-01`; `E-ORG-INT-05`. |
| Plantilla operativa de solicitud de integración | Revisión de campos mínimos contra requisitos de solicitud válida y evidencia de verificación. | Cumple como instrumento operativo para descripción de solicitud de integración. | `E-ORG-INT-02`. |
| `STD-GIT-002` | Revisión de título, uso de plantilla, validación y excepciones. | Cumple como estándar, diferenciado de la plantilla. | `E-ORG-INT-03`; `E-ORG-INT-05`. |
| `STD-GIT-003` | Revisión de formato de commit, tipos permitidos, ejemplos y validación mínima. | Cumple como convención mínima de commits y mantiene alineación con ramas y solicitudes. | `E-ORG-INT-04`; `E-ORG-INT-05`. |
| Repositorio `.github` | Revisión visual de repositorio y ramas. | Evidencia instanciación inicial; se detecta fricción en nombre de rama. | `E-GH-ORG-01`. |

La verificación interna confirma que los productos documentales y técnicos iniciales existen y están alineados con los requisitos del artefacto. Sin embargo, esta verificación no equivale a evaluación de campo. Todavía falta observar el uso del marco en una solicitud de integración real de Central y registrar evidencia de verificación técnica.

## Trazabilidad producto → componente → indicador

| Producto construido | Componente del marco | Indicadores relacionados | Función en el artefacto |
|:--|:--|:--|:--|
| `STD-GIT-001` | C2. Trazabilidad del código | I3, I4, I9 | Define convención mínima de ramas y relación inicial con commits. |
| `STD-GIT-003` | C2. Trazabilidad del código | I4, I9 | Define convención mínima de commits con código de tarea. |
| Plantilla operativa de solicitud de integración | C3. Integración y revisión de cambios | I5, I6, I9 | Estructura la descripción del cambio, verificación, validación y evidencia. |
| `STD-GIT-002` | C3. Integración y revisión de cambios | I5, I6, I9 | Define título, uso obligatorio de plantilla, solicitud válida y excepciones. |
| Repositorio `.github` | C3. Integración y revisión de cambios | I5, I6, I9 | Instancia la plantilla en GitHub para la organización. |
| Estructura documental de estándares | C2, C3 y C6 | I3, I4, I5, I6, I9 | Facilita disponibilidad, gobernanza mínima y seguimiento. |

## Problemas y fricciones detectadas

| Fricción | Evidencia | Interpretación | Acción prevista |
|:--|:--|:--|:--|
| Uso de guion bajo en `config/ADM-4940_config_pr_template`. | `E-GH-ORG-01`. | La regla fue comprendida parcialmente: se usó tipo y código de tarea, pero no el separador definido para la descripción. | Registrar como fricción formativa y reforzar el ejemplo correcto en la comunicación del estándar. |
| Diferencia inicial entre plantilla y estándar de solicitud de integración. | `E-ORG-INT-02`; `E-ORG-INT-03`. | La plantilla resolvía la descripción, pero no el título de la solicitud; el estándar completo cerró esa brecha. | Mantener ambos productos separados: plantilla operativa y estándar institucional. |
| Verificación técnica aún no ejecutada en Central. | Pendiente `E-TEST-INT-01`. | La construcción documental no demuestra por sí sola verificación técnica del código. | Ejecutar prueba, construcción, prueba de API o prueba manual documentada en componente crítico. |
| Solicitud de integración real posterior pendiente. | Pendiente `E-GH-INT-01`. | Aún no se observó el uso completo de rama, commits, título, plantilla y evidencia en un cambio real de Central. | Aplicar el marco en una solicitud real y capturar evidencia. |

## Estado frente al criterio de suficiencia de E7d

| Condición definida en E7d | Estado actual | Comentario |
|:--|:--|:--|
| Plantilla disponible mediante repositorio `.github`. | Parcialmente cumplida. | Existe evidencia del repositorio `.github`; falta capturar la plantilla aplicada en una solicitud nueva si aún no se tiene. |
| Central con componentes, responsables y repositorios o excepciones. | Definido documentalmente. | Componentes y responsables están codificados en documentos previos; falta integrarlo en ficha E7f. |
| Ramas permanentes y equivalencias declaradas por repositorio. | Parcial. | Hay estándar general; falta ficha por repositorio Central. |
| Convención comunicada a responsables. | Parcial. | La publicación en SharePoint evidencia disponibilidad; falta evidencia de comunicación o uso por los responsables. |
| Al menos una solicitud nueva con plantilla o fricción. | Pendiente. | Debe levantarse `E-GH-INT-01`. |
| Mecanismo para registrar evidencia de verificación. | Definido, no aplicado. | La plantilla exige evidencia; falta `E-TEST-INT-01`. |
| Evidencias categorizadas. | Cumplido para intervención inicial. | `06_plan_evidencias_privadas.md` separa línea base, intervención y evaluación. |

## Pendientes para cerrar E7e completamente

E7e queda **avanzado, pero no cerrado de forma absoluta**. La construcción documental e institucional de V1.0-Central está respaldada por evidencias, pero aún falta demostrar aplicación completa en un cambio real de Central. Los pendientes mínimos son:

1. Capturar `E-GH-INT-01`: primera solicitud de integración posterior al marco usando título, plantilla, rama y commits trazables.
2. Capturar `E-TEST-INT-01`: evidencia de verificación técnica en al menos un componente crítico de Central.
3. Registrar, si corresponde, `E-FORM-01`: fricciones observadas por responsables o por el tesista durante el primer uso.
4. Integrar las evidencias de aplicación real en E8 como evaluación formativa.

## Estado del gate E7e

E7e queda **suficiente como registro inicial de construcción y verificación interna**, porque existen productos operativos construidos, evidencias privadas verificadas y fricciones documentadas. No obstante, para cumplir el estándar de maestría en Design Science, esta etapa debe completarse con una aplicación real en Central y con evidencia de verificación técnica antes de pasar a una evaluación sumativa.
