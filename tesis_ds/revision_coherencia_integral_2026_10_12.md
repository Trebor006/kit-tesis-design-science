# Revisión integral de coherencia documental — 2026-10-12

## Propósito

Este documento registra la revisión de coherencia realizada sobre los archivos de trabajo de la tesis Design Science. La revisión contrasta los eslabones problema → objeto → campo → objetivo → pregunta → artefacto → evaluación → criterios → evidencia → contribución, y verifica que los documentos no presenten como validado aquello que todavía está pendiente de evidencia.

## Veredicto general

El conjunto documental es **coherente para un borrador avanzado de Design Science**, con una restricción central: todavía no debe presentarse como tesis evaluada ni como contribución validada. El artefacto está diseñado, construido documentalmente e instanciado parcialmente en PRX; la evaluación está planificada, pero falta evidencia de uso real en Central, verificación técnica, rediseño formativo y comparación posterior.

La cadena metodológica principal queda consistente:

```text
problema de diseño en PRX → brecha de investigación → marco como objeto de estudio → Central como primera aplicación → evaluación formativa y sumativa → principios de diseño candidatos
```

## Correcciones realizadas durante la revisión

| Hallazgo | Riesgo metodológico | Corrección aplicada |
|:--|:--|:--|
| `00_estado.md` todavía decía que E7e-E10 estaban pendientes. | Contradicción con los archivos ya creados. | Se actualizó el estado: E7e y E7f suficientes como versión inicial; E8 planificada; E9 y E10 iniciados, no cerrados. |
| `06_plan_evidencias_privadas.md` mantenía pendientes ya resueltos, como publicación de estándares y repositorio `.github`. | Confusión entre intervención ya documentada y evaluación pendiente. | Se actualizaron pendientes hacia `E-GH-INT-01`, `E-TEST-INT-01`, `E-FORM-01` y `E-SUM-01`. |
| `06_configuracion_github_propuesta.md` contenía una propuesta anterior con `dev` y `feature`. | Contradicción con el flujo vigente basado en tronco y tipos mínimos `feat`, `fix`, `hotfix`, `config`, `test`, `docs`, `refactor`. | Se marcó el archivo como antecedente histórico reemplazado parcialmente por `STD-GIT-001`, `STD-GIT-002` y `STD-GIT-003`. |
| `06_instrumentos_linea_base.md` tenía un salto de línea defectuoso con literal `` `r`n ``. | Error formal de documento. | Se corrigió el salto de línea en la guía de entrevista. |
| Documentos del perfil mantenían una muestra inicial de cinco desarrolladores. | Inconsistencia con la decisión posterior de concentrar la primera aplicación en Central. | Se alinearon `02_delimitacion.md`, `03_perfil_ds.md`, `03_perfil_ds_limpio.md`, `06_diagnostico.md`, `07a_alternativas.md` y `plan_cierre_borrador_para_alsie.md` con tres responsables técnicos codificados de Central. |
| El criterio I7 seguía formulado como pruebas unitarias por proyecto piloto. | Sobrealcance y contradicción con la primera aplicación centrada en Central. | Se reformuló I7 como verificación técnica mínima documentada en al menos un componente crítico de Central. |
| `matriz_coherencia.md` no reflejaba completamente E7e-E10. | Riesgo de trazabilidad incompleta. | Se actualizó el estado del artefacto, evaluación, evidencia y contribución preliminar. |

## Validación por eslabón de coherencia

| Eslabón | Estado revisado | Veredicto |
|:--|:--|:--|
| Problema de diseño | La línea de software a medida de PRX carece de una ruta ligera, común y verificable para gestión técnica trazable. | Coherente. |
| Problema de investigación | Brecha sobre cómo diseñar marcos ligeros de adopción inicial para equipos pequeños con baja estandarización. En el formato institucional se registrará como problema científico. | Coherente. |
| Objeto de estudio | El marco ligero progresivo, no PRX ni su proceso actual. | Coherente con Design Science. |
| Campo de acción | Adopción inicial de prácticas mínimas en equipos pequeños con baja estandarización; aplicación inicial en Central. | Coherente después de corrección. |
| Artefacto | Marco con componentes C0-C6, método, reglas, plantillas, estándares, indicadores y niveles de adopción. | Coherente. |
| Evaluación | Plan FEDS con ciclo formativo, rediseño y ciclo sumativo inicial. | Coherente, pero pendiente de ejecución. |
| Criterios | I1-I9 definidos; I7 ajustado a verificación técnica mínima en Central. | Coherente si el ajuste se mantiene como decisión previa a evaluación. |
| Evidencia | Línea base e intervención inicial disponibles; evaluación pendiente. | Coherente. |
| Contribución | Principios de diseño candidatos, no validados. | Coherente y prudente. |

## Correcciones o validaciones que todavía deben hacerse

1. Capturar `E-GH-INT-01`: primera solicitud de integración real en Central usando la convención de rama, título de solicitud, plantilla y vínculo con tarea.
2. Capturar `E-TEST-INT-01`: evidencia técnica documentada en al menos un componente crítico de Central.
3. Registrar `E-FORM-01`: fricciones reales y rediseño V1.1-Central.
4. Ejecutar `E-SUM-01`: comparación posterior contra línea base.
5. Actualizar `09_enlace_solucion.md` con cumplimiento real después de la evaluación.
6. Ajustar `10_contribucion_conclusiones.md` para convertir principios candidatos en principios sustentados por evidencia, sin exceder la generalización analítica permitida.

## Advertencia metodológica

La tesis todavía no puede afirmar que el marco mejora la trazabilidad ni que los principios están validados. Puede afirmar que existe un artefacto construido e instanciado parcialmente, con plan de evaluación listo. La diferencia no es formal: es la frontera entre una tesis Design Science defendible y una racionalización posterior de una mejora organizacional.

## Estado final de esta revisión

La documentación queda coherente para continuar con la aplicación real en Central. El siguiente paso no es seguir agregando teoría ni crear más estructura documental; el siguiente paso científico es producir evidencia de campo.
