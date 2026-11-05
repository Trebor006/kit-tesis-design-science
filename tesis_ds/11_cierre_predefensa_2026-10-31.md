# Cierre operativo para la predefensa — 31 de octubre de 2026

> **Estado documental.** Registro histórico de preparación de predefensa. Sus pendientes se resolvieron o se reclasificaron posteriormente; para el estado vigente prevalecen `00_estado.md` y los documentos canónicos E8–E10.

## Propósito

Este documento delimita qué puede presentarse como evidencia al corte de la predefensa y qué permanece abierto para el cierre de la tesis. La predefensa no equivale a defensa final: su función es someter a revisión la coherencia entre problema, artefacto, evidencia y límites, sin adelantar conclusiones que requieren evaluación posterior.

## Evidencia disponible para la predefensa

| Elemento | Estado al corte | Afirmación permitida |
|:--|:--|:--|
| Diagnóstico documental | Disponible | El contexto muestra prácticas heterogéneas de tareas, repositorios, ramas, *commits*, solicitudes y verificación. |
| Entrevistas `DEV-001` y `DEV-002` | Registradas y parcialmente trianguladas | Aportan declaraciones retrospectivas sobre prácticas anteriores a los estándares; no prueban adopción. |
| `E-GH-BASE-02` a `E-GH-BASE-04` | Disponible | En Central Odoo Backend existían ramas con códigos de tarea y solicitudes fusionadas; los *commits* visibles no muestran código de tarea. |
| `E-GH-BASE-06` | Disponible | Central API tenía historial Git desde 2025; la captura no atribuye prácticas individuales ni prueba solicitudes de integración. |
| Artefacto C0–C6 | Construido y documentado | El marco contiene reglas, productos, indicadores y una instanciación en PRX. |
| `CCC-7336` | Aplicación formativa cerrada | El flujo produjo una cadena trazable, fusión de solicitud, eliminación de rama y 169 pruebas unitarias exitosas. |
| `CCC-7480` | Evidencia en curso | Hay rama, solicitud abierta y 182 pruebas unitarias; no se afirma fusión, entrega ni resultado cerrado. |

## Afirmaciones prohibidas

- El marco fue adoptado institucionalmente.
- El marco mejoró sostenidamente los indicadores de PRX.
- Las entrevistas prueban el comportamiento de toda la organización.
- La auto-validación equivale a revisión independiente.
- `CCC-7480` está integrado, entregado o evaluado sumativamente.
- Los principios de diseño están plenamente validados.

## Lista de cierre antes de exponer

1. Usar la versión actualizada de `instituciones/alsie/presentacion_predefensa_2026-10-31.md`.
2. No proyectar capturas privadas con nombres de usuario, nombres personales, enlaces o datos internos; usar códigos de evidencia o copias anonimizadas.
3. Ensayar una exposición de 17 minutos y reservar respuestas para límites, evaluación y contribución.
4. Preparar una respuesta breve para explicar que la evaluación sumativa inicial de `CCC-7336` es de caso, no de periodo comparable.
5. Registrar cada observación del tribunal como posible entrada de rediseño o corrección, sin reescribir retrospectivamente la línea base.

## Pendientes posteriores a la predefensa

1. Completar la triangulación documental disponible de `DEV-002` sin atribuirle eventos no verificables.
2. Decidir si Ansular permanecerá solo como contexto diagnóstico o si se requiere una entrevista a `DEV-004` para sostener una afirmación específica sobre ese proyecto.
3. Obtener un periodo posterior comparable o declarar de manera explícita el límite de la evaluación sumativa inicial.
4. Aplicar y evaluar C5, o mantenerlo como componente diseñado y no evaluado.
5. Actualizar E8, E9 y E10 con evidencia posterior; recién entonces regenerar el IFI desde `tesis_ds/`.
