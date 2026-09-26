# Instrumentos para línea base del diagnóstico

## Propósito

Estos instrumentos se usarán para levantar la línea base antes de aplicar el marco ligero. Su función es producir evidencia trazable sobre visibilidad del trabajo, trazabilidad de cambios y verificación básica del código en la línea de software a medida de PRX. No deben usarse para evaluar desempeño individual de los desarrolladores; el foco de la investigación es el artefacto propuesto y la clase de problema, no la calificación laboral de personas.

## Ficha 1. Extracción del tablero interno de gestión de tareas implementado en Odoo

| Campo | Valor |
|:--|:--|
| Fecha de extracción | Pendiente |
| Responsable de extracción | Robert Cabrera Lara |
| Proyecto piloto | Pendiente |
| Ventana observada | Pendiente |
| Total de tareas registradas | Pendiente |
| Total de tareas activas registradas | Pendiente |
| Tareas con responsable asignado | Pendiente |
| Tareas activas declaradas por entrevista y no registradas | Pendiente |
| Evidencia almacenada | Enlace, captura o identificador interno pendiente |
| Observaciones | Pendiente |

### Tabla de tareas

| ID de tarea | Proyecto | Descripción breve | Responsable | Estado | Fecha de creación | ¿Activa en periodo? | ¿Cuenta para I1? | Observación |
|:--|:--|:--|:--|:--|:--|:--|:--|:--|
| Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente |

## Ficha 2. Extracción de GitHub institucional

| Campo | Valor |
|:--|:--|
| Fecha de extracción | Pendiente |
| Proyecto piloto | Pendiente |
| URL o identificador del repositorio | Pendiente |
| Rama principal observada | Pendiente |
| Ventana observada | Pendiente |
| Total de ramas creadas en ventana | Pendiente |
| Ramas conformes con convención | Pendiente |
| Total de commits en ventana | Pendiente |
| Commits conformes con convención | Pendiente |
| Cambios integrados a rama principal | Pendiente |
| Cambios integrados mediante solicitud de integración | Pendiente |
| Solicitudes con evidencia mínima de verificación | Pendiente |
| Evidencia almacenada | Enlace, captura o exportación pendiente |

### Tabla de ramas y commits

| Repositorio | Rama o commit | Tipo | Autor | Fecha | Mensaje o nombre | ¿Conforme? | Regla aplicada | Observación |
|:--|:--|:--|:--|:--|:--|:--|:--|:--|
| Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente |

### Tabla de solicitudes de integración de cambios

| Repositorio | ID o enlace | Fecha | Cambio asociado | ¿Tiene descripción? | ¿Tiene evidencia de verificación? | Tipo de evidencia | Resultado | Observación |
|:--|:--|:--|:--|:--|:--|:--|:--|:--|
| Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente | Pendiente |

## Ficha 3. Pruebas unitarias iniciales

| Campo | Valor |
|:--|:--|
| Proyecto piloto | Pendiente |
| Componente crítico identificado | Pendiente |
| Razón de criticidad | Lógica de negocio, integración, transformación de datos, defecto reciente u otro motivo documentado |
| ¿Existen pruebas unitarias? | Pendiente |
| Comando de ejecución | Pendiente |
| Resultado de ejecución | Pendiente |
| Fecha de ejecución | Pendiente |
| Evidencia almacenada | Captura, registro de consola o enlace pendiente |
| Observaciones | Pendiente |

## Guía de entrevista breve a desarrolladores

La entrevista debe durar entre 10 y 15 minutos por participante. Debe registrarse fecha, participante codificado, rol general y proyecto relacionado. No se deben registrar afirmaciones personales sensibles ni juicios de desempeño individual.

1. ¿En qué tareas trabajó durante la ventana observada y cuáles de ellas estaban registradas en el tablero interno de gestión de tareas implementado en Odoo?
2. ¿Qué repositorio utilizó para esos cambios y cómo organizó ramas y commits?
3. ¿Los cambios se integraron mediante solicitudes de integración de cambios o mediante fusión directa? ¿Por qué?
4. ¿Qué verificación realizó antes de integrar o entregar el cambio?
5. ¿Existe algún componente del proyecto que considere crítico y que debería tener pruebas unitarias iniciales? ¿Por qué?
6. ¿Qué dificultad concreta encuentra para registrar tareas, usar ramas, crear solicitudes de integración o escribir pruebas unitarias?
7. ¿Hubo defectos o correcciones urgentes asociadas a cambios recientes durante la ventana observada?

## Ficha de consolidación de línea base

| Indicador | Valor de línea base | Fuente principal | Fuente secundaria | Evidencia | Observación |
|:--|:--|:--|:--|:--|:--|
| I1. Visibilidad de tareas activas | Pendiente | Odoo | Entrevistas | Pendiente | Pendiente |
| I2. Repositorio institucional | Pendiente | GitHub | Revisión documental | Pendiente | Pendiente |
| I3. Cumplimiento de convención de ramas | Pendiente | GitHub | Revisión manual | Pendiente | Pendiente |
| I4. Cumplimiento de convención de commits | Pendiente | GitHub | Revisión manual | Pendiente | Pendiente |
| I5. Cambios integrados mediante solicitudes de integración | Pendiente | GitHub | Entrevistas | Pendiente | Pendiente |
| I6. Solicitudes con evidencia mínima de verificación | Pendiente | GitHub | Revisión manual | Pendiente | Pendiente |
| I7. Componentes críticos con pruebas unitarias iniciales | Pendiente | Repositorio | Ejecución de pruebas | Pendiente | Pendiente |
| I8. Defectos o correcciones urgentes | Pendiente | Odoo, GitHub o entrevista | Revisión documental | Pendiente | Indicador contextual |

## Registro de cierre de línea base

Antes de aplicar el marco, se deberá completar la siguiente declaración:

> Los valores de línea base fueron levantados entre [fecha] y [fecha], usando datos del tablero interno de gestión de tareas implementado en Odoo, GitHub institucional, repositorios de proyectos piloto y entrevistas breves. Estos valores fueron fijados antes de aplicar el marco y antes de ejecutar la evaluación formativa. Cualquier cambio posterior en los criterios será tratado como rediseño documentado y no como ajuste retroactivo de la evaluación.
