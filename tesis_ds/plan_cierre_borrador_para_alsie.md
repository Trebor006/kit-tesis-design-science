# Plan de cierre del borrador para traducción al modelo ALSIE

## Propósito

Este documento define qué falta para convertir el avance Design Science en un borrador de investigación suficientemente completo para su traducción posterior al modelo documental ALSIE. No reemplaza la traducción institucional; ordena las acciones mínimas para que la tesis no llegue a ALSIE solo con perfil y propuesta, sino con construcción, aplicación inicial, evaluación y contribución preliminar defendible.

## Veredicto de estado

La propuesta ya está formulada y diseñada: E7a, E7b, E7c y E7d están suficientes para el hito. Lo que falta no es seguir diseñando la propuesta en abstracto, sino **aplicarla, generar evidencia y redactar resultados preliminares**. Sin esa evidencia, el documento puede traducirse como perfil avanzado, pero no como borrador de investigación completo.

## Mínimo necesario antes de traducir a ALSIE

| Bloque | Estado actual | Falta mínima | Archivo de salida |
|:--|:--|:--|:--|
| Propuesta del artefacto | Diseñada preliminarmente. | Integrar construcción/aplicación real de V1.0-Central. | `07e_construccion_verificacion.md` |
| Ficha del artefacto | Parcial, distribuida entre E7c, E7d y plantilla. | Consolidar una ficha reproducible del marco. | `07f_ficha_artefacto.md` |
| Evidencia privada | Planificada, no levantada completamente. | Capturas y códigos de evidencia priorizados. | `06_plan_evidencias_privadas.md` y carpeta privada de evidencias |
| Resultados formativos | Pendiente. | Al menos un ciclo real de uso con fricciones y rediseño. | `08_evaluacion.md` |
| Resultados sumativos iniciales | Pendiente. | Comparación posterior contra línea base en Central. | `08_evaluacion.md` |
| Enlace problema-solución | Pendiente. | Matriz problema → requisito → decisión → evidencia → cumplimiento. | `09_enlace_solucion.md` |
| Contribución | Formulada, no validada. | Principios de diseño preliminares proporcionales a evidencia. | `10_contribucion_conclusiones.md` |

## Secuencia de trabajo recomendada

### Paso 1. Levantar evidencias mínimas

Priorizar estas evidencias antes de redactar resultados:

| Código | Evidencia | Razón |
|:--|:--|:--|
| `E-GH-ORG-01` | Repositorio organizacional `.github`, archivo `pull_request_template.md` y prueba de que aparece en una solicitud nueva. | Demuestra construcción de la instanciación PRX de la plantilla. |
| `E-GH-BASE-02` | Ramas permanentes heterogéneas y equivalencias por repositorio. | Justifica RQ5.1 y la regla de ramas permanentes. |
| `E-GH-BASE-03` | Solicitudes de integración de línea base sin evidencia mínima de verificación. | Justifica I6 y la plantilla obligatoria. |
| `E-ODOO-BASE-01` | Tareas de Central o evidencia de visibilidad parcial. | Justifica I1 y tarea válida. |
| `E-TEST-BASE-01` | Evidencia de pruebas existentes o ausencia verificable. | Controla la debilidad de I7. |
| `E-GH-INT-01` | Primera solicitud nueva usando la plantilla. | Evidencia intervención y demostración. |
| `E-TEST-INT-01` | Verificación técnica de al menos un componente crítico de Central. | Evidencia verificación mínima. |

### Paso 2. Redactar E7e construcción y verificación interna

`07e_construccion_verificacion.md` debe registrar qué se construyó/aplicó realmente:

- repositorio `.github` organizacional;
- plantilla de solicitud de integración;
- comunicación o aplicación de convención de ramas y commits;
- declaración de ramas permanentes de Central;
- solicitud de integración posterior a la intervención;
- evidencia de verificación técnica;
- problemas encontrados y decisiones tomadas.

### Paso 3. Crear E7f ficha del artefacto

`07f_ficha_artefacto.md` debe funcionar como anexo reproducible. Debe consolidar objetivo, alcance, componentes C0-C6, reglas, plantilla, niveles, indicadores, aplicación PRX y limitaciones. Otro investigador debe poder entender el marco sin revisar toda la conversación.

### Paso 4. Ejecutar evaluación formativa

La evaluación formativa debe responder una pregunta concreta: ¿la versión V1.0-Central puede usarse en trabajo real sin introducir fricción excesiva y produce evidencia mínima? Debe registrar fricciones, ajustes y justificación del rediseño V1.1-Central.

### Paso 5. Ejecutar evaluación sumativa inicial

La evaluación sumativa debe comparar un periodo posterior contra la línea base. No necesita demostrar transformación total de PRX; debe medir cambio en Central con los indicadores definidos antes de construir.

### Paso 6. Redactar enlace y contribución

Después de la evaluación, se redactan `09_enlace_solucion.md` y `10_contribucion_conclusiones.md`. Antes de tener resultados, esos documentos solo pueden contener estructura y contribución esperada, no conclusiones finales.

## Qué no debe hacerse

- No traducir todavía como tesis completa si no existe evidencia de aplicación.
- No presentar el repositorio `.github` como línea base; es intervención.
- No declarar que el marco fue validado si solo se creó la plantilla.
- No inflar GitHub Actions como núcleo del artefacto; es mejora posterior o apoyo técnico.
- No generalizar a todos los equipos de Ingeniería de Software; la afirmación permitida es analítica y condicionada.

## Criterio de listo para traducción ALSIE

El borrador estará listo para traducción institucional cuando existan, como mínimo:

1. Perfil y matriz de coherencia actualizados.
2. Diagnóstico con línea base y evidencias privadas codificadas.
3. Artefacto diseñado y ficha reproducible.
4. Construcción/aplicación documentada de V1.0-Central.
5. Al menos una evaluación formativa con rediseño documentado.
6. Evaluación sumativa inicial proporcional al alcance.
7. Matriz de trazabilidad problema → requisito → decisión → evidencia → cumplimiento.
8. Principios de diseño preliminares con condiciones de contorno.

Si faltan los puntos 4, 5 y 6, el documento puede traducirse como perfil/propuesta avanzada, pero no como borrador de investigación completo.
