# Evidencia de variación en nombres de ramas

## Propósito

Este documento registra evidencia adicional de línea base sobre nombres de ramas usados en distintos repositorios o proyectos. La evidencia muestra que no existe una convención institucional homogénea para ramas principales, ramas de producción, ramas de validación o ramas de prueba. Esta variación respalda la necesidad de que el marco defina una convención mínima y un flujo de ramificación ligero.

## Evidencia observada

El tesista identificó nombres de ramas heterogéneos en distintos proyectos. Entre los nombres observados aparecen:

- `main`
- `Production`
- `production`
- `Prod`
- `Stage`
- `Staging`
- `staging`
- `stagin`
- `staging-server`
- `TEST`
- `Test`
- `test`
- `COSVI`
- `moriah`

## Interpretación

La evidencia muestra que los repositorios no comparten una convención única para nombrar ramas permanentes o de validación. En algunos casos se usa `Production`; en otros, `production` o `Prod`. Para ambientes de validación aparecen `Stage`, `Staging`, `staging`, `stagin`, `staging-server`, `TEST`, `Test` y `test`. También aparecen nombres específicos como `COSVI` o `moriah`, cuyo propósito no es evidente sin conocimiento contextual adicional.

Además de la variación de nombres, se observó ausencia de ramas esperadas en algunos repositorios: en ciertos casos no existe rama de validación equivalente a `stage`, en otros no existe rama de producción equivalente a `production`, y la rama por defecto varía entre `main` y ramas como `Production`. Esta inconsistencia debilita la trazabilidad organizacional porque un desarrollador o responsable técnico que no conoce el contexto de cada repositorio puede tener dificultad para identificar qué rama representa integración, validación o producción.

Esta variación no implica por sí sola que los proyectos estén mal construidos, pero sí evidencia ausencia de una política institucional de ramas permanentes. Por ello, la estandarización no debe limitarse a nombres de ramas de trabajo; también debe definir el significado de las ramas permanentes, cuál debe ser la rama por defecto y qué excepciones se permiten.

## Implicación para el marco

El marco deberá distinguir dos tipos de ramas:

1. **Ramas permanentes mínimas**, cuyo nombre y propósito deben estar documentados por repositorio. Estándar objetivo recomendado para PRX: `main` como rama por defecto y tronco de integración; `stage` como rama de validación cuando exista ambiente de pruebas; `production` como rama de producción solo cuando el mecanismo de despliegue del proyecto lo requiera.
2. **Ramas temporales de trabajo**, que deben seguir el formato `<tipo>/<codigo-tarea>-<descripcion-corta>`, por ejemplo `feat/CCC-4407-operador-contrato`.

La regla no debe imponer renombrar inmediatamente todas las ramas históricas, porque eso puede ser riesgoso y generar fricción. La primera versión del marco debe exigir que cada repositorio declare sus ramas permanentes oficiales, su propósito y la ruta de integración esperada. La estandarización del nombre puede aplicarse progresivamente en nuevos repositorios o cuando sea técnicamente seguro.

## Estándar objetivo propuesto para PRX

| Rama | Propósito | Regla inicial |
|:--|:--|:--|
| `main` | Rama por defecto y tronco de integración. | Debe existir en todo repositorio nuevo o normalizado. |
| `stage` | Validación previa a producción. | Debe existir cuando el proyecto tenga ambiente de pruebas o validación. |
| `production` | Código efectivamente desplegado o listo para producción. | Solo debe existir si el flujo de despliegue del proyecto requiere una rama separada de producción; si no, la producción debe identificarse por etiqueta, versión o registro de despliegue. |

Para repositorios existentes con ramas como `Production`, `Prod`, `Staging`, `TEST` o `test`, el marco debe registrar primero la equivalencia y luego planificar la normalización. La normalización no debe ejecutarse sin verificar dependencias de despliegue, automatizaciones, Odoo.sh u otros mecanismos que puedan depender del nombre actual de la rama.

## Relación con indicadores

| Indicador | Relación |
|:--|:--|
| I3. Cumplimiento de convención documentada de ramas | La evidencia refuerza que la línea base formal es 0 % en convención documentada de ramas. |
| I9. Evidencia trazable para respaldo de entregables | La variación de nombres dificulta seguir qué cambio llegó a qué ambiente si no existe documentación adicional. |

