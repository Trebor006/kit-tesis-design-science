# Kit de Tesis con Design Science

Asistente para tesistas de **Maestría en Ingeniería de Software** que desarrollan su tesis bajo el paradigma de **Design Science**.

El kit incluye un agente de IA para [opencode](https://opencode.ai) que actúa como director de tesis: hace las preguntas clave, exige evidencia, bloquea los errores clásicos de una tesis de Design Science y acompaña al tesista desde la elección del tema hasta las conclusiones con principios de diseño validados.

---

## ¿Qué resuelve?

La mayoría de las tesis de Ingeniería de Software fracasan científicamente por una razón que no es técnica: el tesista construye un artefacto (sistema, herramienta, modelo) sin articular qué conocimiento transferible genera construirlo. El código compila, el sistema funciona, y el capítulo de conclusiones no puede decir qué se aprendió más allá de que "el sistema funciona". Este agente existe para evitar que esa oportunidad se pierda.

El agente no escribe la tesis por el estudiante. Lo guía, lo interroga y lo obliga a tomar decisiones fundamentadas.

---

## Requisitos

- [opencode](https://opencode.ai) instalado.
- Acceso a un modelo de lenguaje configurado en opencode.
- `git` (para clonar y actualizar).

---

## Instalación

```bash
git clone <URL-DEL-REPOSITORIO> mi-tesis
cd mi-tesis
opencode
```

Al abrir opencode dentro de la carpeta, el agente `asesor-tesis-ds` queda seleccionado por defecto (así lo define `opencode.json`). Si tu opencode no lo selecciona automáticamente, cámbialo al agente **asesor-tesis-ds** (atajo de agentes en la interfaz).

No hay que instalar nada más ni configurar rutas: el agente y su biblioteca de referencia viajan dentro del repositorio.

---

## Cómo trabaja el agente

El agente recorre **11 etapas** y no avanza a la siguiente hasta cerrar la anterior:

| Etapa | Qué se trabaja |
|:--|:--|
| E0 | Encuadre: estándares de maestría y reglas de trabajo |
| E1 | Área de experiencia mayor y propuesta de temas |
| E2 | Delimitación: problema de diseño, problema de investigación, objeto de estudio, campo de acción y propuesta |
| E3 | Perfil de investigación en Design Science |
| E4 | Marco teórico que sustenta el objeto de estudio |
| E5 | Estado del arte sobre la propuesta y los artefactos existentes |
| E6 | Diagnóstico con indicadores y línea base |
| E7 | Diseño y desarrollo del artefacto |
| E8 | Evaluación (formativa con rediseño + sumativa) |
| E9 | Enlace propuesta ↔ solución (matriz de trazabilidad) |
| E10 | Contribución y conclusiones (principios de diseño) |

Los productos se van escribiendo en una carpeta `tesis_ds/` dentro de tu proyecto, un archivo por etapa. La primera vez que abres una sesión nueva, el agente lee `tesis_ds/00_estado.md` y retoma donde quedaron.

La carpeta `tesis_ds/` está en `.gitignore`: es tu trabajo personal y no se sube al repositorio.

---

## Prompts específicos (copiar y pegar)

### Arranque en frío

```
Actúa como mi asesor de tesis. Quiero iniciar mi tesis de maestría en Ingeniería
de Software con el enfoque de Design Science. Estoy empezando de cero y no tengo
tema definido. Guíame.
```

### Etapa 1 — Área de experiencia

```
Mi área de experiencia mayor es [por ejemplo, pruebas de software]. Trabajo desde
hace [N] años en [tipo de organización], con [tecnologías y roles]. Tengo acceso a
[contexto real] durante [tiempo]. Ayúdame a explorar temas de investigación en
Design Science para esta área.
```

### Etapa 2 — Delimitación

```
Ya me interesa el tema [tema]. Ayúdame a delimitar con claridad el problema de
diseño, el problema de investigación, el objeto de estudio, el campo de acción y la
propuesta, y a distinguir cada uno.
```

### Etapa 3 — Perfil de investigación

```
Con lo anterior, redacta el perfil de investigación en Design Science y señala qué
secciones están débiles o ausentes.
```

### Etapa 4 — Marco teórico

```
Construye el marco teórico que sustenta el objeto de estudio. Busca teoría real y
existente, preferentemente libros y fuentes de los últimos 5 años, y verifica cada
referencia antes de citarla.
```

### Etapa 5 — Estado del arte

```
Elabora el estado del arte sobre la propuesta: qué soluciones y artefactos existen
para esta clase de problema, cómo se evaluaron y qué limitaciones tienen. Justifica
la novedad de la propuesta con evidencia.
```

### Etapa 6 — Diagnóstico

```
Ayúdame a definir los indicadores del diagnóstico (definición, fuente, línea base y
valor esperado) y a fijar los criterios de éxito antes de construir el artefacto.
```

### Etapa 7 — Diseño y desarrollo

```
Ayúdame a derivar los requisitos del artefacto y a documentar las decisiones de
diseño y sus versiones (prototipo exploratorio, experimental y operacional).
```

### Etapa 8 — Evaluación

```
Diseña la estrategia de evaluación con el marco FEDS: un ciclo formativo con
rediseño y un ciclo sumativo. Define la muestra, los instrumentos y las amenazas a
la validez.
```

### Etapa 9 — Enlace propuesta ↔ solución

```
Ayúdame a enlazar la propuesta con la solución del problema mediante la matriz de
trazabilidad, y dime qué afirmaciones no tienen evidencia suficiente.
```

### Etapa 10 — Conclusiones

```
Formula la contribución como principios de diseño (objetivo, contexto, mecanismo y
principio), con condiciones de contorno y amenazas a la validez. Recuérdame que el
nivel es de maestría.
```

### Continuar una sesión

```
Lee tesis_ds/00_estado.md y dime en qué etapa estamos, qué se cerró y qué sigue.
```

### Revisión crítica

```
Revisa críticamente tesis_ds/03_perfil_ds.md contra los gates de Design Science y
señala los tres problemas más graves y los tres mayores aciertos.
```

---

## Estructura del repositorio

```text
.
├── README.md                          Este documento
├── opencode.json                      Configuración que activa el agente por defecto
├── .gitignore                         Ignora tesis_ds/ y archivos temporales
├── .opencode/
│   └── agent/
│       └── asesor-tesis-ds.md         El agente (prompt completo)
├── referencias/                       Libro de Design Science (16 capítulos, .md)
│   ├── ds_ch00_prefacio.md
│   ├── ds_ch01_fundamentos.md
│   └── ... ds_ch15_referencias.md
└── plantillas/                        Esqueletos opcionales de trabajo
    ├── 00_estado.md
    ├── matriz_coherencia.md
    └── referencias.md
```

---

## Reglas del agente (resumen)

- Habla en **español académico de Bolivia**, con trato formal de "usted".
- Calibra todo al **nivel de maestría**: contribución mediante **principios de diseño validados**, con al menos un ciclo de evaluación formativa con rediseño y un ciclo sumativo.
- Bloquea el sobrealcance (teoría de diseño sin evidencia multi-contexto) y el subalcance (solo el artefacto, sin principios transferibles).
- Trabaja con terminología de Design Science y, cuando corresponde, anota su traducción institucional: el **problema de investigación** se registrará en el formato institucional como **"problema científico"**.
- Hace explícita la resignificación de Design Science: el **objeto de estudio es el artefacto propuesto**, no el proceso del contexto.
- Nunca inventa referencias. Busca y verifica fuentes reales; lo no verificable se marca como `[por verificar]`.
- Exige que los criterios de éxito y los indicadores se definan antes de construir el artefacto.
- No escribe la tesis por el estudiante: co-construye sobre decisiones que él ya tomó y puede defender.
- Todos los entregables y artefactos se producen **siempre en archivos Markdown (`.md`)**.
- Las citas y referencias siguen **APA 7 de forma obligatoria** en todos los archivos y etapas.

---

## Preguntas frecuentes

**¿Sirve para doctorado?** No. El agente está calibrado exclusivamente para maestría. Un doctorado necesita evidencia en al menos dos contextos independientes y una teoría de diseño, que este agente deliberadamente no exige.

**¿Reemplaza al director de tesis?** No. Es una herramienta de acompañamiento metodológico. Las decisiones académicas y la dirección formal recaen en el director y el comité del programa.

**¿El agente inventa bibliografía?** No. Tiene la instrucción explícita de verificar cada fuente y de marcar como `[por verificar]` lo que no pueda confirmar.

**¿Puedo usarlo para mi plantilla institucional?** Este kit produce el trabajo en clave de Design Science. La traducción a la plantilla institucional (por ejemplo, con los apartados de problema científico, objeto de estudio y campo de acción) se hará con un agente de traducción que se desarrollará en una fase posterior.

**¿En qué formato entrega el agente?** Siempre en archivos Markdown (`.md`), con citas y referencias en APA 7. No genera Word ni PDF directamente; si necesitas otro formato, se convierte después a partir del `.md`.

**¿Cómo actualizo el kit?** Con `git pull` dentro de la carpeta. Tu carpeta `tesis_ds/` no se ve afectada porque está ignorada por Git.

---

## Licencia y derechos

El contenido del libro de Design Science incluido en `referencias/` es obra de Luis Roberto Pérez Rios, Ph.D., y se distribuye en este repositorio con fines académicos y educativos. El código de configuración y el agente pueden reutilizarse citando la fuente.

© Luis Roberto Pérez Rios, Ph.D.
