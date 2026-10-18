# Enmienda V1.1 — STD-GIT-001: Convención mínima de ramas

## Decisión de actualización

La convención institucional vigente de ramas permanentes en PRX es:

```text
main
Stage
Production
```

La decisión se tomó el 2026-10-17 después de revisar los repositorios Odoo disponibles. Según la declaración del tesista, aproximadamente el 90 % de esos repositorios usa `main`, `Stage` y `Production`. Las capturas privadas disponibles corroboran que estas denominaciones existen en el contexto de PRX; el porcentaje declarado no se presenta como medición independiente hasta contar con un inventario reproducible de repositorios.

## Regla vigente

| Rama | Propósito institucional | Aplicación |
|:--|:--|:--|
| `main` | Rama por defecto y tronco de integración. | Obligatoria para repositorios nuevos y objetivo de normalización progresiva para repositorios existentes. |
| `Stage` | Rama de validación previa a producción. | Obligatoria solo cuando el repositorio tenga ambiente o mecanismo real de validación. |
| `Production` | Rama asociada a producción. | Obligatoria solo cuando el despliegue requiera una rama separada de producción. |

Las mayúsculas de `Stage` y `Production` son parte de la convención. No deben sustituirse por `stage` o `production` en nuevos repositorios ni en cambios de configuración posteriores.

## Compatibilidad con repositorios existentes

La enmienda no ordena renombramientos inmediatos. Para un repositorio histórico con `master`, `Prod`, `production`, `Staging`, `test` u otra denominación, el responsable debe primero declarar: rama actual, propósito, dependencias de despliegue, equivalencia con la convención vigente y plan de transición. No se renombrará una rama conectada con Odoo.sh, automatizaciones o despliegues sin verificación técnica previa.

`master` se considera rama heredada. Cuando sea técnicamente seguro, deberá reemplazarse por `main`; mientras tanto, su equivalencia y condiciones de retiro deben documentarse.

## Flujo de integración

El marco mantiene el flujo basado en tronco. Las ramas temporales parten de `main`, se integran a `main` mediante solicitud de integración y se eliminan después de fusionarse. La promoción a `Stage` o `Production` ocurre solo cuando el mecanismo real de despliegue del repositorio lo exige; estas ramas no son espacios de desarrollo directo.

Las ramas temporales conservan el formato:

```text
<tipo>/<codigo-tarea>-<descripcion-corta>
```

## Acción institucional requerida

Esta enmienda debe incorporarse en SharePoint como versión 1.1 de `STD-GIT-001 — Convención mínima de ramas`. La captura `Tarea central - add stage and production branch.png` debe clasificarse como evidencia de intervención de configuración de ramas permanentes, no como evidencia de evaluación de la tarea `CCC-7336`.

## Estado

La enmienda deja sin efecto, para documentos vigentes, la formulación anterior que usaba `stage` y `production` en minúscula como estándar objetivo. No altera la línea base histórica, donde esas y otras variantes siguen siendo evidencia de heterogeneidad previa.
