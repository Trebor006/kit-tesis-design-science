# Plantilla mínima obligatoria de solicitud de integración

## Propósito

Esta plantilla forma parte del artefacto **Marco ligero progresivo para la gestión técnica trazable del trabajo de desarrollo en equipos pequeños con baja estandarización**. Su función es convertir cada solicitud de integración en evidencia verificable de trazabilidad, validación y verificación mínima del cambio. En la tesis, la plantilla deberá citarse dentro del diseño del artefacto y presentarse completa como anexo operativo.

## Uso previsto

La plantilla debe incorporarse en los repositorios donde se aplique el marco como archivo de plantilla de solicitud de integración. En GitHub, la instanciación recomendada es `.github/pull_request_template.md`. Si el repositorio usa otra plataforma, debe adaptarse al mecanismo equivalente de solicitudes de integración.

## Plantilla

```markdown
## Tarea relacionada

Código de tarea:
Enlace o referencia:

## Descripción del cambio

¿Qué se cambió y por qué?

## Tipo de cambio

- [ ] feat
- [ ] fix
- [ ] hotfix
- [ ] config
- [ ] test
- [ ] docs
- [ ] refactor

## Componentes afectados

- [ ] Odoo Backend
- [ ] API
- [ ] Frontend
- [ ] Base de datos
- [ ] Configuración / despliegue
- [ ] Otro:

## Riesgo del cambio

- [ ] Bajo
- [ ] Medio
- [ ] Alto

Justificación si es medio o alto:

## Verificación realizada

Método:

- [ ] Prueba manual documentada
- [ ] Prueba unitaria
- [ ] Prueba de integración
- [ ] Prueba de API
- [ ] Construcción / compilación
- [ ] No aplica, con justificación

Evidencia:

## Validación

- [ ] Revisado por otra persona
- [ ] Auto-validación documentada
- [ ] Validación automática
- [ ] Excepción documentada

Validador o justificación:

## Checklist mínima

- [ ] Rama incluye código de tarea.
- [ ] Commits incluyen código de tarea.
- [ ] No incluye credenciales ni datos sensibles.
- [ ] Listo para `squash merge`.
- [ ] Rama se eliminará después de fusionar.
```

## Criterio de validez de la solicitud

Una solicitud de integración se considera válida para el marco cuando completa, al menos, los campos de tarea relacionada, descripción, tipo de cambio, componentes afectados, riesgo, verificación, evidencia y validación. Una solicitud que solo contiene título y commits puede ser trazable, pero no cuenta como solicitud válida si no permite verificar qué se cambió, por qué se cambió y cómo fue validado.

## Relación con indicadores

| Indicador | Relación con la plantilla |
|:--|:--|
| I3. Cumplimiento de convención de ramas | La lista mínima verifica que la rama incluya código de tarea. |
| I4. Cumplimiento de convención de commits | La lista mínima verifica que los commits incluyan código de tarea. |
| I5. Cambios integrados mediante solicitudes de integración | La plantilla estructura la solicitud como producto de trabajo observable. |
| I6. Solicitudes con evidencia mínima de verificación | La sección de verificación y evidencia permite evaluar este indicador. |
| I9. Evidencia trazable para respaldo de entregables | La plantilla conecta tarea, cambio, validación y evidencia. |

## Condición de frontera

En componentes atendidos por un solo desarrollador, la auto-validación documentada se acepta como excepción explícita. Esta excepción no debe interpretarse como revisión independiente; debe registrar la evidencia mínima de verificación y la justificación de ausencia de revisor distinto del autor.
