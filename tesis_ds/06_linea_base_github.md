# Línea base específica de GitHub institucional

## Propósito

Esta ficha registra la línea base de uso de GitHub antes de aplicar el marco ligero. Su objetivo es documentar cómo se usan actualmente los repositorios, ramas, commits, solicitudes de integración de cambios y evidencia de verificación en los proyectos piloto de software a medida. La línea base no demuestra mejora todavía; fija el punto de partida para comparar la evaluación posterior del artefacto.

## Ventana de observación

La ventana de observación corresponde al periodo comprendido entre el **21 de septiembre de 2026** y el **4 de octubre de 2026**. Los datos históricos fuera de esta ventana se registran solo como evidencia contextual y no se usan para calcular los indicadores principales.

Las fusiones directas mencionadas por el tesista corresponden, en varios casos, a práctica histórica y no necesariamente a actividad ocurrida dentro de la ventana observada. Para los indicadores I5 e I6 solo se contabilizan solicitudes de integración y fusiones ocurridas entre el 21 de septiembre de 2026 y el 4 de octubre de 2026.

## Situación inicial actualizada

La información nueva obtenida del desarrollador Odoo corrige datos preliminares anteriores. En Central Odoo, el backend operativo se encuentra instalado en un servidor local, con un clon en Odoo.sh que no siempre está actualizado; el repositorio visible en GitHub institucional corresponde a ese entorno relacionado. Esta condición debe registrarse porque afecta la trazabilidad real entre código en producción, Odoo.sh y GitHub.

La situación general sigue mostrando institucionalización incompleta: algunos componentes están en GitHub institucional de PRX, otros permanecen en cuentas personales u otras organizaciones, y no existe documentación formal de ramas, commits o verificación mínima.

## Repositorios por proyecto y componente

| Proyecto | Componente | Tecnología | Repositorio | ¿GitHub institucional PRX? | Situación previa | Observación |
|:--|:--|:--|:--|:--|:--|:--|
| Central | Backend Odoo | Python - Odoo | `https://github.com/PRX/Premmium-Finance` | Sí | Estaba en otra organización. | El backend operativo está en servidor local; existe clon en Odoo.sh que no siempre está actualizado. |
| Central | API | C# | `https://github.com/joselo/insFinanceApi` | No | Cuenta personal; antes no estaba en GitHub. | Pendiente migración a la organización institucional. Hubo cambios en las dos semanas, pero no fueron subidos. |
| Central | Frontend | Angular - TypeScript | `https://github.com/PRX/central-front` | Sí | Estaba en otra organización; incorporación aproximada en abril de 2026. | Sin actividad en la ventana; uso histórico de solicitudes de integración y despliegue automático desde rama de prueba. |
| Ansular | Backend Odoo | Python - Odoo | `https://github.com/PRX/ansular-trading` | Sí | Estaba en otra organización; incorporación aproximada en febrero de 2026. | Requiere coordinación con desarrolladores Odoo para acceso directo y evidencia complementaria. |
| Ansular | Frontend | Angular - TypeScript | `https://github.com/software/ansular-front` | No | Está en otra organización. | Pendiente migración al GitHub institucional. |
| PConst | Backend | Express.js - TypeScript | `https://github.com/software/pconst-back` | No | Está en otra organización. | Usa prácticas de commits no documentadas; tiene pruebas unitarias, pruebas de integración y empaquetado automático hacia AWS Lambda. |
| PConst | Frontend | Angular - TypeScript | `https://github.com/software/pconst-front` | No | Está en otra organización. | Usa prácticas de commits no documentadas; tiene pruebas unitarias en componentes, pruebas de integración y proyecto de pruebas de extremo a extremo. |

## Fichas por repositorio

### Central - Backend Odoo

| Campo | Valor |
|:--|:--|
| Proyecto | Central |
| Componente | Backend Odoo |
| Tecnología | Python - Odoo |
| Repositorio | `https://github.com/PRX/Premmium-Finance` |
| Rama principal actual | `main` |
| ¿Está en GitHub institucional de PRX? | Sí |
| Situación previa | Estaba en otra organización. |
| Ramas creadas en la ventana | 1 |
| Commits en la ventana | 2 |
| Solicitudes de integración en la ventana | 1 |
| ¿Hubo fusiones directas a rama principal? | No |
| ¿Existe convención documentada de ramas? | No hay documentación formal; se observa uso del código del proyecto en la rama. |
| ¿Existe convención documentada de commits? | No hay documentación formal; se observa uso de una convención similar a commits convencionales. |
| ¿Hay evidencia de verificación en solicitudes de integración? | No |
| Observaciones | El tesista no tiene acceso directo completo y debe coordinar con desarrolladores Odoo. El backend operativo está en servidor local; existe clon en Odoo.sh que no siempre está actualizado y aparece relacionado con el GitHub institucional. |

#### Registro de solicitudes de integración y commits

| Solicitud de integración | Rama | Destino | Fecha | Hash parcial | Autor codificado | Mensaje | Evidencia de verificación | Observación |
|:--|:--|:--|:--|:--|:--|:--|:--|:--|
| `feat(ibt_premiun_finance): cancellation notices with automatic creation` | `CCC-4900` | `Stage` | 2026-10-01 | `cb8501d` | DEV-001 | `feat(ibt_premiun_finance): auto-create cancellation notices from overdue debt` | No | Commit asociado a solicitud de integración. |
| `feat(ibt_premiun_finance): cancellation notices with automatic creation` | `CCC-4900` | `Stage` | 2026-10-01 | `c3f2b36` | DEV-001 | `feat(ibt_premiun_finance): add cancellation notice models and views` | No | Commit asociado a solicitud de integración. |

### Central - API

| Campo | Valor |
|:--|:--|
| Proyecto | Central |
| Componente | API |
| Tecnología | C# |
| Repositorio | `https://github.com/joselo/insFinanceApi` |
| Rama principal actual | `master` |
| ¿Está en GitHub institucional de PRX? | No |
| Situación previa | Cuenta personal; antes no estaba en GitHub. |
| Fecha aproximada de incorporación al GitHub institucional | Pendiente |
| Ramas creadas en la ventana | 0 |
| Commits en la ventana | 0 |
| Solicitudes de integración en la ventana | 0 |
| ¿Hubo fusiones directas a rama principal? | No registradas en GitHub durante la ventana; se reportan cambios no subidos. |
| ¿Existe convención documentada de ramas? | No |
| ¿Existe convención documentada de commits? | No |
| ¿Hay evidencia de verificación en solicitudes de integración? | No aplica; no hubo solicitudes. |
| Observaciones | Hay una tarea a cargo del tesista para mover repositorios a la cuenta de la organización. Se reporta trabajo realizado en las dos semanas, pero aún no subido al repositorio; esto debe tratarse como evidencia de trabajo no trazable en GitHub. Existe evidencia histórica de uso de solicitudes de integración fuera de la ventana observada; no se contabiliza en los indicadores principales de línea base. |

### Central - Frontend

| Campo | Valor |
|:--|:--|
| Proyecto | Central |
| Componente | Frontend |
| Tecnología | Angular - TypeScript |
| Repositorio | `https://github.com/PRX/central-front` |
| Rama principal actual | `main` |
| ¿Está en GitHub institucional de PRX? | Sí |
| Situación previa | Estaba en otra organización; incorporación aproximada en abril de 2026. |
| Ramas creadas en la ventana | 0 |
| Commits en la ventana | 0 |
| Solicitudes de integración en la ventana | 0 |
| ¿Hubo fusiones directas a rama principal? | No en la ventana; existe práctica histórica. |
| ¿Existe convención documentada de ramas? | No |
| ¿Existe convención documentada de commits? | No |
| ¿Hay evidencia de verificación en solicitudes de integración? | No aplica en la ventana; existe evidencia histórica declarada fuera del periodo. |
| Observaciones | En las últimas semanas no hubo desarrollo. El tesista declara uso histórico de solicitudes de integración, separación en ramas `test` y `master`, y despliegue automático desde `test` hacia servidor de pruebas. La evidencia histórica de solicitudes de integración fuera de la ventana observada no se contabiliza en los indicadores principales de línea base. |

### Ansular - Backend Odoo

| Campo | Valor |
|:--|:--|
| Proyecto | Ansular |
| Componente | Backend Odoo |
| Tecnología | Python - Odoo |
| Repositorio | `https://github.com/PRX/ansular-trading` |
| Rama principal actual | `main` |
| ¿Está en GitHub institucional de PRX? | Sí |
| Situación previa | Estaba en otra organización; incorporación aproximada en febrero de 2026. |
| Ramas creadas o usadas en la ventana | 4 ramas asociadas a solicitudes de integración: `insular-7055`, `insular-7074`, `insular-7055-prod` e `insular-7074-prod`. |
| Commits en la ventana | 6 |
| Solicitudes de integración en la ventana | 4 |
| ¿Hubo fusiones directas a rama principal? | No |
| ¿Existe convención documentada de ramas? | No |
| ¿Existe convención documentada de commits? | No |
| ¿Hay evidencia de verificación en solicitudes de integración? | No |
| Observaciones | El tesista no tiene acceso directo completo al repositorio y debe coordinar con desarrolladores Odoo. Las ramas fueron identificadas a partir de las solicitudes de integración proporcionadas como evidencia; si posteriormente se requiere fecha exacta de creación de rama, deberá verificarse en GitHub. |

#### Registro de solicitudes de integración y commits

| Solicitud de integración | Rama | Destino | Fecha | Hash parcial | Autor codificado | Mensaje | Evidencia de verificación | Observación |
|:--|:--|:--|:--|:--|:--|:--|:--|:--|
| `[insular-7055] Bounce Checks - #89` | `insular-7055` | `Stage` | 2026-09-22 | `1450a6b` | DEV-004 | `Add sales_team dependency so bounce check CI can load the menu.` | No | Commit asociado a solicitud de integración. |
| `[insular-7055] Bounce Checks - #89` | `insular-7055` | `Stage` | 2026-09-22 | `a50a60b` | DEV-004 | `Credit the original payment bank account on bounce check debit memos.` | No | Commit asociado a solicitud de integración. |
| `[insular-7074] Facturas Void - #90` | `insular-7074` | `Stage` | 2026-09-23 | `1acdfaf` | DEV-004 | `Fix vendor bills stuck as Paid after Void Check.` | No | Commit asociado a solicitud de integración. |
| `[insular-7055] Bounce Checks - #91` | `insular-7055-prod` | `Stage` | 2026-09-24 | `41f4a80` | DEV-004 | `Add sales_team dependency so bounce check CI can load the menu.` | No | Commit asociado a solicitud de integración. |
| `[insular-7055] Bounce Checks - #91` | `insular-7055-prod` | `Stage` | 2026-09-24 | `d85f7ae` | DEV-004 | `Credit the original payment bank account on bounce check debit memos.` | No | Commit asociado a solicitud de integración. |
| `[insular-7074] Facturas Void - #92` | `insular-7074-prod` | `Production` | 2026-09-24 | `e34f6c6` | DEV-004 | `Fix vendor bills stuck as Paid after Void Check. (#90)` | No | Commit asociado a solicitud de integración hacia producción. |

### Ansular - Frontend

| Campo | Valor |
|:--|:--|
| Proyecto | Ansular |
| Componente | Frontend |
| Tecnología | Angular - TypeScript |
| Repositorio | `https://github.com/software/ansular-front` |
| Rama principal actual | `master` |
| ¿Está en GitHub institucional de PRX? | No |
| Situación previa | Está en otra organización. |
| Fecha aproximada de incorporación al GitHub institucional | Pendiente |
| Ramas creadas en la ventana | 0 |
| Commits en la ventana | 0 |
| Solicitudes de integración en la ventana | 0 |
| ¿Hubo fusiones directas a rama principal? | No registradas dentro de la ventana; existe práctica histórica declarada. |
| ¿Existe convención documentada de ramas? | No |
| ¿Existe convención documentada de commits? | No |
| ¿Hay evidencia de verificación en solicitudes de integración? | No aplica; no hubo solicitudes. |
| Observaciones | Está pendiente moverlo al GitHub institucional de PRX. Existe evidencia histórica de uso de solicitudes de integración fuera de la ventana observada; no se contabiliza en los indicadores principales de línea base. |

### PConst - Backend

| Campo | Valor |
|:--|:--|
| Proyecto | PConst |
| Componente | Backend |
| Tecnología | Express.js - TypeScript |
| Repositorio | `https://github.com/software/pconst-back` |
| Rama principal actual | `main` |
| ¿Está en GitHub institucional de PRX? | No |
| Situación previa | Está en otra organización. |
| Fecha aproximada de incorporación al GitHub institucional | Pendiente |
| Ramas creadas en la ventana | 0 |
| Commits en la ventana | 0 |
| Solicitudes de integración en la ventana | 0 |
| ¿Hubo fusiones directas a rama principal? | No |
| ¿Existe convención documentada de ramas? | No |
| ¿Existe convención documentada de commits? | No, aunque existen prácticas usadas no documentadas. |
| ¿Hay evidencia de verificación en solicitudes de integración? | No aplica; no hubo solicitudes. |
| Observaciones | El tesista se integró al proyecto en mayo. Declara desarrollo del backend, uso práctico de estándares de commits no documentados, incorporación de pruebas unitarias, pruebas de integración, empaquetado automático para despliegue en AWS Lambda y creación de un proyecto para pruebas de extremo a extremo. Existe evidencia histórica de uso de solicitudes de integración fuera de la ventana observada; no se contabiliza en los indicadores principales de línea base. |

### PConst - Frontend

| Campo | Valor |
|:--|:--|
| Proyecto | PConst |
| Componente | Frontend |
| Tecnología | Angular - TypeScript |
| Repositorio | `https://github.com/software/pconst-front` |
| Rama principal actual | `main` |
| ¿Está en GitHub institucional de PRX? | No |
| Situación previa | Está en otra organización. |
| Fecha aproximada de incorporación al GitHub institucional | Pendiente |
| Ramas creadas en la ventana | 0 |
| Commits en la ventana | 0 |
| Solicitudes de integración en la ventana | 0 |
| ¿Hubo fusiones directas a rama principal? | No registradas dentro de la ventana; existe práctica histórica declarada. |
| ¿Existe convención documentada de ramas? | No |
| ¿Existe convención documentada de commits? | No, aunque existen prácticas usadas no documentadas. |
| ¿Hay evidencia de verificación en solicitudes de integración? | No aplica; no hubo solicitudes. |
| Observaciones | El tesista se integró al proyecto en mayo. Declara desarrollo del frontend, uso práctico de estándares de commits no documentados, incorporación de pruebas unitarias en componentes, pruebas de integración y creación de otro proyecto para pruebas de extremo a extremo. Existe evidencia histórica de uso de solicitudes de integración fuera de la ventana observada; no se contabiliza en los indicadores principales de línea base. |

## Consolidación preliminar de indicadores GitHub

Esta consolidación es preliminar porque todavía faltan capturas, exportaciones o revisión conjunta que respalden cada valor. Los porcentajes se calculan sobre los siete componentes técnicos identificados.

| Indicador | Valor preliminar | Cálculo | Interpretación |
|:--|:--|:--|:--|
| I2. Componentes con repositorio en GitHub institucional | 3 de 7 componentes, equivalente a 42,86 %. | Central Odoo, Central Frontend y Ansular Backend están en PRX; Central API, Ansular Frontend, PConst Backend y PConst Frontend no están en PRX. | Existe GitHub para los componentes, pero la institucionalización todavía es incompleta. |
| I3. Cumplimiento de convención documentada de ramas | 0 %. | Ningún componente tiene convención documentada de ramas. | Existen ramas asociadas a solicitudes de integración y patrones usados en algunos repositorios, pero no constituyen estándar formal documentado. |
| I4. Cumplimiento de convención documentada de commits | 0 %. | Ningún componente tiene convención documentada de commits. | Central Odoo y PConst muestran prácticas aparentes, pero no documentadas institucionalmente. |
| I5. Cambios integrados mediante solicitudes de integración | 5 de 5 cambios integrados observables en GitHub durante la ventana, equivalente a 100 %. | Central Odoo: 1; Ansular Backend: 4. Todas las solicitudes fueron fusionadas dentro de las fechas indicadas. El cálculo excluye trabajo no subido a GitHub, como el caso reportado de Central API. | Existe uso de solicitudes de integración en los cambios observables de Odoo, pero no hay homogeneidad entre todos los componentes, no hay revisión independiente y no hay evidencia de verificación asociada. |
| I6. Solicitudes con evidencia mínima de verificación | 0 de 5 solicitudes, equivalente a 0 %. | Las solicitudes registradas no incluyen evidencia de verificación declarada. | La solicitud de integración existe en algunos casos, pero no funciona todavía como control verificable de calidad. |

## Observaciones metodológicas

1. Central API presenta trabajo no trazado: hubo cambios en las dos semanas, pero no fueron subidos al repositorio. Esto fortalece el diagnóstico sobre falta de trazabilidad institucional.
2. Central Odoo requiere una nota especial porque el backend operativo está en servidor local y el clon en Odoo.sh no siempre está actualizado. Esto puede afectar la validez de GitHub como fuente única de evidencia.
3. En Ansular Backend, las ramas `insular-7055`, `insular-7074`, `insular-7055-prod` e `insular-7074-prod` se registran como ramas usadas en solicitudes de integración dentro de la ventana. Si posteriormente se requiere precisión sobre fecha exacta de creación, deberá verificarse en GitHub.
4. El uso de convenciones aparentes no equivale a convención documentada. Para la línea base formal, la ausencia de documentación debe registrarse como 0 % de conformidad formal.
5. PConst tiene avances técnicos relevantes en pruebas y automatización, pero al estar fuera del GitHub institucional y carecer de convención documentada, esos avances no constituyen todavía estándar institucional común.
6. Central Frontend, Central API, Ansular Frontend, PConst Backend y PConst Frontend tienen evidencia histórica de uso de solicitudes de integración fuera de la ventana observada. Esa evidencia se conserva como contexto, pero no se contabiliza en los indicadores principales porque la línea base mide el periodo del 21 de septiembre de 2026 al 4 de octubre de 2026.
7. En Central Frontend, las prácticas de rama de trabajo, solicitud de integración, referencia al ticket y `squash merge` fueron introducidas por el tesista después de recibir un repositorio con trazabilidad inicial mínima. Por tanto, no se interpretan como estándar institucional existente, sino como antecedente práctico de la propuesta de estandarización.
8. Existen diferencias de nomenclatura entre componentes: en Central Frontend se usa una rama de prueba denominada `test`, mientras que en proyectos Odoo aparece una rama o destino denominado `Stage`. Esta variación refuerza la ausencia de una convención institucional única para ramas de integración o validación.
9. En los proyectos donde un solo desarrollador concentra el trabajo de un componente, las solicitudes de integración pueden ser creadas y fusionadas por la misma persona. Por tanto, la existencia de solicitud de integración no debe interpretarse automáticamente como revisión independiente. El marco deberá distinguir entre solicitud de integración como mecanismo de trazabilidad y solicitud de integración revisada por un tercero.

## Datos pendientes para cerrar esta línea base

- Guardar capturas, exportaciones o revisión conjunta de los repositorios observados.
- Verificar fecha exacta de creación de las ramas de Ansular Backend solo si el tribunal exige distinguir entre ramas creadas en la ventana y ramas usadas en solicitudes de integración durante la ventana.
- Confirmar si la solicitud de integración de Central Odoo hacia `Stage` corresponde a GitHub, Odoo.sh o flujo mixto GitHub/Odoo.sh.
- Registrar si hubo cambios no subidos en Central API con una fuente secundaria, por ejemplo entrevista o tarea interna, porque no aparecen en GitHub.
- Obtener evidencia de ausencia de actividad en Central Frontend, Ansular Frontend, PConst Backend y PConst Frontend durante la ventana.

## Cierre de línea base GitHub

Antes de aplicar el marco, complete esta declaración:

> La línea base de GitHub fue levantada entre el 21 de septiembre de 2026 y el 4 de octubre de 2026, sobre los repositorios vinculados a Central, Ansular y PConst. Los valores registrados reflejan el estado de uso de repositorios, ramas, commits, solicitudes de integración y evidencia de verificación antes de aplicar el marco ligero. La información histórica fuera de la ventana fue tratada como contexto y no como indicador principal de la medición.
