# Guía específica para recolectar la línea base por proyecto

## Propósito

Esta guía organiza la evidencia que debe recolectarse antes de aplicar el marco ligero de adopción inicial de prácticas de Ingeniería de Software. La recolección se hará por cada proyecto piloto seleccionado, porque la línea base debe mostrar cómo se encuentra cada proyecto antes del artefacto y luego consolidar los indicadores de diagnóstico. La evidencia no debe usarse para evaluar desempeño individual de desarrolladores, sino para demostrar la existencia del problema de diseño y fijar una línea base verificable.

## Regla metodológica central

La línea base debe levantarse antes de aplicar el marco. Si un proyecto no tiene tareas registradas, repositorio institucional, solicitudes de integración o pruebas unitarias, esa ausencia se registra como evidencia del problema; no debe corregirse antes de medirla ni completarse con estimaciones informales.

## Proyectos a revisar

| Código sugerido | Proyecto real | Decisión de inclusión | Observación |
|:--|:--|:--|:--|
| Proyecto A | Central | Pendiente de confirmar | Proyecto de software a medida compuesto por tres componentes: un módulo o sistema en Odoo, una API en C# y un frontend en Angular. Revisar actividad reciente, repositorios, tareas y pruebas existentes por componente. |
| Proyecto B | Ansular | Pendiente de confirmar | Proyecto de software a medida compuesto por un componente en Odoo y un frontend en Angular que consume directamente servicios REST de Odoo. Revisar trazabilidad de cambios, defectos recientes y verificación por componente. |
| Proyecto C | PConst | Pendiente de confirmar | Proyecto de software a medida con backend en TypeScript y frontend en Angular. Revisar existencia de pruebas unitarias, registro de tareas y trazabilidad de cambios por componente. |

Los tres proyectos candidatos pertenecen a la línea de software a medida. No se clasifican como proyectos WordPress. Cuando un proyecto tenga más de un componente técnico, la línea base debe registrar evidencia por componente, pero la consolidación de indicadores se hará por proyecto y luego de forma agregada para la línea de software a medida.

Actualmente los componentes principales cuentan con repositorios en el GitHub institucional de PRX, aunque antes algunos no tenían repositorio institucional o estaban distribuidos en diferentes cuentas de GitHub. Esta regularización debe documentarse como antecedente de línea base. La ficha específica para revisar GitHub se encuentra en `tesis_ds/06_linea_base_github.md`.

## Lista de revisión por cada proyecto

Use esta lista para cada proyecto piloto. Si un dato no existe, registre “sin evidencia disponible” o “no existente al momento de la línea base”, según corresponda.

### 1. Datos mínimos del proyecto

- [ ] Nombre codificado del proyecto: `Proyecto A`, `Proyecto B` o `Proyecto C`.
- [ ] Tipo de sistema: aplicación web, API, módulo Odoo, sitio WordPress u otro.
- [ ] Componentes técnicos del proyecto: backend, frontend, Odoo, API, servicios REST u otros.
- [ ] Estado actual: activo, mantenimiento, pausado o cerrado.
- [ ] Desarrolladores involucrados, codificados como `D1`, `D2`, `D3`, etc.
- [ ] Responsable técnico o funcional, codificado.
- [ ] Ventana de observación usada para la línea base.

### 2. Evidencia desde el tablero interno de tareas implementado en Odoo

- [ ] Lista de tareas activas durante la ventana observada.
- [ ] Responsable asignado por tarea.
- [ ] Estado de cada tarea.
- [ ] Fecha de creación o actualización.
- [ ] Tareas reales mencionadas por desarrolladores que no estén registradas en Odoo.
- [ ] Captura, enlace interno o exportación como evidencia.

### 3. Evidencia desde GitHub institucional

- [ ] Existencia del repositorio institucional.
- [ ] Rama principal usada: `main`, `master`, `develop` u otra.
- [ ] Ramas creadas durante la ventana observada.
- [ ] Commits realizados durante la ventana observada.
- [ ] Mensajes de commits.
- [ ] Fusiones directas a la rama principal.
- [ ] Solicitudes de integración de cambios, si existen.
- [ ] Descripciones o evidencias de verificación dentro de esas solicitudes, si existen.
- [ ] Hash parcial de commits o identificadores internos suficientes para auditoría.

### 4. Evidencia sobre pruebas unitarias iniciales

- [ ] Existencia de carpeta o estructura de pruebas.
- [ ] Herramienta de pruebas usada o disponible.
- [ ] Comando para ejecutar pruebas.
- [ ] Resultado de ejecución.
- [ ] Componente crítico identificado.
- [ ] Razón de criticidad: lógica de negocio, integración, transformación de datos, defecto reciente u otro motivo documentado.
- [ ] Confirmación de si existe al menos una prueba unitaria ejecutable para el componente crítico.
- [ ] Si no existen pruebas, registrar explícitamente: “sin evidencia de pruebas unitarias ejecutables”.

### 5. Evidencia contextual

- [ ] Defectos recientes o correcciones urgentes asociadas al proyecto.
- [ ] Cambios sin tarea asociada.
- [ ] Commits sin contexto suficiente.
- [ ] Entregas o avances sin evidencia trazable.
- [ ] Dificultades declaradas por desarrolladores para registrar tareas, usar ramas, crear solicitudes de integración o escribir pruebas.
- [ ] Forma actual de demostrar avance ante clientes o responsables internos.

### 6. Evidencia que debe conservarse

- [ ] Capturas con datos sensibles ocultos.
- [ ] Identificadores internos de tareas.
- [ ] Hash parcial de commits.
- [ ] Conteo de ramas, commits y solicitudes de integración.
- [ ] Fecha y hora de extracción.
- [ ] Notas breves de entrevista codificadas.

## Plantilla breve por proyecto

Copie esta plantilla una vez por cada proyecto piloto.

| Campo | Valor |
|:--|:--|
| Código del proyecto | Pendiente |
| Nombre real del proyecto | Pendiente |
| Tipo de sistema | Pendiente |
| Estado actual | Pendiente |
| Ventana observada | Pendiente |
| Participantes codificados | Pendiente |
| Repositorio institucional | Pendiente |
| Rama principal | Pendiente |
| Total de tareas activas registradas | Pendiente |
| Tareas activas no registradas detectadas por entrevista | Pendiente |
| Total de ramas creadas | Pendiente |
| Total de commits | Pendiente |
| Total de solicitudes de integración | Pendiente |
| Solicitudes con evidencia mínima de verificación | Pendiente |
| Componente crítico revisado | Pendiente |
| Pruebas unitarias ejecutables | Pendiente |
| Defectos o correcciones urgentes identificadas | Pendiente |
| Evidencia almacenada | Pendiente |
| Observaciones | Pendiente |

## Consolidación posterior

Después de completar la revisión por proyecto, los datos deben consolidarse en los indicadores I1 a I9 definidos en `tesis_ds/06_diagnostico.md` y `tesis_ds/06_instrumentos_linea_base.md`. Esa consolidación permitirá cerrar E6 solo si los valores tienen evidencia trazable y fueron fijados antes de aplicar el marco.

## Nota de confidencialidad

No se deben nombrar desarrolladores en el perfil ni en la tesis. Use códigos como `D1`, `D2` y `D3`. Tampoco se deben publicar enlaces abiertos a repositorios privados de PRX; basta registrar identificadores internos, capturas con datos sensibles ocultos, hash parcial de commits y fechas de extracción suficientes para auditoría académica.
