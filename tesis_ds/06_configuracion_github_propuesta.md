# Propuesta de configuración estándar para GitHub institucional

> **Estado del documento:** histórico / reemplazado parcialmente. Este borrador fue útil para explorar una configuración inicial de GitHub, pero varias decisiones fueron ajustadas posteriormente por el artefacto V1.0-Central. La versión vigente del marco no adopta `dev` como rama permanente obligatoria ni usa `feature` como tipo inicial; la convención vigente se encuentra en `STD-GIT-001`, `STD-GIT-002` y `STD-GIT-003`, documentados en `07e_construccion_verificacion.md` y `07f_ficha_artefacto.md`. Este archivo debe leerse como antecedente de diseño, no como regla actual.

## Propósito

Este documento define una configuración mínima y homogénea para los repositorios de GitHub institucional de PRX vinculados a los proyectos piloto Central, Ansular y PConst. La configuración no debe aplicarse antes de cerrar la línea base de GitHub; primero se debe medir el estado actual y luego aplicar estas reglas como parte del marco ligero. Esta separación evita atribuir al artefacto mejoras que fueron realizadas antes de la evaluación.

## Decisión general

PRX debe mantener una sola organización institucional en GitHub y administrar el acceso mediante equipos, repositorios privados y permisos mínimos por proyecto. No se recomienda crear varias organizaciones para separar Odoo, frontend, backend o proyectos específicos, porque eso aumentaría la administración y fragmentaría la trazabilidad. La separación adecuada para este contexto es: una organización, equipos por rol o proyecto, repositorios privados y permisos explícitos por equipo.

La recomendación se apoya en la documentación de GitHub: los equipos permiten administrar acceso por grupos, asignar permisos de lectura o escritura y solicitar revisiones a equipos; las reglas de protección de ramas permiten exigir solicitudes de integración de cambios, revisiones y verificaciones antes de fusionar código; y los archivos `CODEOWNERS` permiten solicitar revisión automática a responsables de áreas de código (GitHub Docs, s. f.-a, s. f.-b, s. f.-c).

## Estructura de organización y equipos

| Elemento | Configuración propuesta | Justificación |
|:--|:--|:--|
| Organización | Una sola organización institucional de PRX en GitHub. | Centraliza trazabilidad, auditoría y gestión de acceso. |
| Repositorios | Privados por defecto. | Evita exposición de código, clientes y activos internos. |
| Equipos | Equipos por función y, cuando sea necesario, por proyecto. | Permite aplicar el principio de menor privilegio sin crear organizaciones separadas. |
| Acceso | Permisos por equipo, no por usuario individual salvo excepciones justificadas. | Reduce errores administrativos y facilita altas/bajas de desarrolladores. |
| Equipos sensibles | Usar equipos secretos cuando la composición del equipo no deba ser visible para toda la organización. | GitHub permite equipos visibles o secretos; los secretos solo son visibles para sus miembros y propietarios de la organización. |

## Equipos sugeridos

| Equipo | Acceso sugerido | Uso |
|:--|:--|:--|
| `software-a-medida` | Lectura o escritura según repositorio. | Equipo base de la línea de software a medida. |
| `odoo` | Escritura solo en repositorios o componentes Odoo autorizados. | Cambios en módulos Odoo y servicios relacionados. |
| `backend` | Escritura en API C# y backend TypeScript autorizados. | Desarrollo de servicios y lógica de servidor. |
| `frontend` | Escritura en frontends Angular autorizados. | Desarrollo de interfaz y consumo de servicios. |
| `responsables-tecnicos` | Mantenimiento o administración limitada según necesidad. | Revisión, aprobación y soporte técnico. |

Si un desarrollador de Odoo no debe ver proyectos que no le corresponden, la condición necesaria es que esos repositorios sean privados y que el equipo `odoo` no tenga acceso a ellos. La visibilidad se controla por permisos de repositorio dentro de la organización, no creando repositorios personales ni cuentas dispersas.

## Acceso eventual de clientes

Si PRX necesita que algunos clientes puedan ver o auditar repositorios específicos, la opción inicial recomendada es mantener los repositorios dentro de la organización institucional de PRX y otorgar acceso limitado solo a los repositorios correspondientes. No se recomienda crear una organización distinta por cliente como regla inicial, porque eso fragmentaría la trazabilidad, duplicaría la administración y haría más difícil sostener un estándar común de ramas, solicitudes de integración y verificación.

La configuración debe distinguir entre acceso interno y acceso externo. Los clientes no deberían tener permisos administrativos ni capacidad de modificar ramas protegidas. En la mayoría de los casos, el acceso de cliente debe ser de solo lectura o, si el contrato lo exige, acceso limitado para revisar solicitudes de integración, incidencias o documentación. La decisión concreta dependerá de acuerdos de confidencialidad, propiedad intelectual, soporte y responsabilidad contractual; por ello, para esta tesis se registra como una extensión futura del marco y no como una regla obligatoria de la primera versión.

| Escenario | Configuración recomendada | Justificación |
|:--|:--|:--|
| Cliente solo necesita auditar avance o código entregado. | Acceso de lectura al repositorio privado específico. | Permite visibilidad sin riesgo de cambios no controlados. |
| Cliente participa revisando entregables técnicos. | Acceso limitado al repositorio específico y revisión mediante solicitudes de integración o incidencias. | Mantiene trazabilidad sin abrir otros proyectos. |
| Cliente requiere propiedad o administración completa del repositorio. | Evaluar repositorio bajo organización del cliente o transferencia formal. | Ya no es solo colaboración operativa; afecta propiedad, soporte y gobierno. |
| Varios clientes con proyectos separados. | Mantener repositorios privados separados y permisos específicos por cliente. | Evita que un cliente vea activos de otro cliente. |

Para la primera versión del marco, este punto no se implementará antes de la medición. Se documentará como decisión de diseño futura o condición de contorno, porque el problema actual se concentra en estandarizar el uso interno de GitHub dentro de la línea de software a medida de PRX.

## Ramas estándar exploratorias

> Esta sección queda como antecedente. La decisión vigente para V1.1-Central usa `main` como tronco de integración, `Stage` como validación cuando exista ambiente y `Production` solo cuando el mecanismo de despliegue lo requiera. `dev` no forma parte obligatoria de la versión mínima. La versión vigente se formaliza en `07e_STD-GIT-001_enmienda_v1_1.md`.

| Rama | Propósito | Regla |
|:--|:--|:--|
| `main` | Versión estable o producción. | Protegida; nadie debe integrar cambios directamente. |
| `stage` | Validación previa a producción o ambiente de pruebas de aceptación. | Protegida; recibe cambios mediante solicitud de integración desde `dev` o ramas de versión. |
| `dev` | Integración de trabajo en curso validado mínimamente. | Protegida de eliminación y fuerza de empuje; cambios mediante solicitud de integración. |

Esta estructura solo es recomendable si PRX efectivamente diferencia ambientes de desarrollo, preproducción y producción. Si un proyecto no tiene ambiente de preproducción, mantener `stage` puede convertirse en una rama decorativa; en ese caso debe documentarse como deuda de proceso o excluirse temporalmente de la regla operacional.

## Flujo mínimo de integración exploratorio

> Esta sección no representa la decisión vigente. El flujo vigente es flujo basado en tronco: ramas temporales cortas desde `main`, solicitud de integración hacia `main`, y promoción posterior a `Stage` o `Production` si corresponde.

1. El desarrollador crea una rama de trabajo desde `dev`.
2. El cambio se desarrolla en la rama de trabajo.
3. El desarrollador crea una solicitud de integración hacia `dev`.
4. La solicitud debe incluir descripción, tarea relacionada y evidencia mínima de verificación.
5. Otro desarrollador o responsable técnico revisa la solicitud.
6. La integración hacia `dev`, `stage` o `main` se realiza solo mediante solicitud de integración aprobada.

## Convención de nombres de ramas exploratoria

> La convención vigente usa tipos mínimos `feat`, `fix`, `hotfix`, `config`, `test`, `docs` y `refactor`, con formato `<tipo>/<codigo-tarea>-<descripcion-corta>`. Ver `STD-GIT-001`.

Formato propuesto:

```text
<tipo>/<codigo-tarea>-<descripcion-corta>
```

Tipos permitidos:

| Tipo | Uso | Ejemplo |
|:--|:--|:--|
| `feature` | Nueva funcionalidad. | `feature/ODOO-123-registro-cliente` |
| `fix` | Corrección de defecto. | `fix/API-045-validacion-token` |
| `hotfix` | Corrección urgente sobre producción. | `hotfix/PCONST-018-error-login` |
| `refactor` | Mejora interna sin cambio funcional esperado. | `refactor/ANG-077-limpiar-servicio-auth` |
| `test` | Incorporación o ajuste de pruebas. | `test/API-052-pruebas-calculo` |
| `docs` | Documentación técnica. | `docs/ANS-010-guia-instalacion` |

Reglas mínimas:

- usar minúsculas;
- separar palabras con guion medio;
- incluir identificador de tarea cuando exista;
- no usar nombres personales en ramas;
- no crear ramas genéricas como `cambios`, `prueba`, `robert`, `nuevo` o `final`.

## Convención de commits exploratoria

> La convención vigente usa `<tipo>(<codigo-tarea>): <descripcion-breve>`, donde el campo entre paréntesis representa el código de tarea. Ver `STD-GIT-003`.

Formato propuesto:

```text
<tipo>(<alcance>): <descripcion breve>
```

Ejemplos:

```text
feat(api): agregar validación de token
fix(odoo): corregir cálculo de saldo pendiente
test(pconst): agregar prueba de cálculo de mora
refactor(frontend): separar servicio de autenticación
docs(repo): documentar ejecución local
```

Tipos permitidos:

| Tipo | Significado |
|:--|:--|
| `feat` | Nueva funcionalidad. |
| `fix` | Corrección de defecto. |
| `test` | Pruebas. |
| `refactor` | Mejora interna sin cambio funcional esperado. |
| `docs` | Documentación. |
| `chore` | Tarea técnica menor. |
| `build` | Cambios de construcción o dependencias. |

Reglas mínimas:

- escribir mensajes breves y comprensibles;
- evitar commits como `update`, `cambios`, `fix`, `final`, `prueba` o `asd`;
- asociar el commit con una tarea o solicitud cuando sea posible;
- evitar mezclar cambios no relacionados en un mismo commit.

## Protección de ramas

| Rama | Protección mínima |
|:--|:--|
| `main` | Exigir solicitud de integración, al menos una aprobación, conversación resuelta, bloqueo de eliminación y bloqueo de fuerza de empuje. |
| `stage` | Exigir solicitud de integración, al menos una aprobación y bloqueo de fuerza de empuje. |
| `dev` | Exigir solicitud de integración y bloqueo de fuerza de empuje; aprobación obligatoria cuando el cambio afecte componentes críticos. |

Cuando existan pruebas automatizadas, se debe exigir que las verificaciones pasen antes de fusionar a `main` y `stage`. Si todavía no existen pruebas, no se debe fingir control automático; se debe exigir evidencia manual mínima en la solicitud de integración hasta que el proyecto tenga pruebas ejecutables.

## Plantilla mínima de solicitud de integración

Crear un archivo `.github/pull_request_template.md` con el siguiente contenido base:

```markdown
## Cambio realizado

Describa brevemente qué se modificó.

## Tarea relacionada

Indique el identificador de Odoo u otro registro interno.

## Tipo de cambio

- [ ] Nueva funcionalidad
- [ ] Corrección
- [ ] Refactorización
- [ ] Prueba
- [ ] Documentación

## Evidencia de verificación

- [ ] Se ejecutó prueba automatizada
- [ ] Se realizó verificación manual
- [ ] Se adjunta captura o registro
- [ ] No aplica, con justificación

## Riesgo del cambio

Explique si el cambio afecta autenticación, pagos, reportes, integraciones, datos o lógica crítica.
```

## Archivo CODEOWNERS

Cuando existan responsables técnicos claros, crear `.github/CODEOWNERS` para solicitar revisión automática. Ejemplo general:

```text
* @prx/responsables-tecnicos
*.cs @prx/backend
*.ts @prx/frontend
*.py @prx/odoo
/.github/ @prx/responsables-tecnicos
```

El archivo debe ajustarse a la estructura real de cada repositorio. GitHub exige que los usuarios o equipos definidos como propietarios de código tengan permiso de escritura sobre el repositorio (GitHub Docs, s. f.-c).

## Configuración adicional recomendada

| Configuración | Recomendación | Razón |
|:--|:--|:--|
| Desactivar eliminación de ramas protegidas | Sí. | Evita pérdida de ramas críticas. |
| Bloquear fuerza de empuje en ramas protegidas | Sí. | Evita reescritura riesgosa del historial compartido. |
| Fusionar con squash | Recomendado para equipos pequeños. | Mantiene historial más limpio y facilita revertir cambios. |
| Exigir resolución de conversaciones | Sí en `main` y `stage`. | Evita fusionar cambios con observaciones pendientes. |
| Revisiones obligatorias | Una aprobación mínima al inicio. | Es viable para equipo pequeño; más aprobaciones podrían frenar el trabajo. |
| Verificaciones automáticas | Exigirlas solo cuando existan pruebas o construcción automatizada. | Evita bloquear al equipo con una regla que todavía no puede cumplir. |
| Secretos y variables | Usar secretos del repositorio u organización, no archivos versionados. | Evita exponer credenciales. |
| Archivo `README.md` por repositorio | Sí. | Permite instalación, ejecución local y verificación mínima. |
| Archivo `.gitignore` por tecnología | Sí. | Evita subir binarios, dependencias, credenciales o archivos temporales. |

## Criterio de aplicación gradual

Para no convertir el marco en una carga inviable, la adopción debe ser gradual:

1. Medir línea base actual de GitHub.
2. Crear o confirmar ramas `main`, `stage` y `dev` solo donde correspondan a ambientes reales.
3. Activar protección mínima de `main` y `stage`.
4. Introducir convención de ramas y commits.
5. Exigir solicitudes de integración con plantilla.
6. Incorporar `CODEOWNERS` cuando existan responsables técnicos definidos.
7. Añadir verificaciones automáticas cuando existan pruebas ejecutables.

## Origen práctico de la propuesta

La propuesta no parte de una práctica institucional ya consolidada. Surge de prácticas aisladas que el tesista comenzó a aplicar en componentes bajo su responsabilidad, especialmente en Central Frontend, donde introdujo uso de rama de trabajo, solicitud de integración, referencia al ticket y fusión mediante `squash merge` después de recibir un repositorio con trazabilidad inicial mínima. Ese antecedente sirve como ejemplo práctico, pero no debe confundirse con línea base institucional: el objetivo del marco es transformar prácticas individuales y dispersas en reglas comunes para el equipo de desarrollo de software, responsables técnicos y jefes de proyecto.

Esta distinción es metodológicamente importante. Si la tesis presentara esas prácticas como ya existentes en toda la organización, debilitaría el diagnóstico. Si, en cambio, las presenta como aprendizaje local que motiva el diseño del artefacto, fortalece la lógica de Design Science: el artefacto busca formalizar, adaptar y evaluar una forma de trabajo que hoy depende de personas y no de un estándar compartido.

## Riesgos de sobreconfiguración

La configuración no debe intentar replicar un proceso corporativo pesado. Para una línea de software a medida con baja estandarización, el objetivo inicial es lograr trazabilidad mínima y verificación básica. Exigir firmas criptográficas, múltiples aprobaciones, cola de integración o reglas complejas desde el primer ciclo puede producir rechazo del equipo y afectar la aplicabilidad del artefacto.

## Referencias

GitHub Docs. (s. f.-a). *About organization teams*. Recuperado el 1 de octubre de 2026, de https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams

GitHub Docs. (s. f.-b). *About protected branches*. Recuperado el 1 de octubre de 2026, de https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/about-protected-branches

GitHub Docs. (s. f.-c). *About code owners*. Recuperado el 1 de octubre de 2026, de https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners

GitHub Docs. (s. f.-d). *About rulesets*. Recuperado el 1 de octubre de 2026, de https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets
