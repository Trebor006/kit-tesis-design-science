# ALSIE — Informe Final de Investigación (IFI)

Documentos normativos del modelo institucional de **ALSIE** para el Informe Final de Investigación, convertidos a Markdown. Son la fuente de la forma que aplica el agente `traductor-alsie`.

## Documentos

| Archivo | Contenido | Uso |
|:--|:--|:--|
| `guia_ifi_contenido.md` | Qué debe contener, punto a punto, cada apartado del IFI: carátula, resumen, índice, introducción, capítulos I–IV, conclusiones, recomendaciones, referencias y anexos | Estructura y contenido de cada apartado |
| `indicadores_revision_ifi.md` | Criterios de evaluación por apartado y relaciones esenciales del documento | Autoevaluación del IFI |

## Notas

- El agente aplica **solo el nivel de maestría**: desarrolla el Capítulo III (Modelo teórico) y el Capítulo IV (Propuesta), e incluye en el perfil Hipótesis, Aporte teórico y Significación práctica.
- Quedan **excluidas** las variantes de Diplomado, Especialidad y Monografía, donde no se desarrolla el Modelo teórico y el perfil omite Hipótesis, Aporte teórico y Significación práctica.
- Los archivos `.docx` originales no se versionan. Para regenerar los Markdown:

```bash
pandoc "Guía  IFI_Contenido_2da Edición_2023_Cuerpo.docx" -f docx -t gfm --wrap=none -o guia_ifi_contenido.md
pandoc "Indicadores para la revisión del IFI_1ra Rev_junio 2024.docx" -f docx -t gfm --wrap=none -o indicadores_revision_ifi.md
```
