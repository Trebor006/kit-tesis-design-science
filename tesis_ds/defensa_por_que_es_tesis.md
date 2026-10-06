# Defensa conceptual: por qué el tema es tesis y no solo adopción de buenas prácticas

## Respuesta corta

El trabajo no se plantea como una simple adopción de buenas prácticas en PRX. Si se formulara así, sería consultoría interna. La tesis se sostiene como investigación Design Science porque diseña, formaliza, aplica y evalúa un **marco ligero** para adoptar prácticas mínimas de Ingeniería de Software en una clase de contextos: equipos pequeños de desarrollo con baja estandarización.

La contribución no será demostrar que GitHub, las tareas visibles o las pruebas unitarias son buenas prácticas. Eso ya es conocido por la comunidad. La contribución será identificar qué principios de diseño permiten seleccionar, ordenar, adaptar y verificar esas prácticas para que sean aplicables y sostenibles en equipos pequeños que no pueden adoptar modelos pesados de mejora de procesos.

## Riesgo que se debe evitar

La formulación débil sería:

> La tesis propone adoptar buenas prácticas de Ingeniería de Software en PRX.

Esa formulación no es suficiente para una tesis de maestría porque el conocimiento ya existe y el resultado sería una mejora local. Un consultor podría recomendar registrar tareas, usar ramas, crear solicitudes de integración de cambios y escribir pruebas unitarias sin generar conocimiento científico nuevo.

La formulación defendible es:

> La tesis diseña y evalúa un marco ligero de adopción inicial que combina prácticas existentes en una ruta gradual, verificable y ajustada a herramientas reales, para derivar principios de diseño aplicables a equipos pequeños de desarrollo con baja estandarización.

La diferencia no es semántica. En el primer caso se aplican prácticas; en el segundo se estudia cómo diseñar un artefacto para que esa adopción sea posible, evaluable y transferible a contextos similares.

## Dónde está la contribución

La novedad relativa del trabajo no está en cada práctica por separado. Las tareas visibles, las ramas, los commits, las solicitudes de integración de cambios y las pruebas unitarias ya son conocidas. La novedad está en el diseño del marco como composición mínima:

1. qué prácticas se seleccionan primero;
2. en qué orden deben adoptarse;
3. qué precondiciones son necesarias;
4. qué prácticas se dejan fuera para evitar sobrecarga;
5. qué evidencia mínima debe producir cada práctica;
6. cómo se mide la adopción inicial;
7. qué condiciones hacen que el marco sea aplicable a equipos pequeños;
8. qué principios pueden transferirse a organizaciones similares.

Ese conocimiento no se obtiene solo leyendo buenas prácticas. Se obtiene construyendo el marco, aplicándolo, observando fricciones, rediseñándolo y evaluando sus resultados contra criterios definidos antes de la construcción.

## Diferencia entre consultoría y Design Science

| Consultoría o mejora interna | Tesis Design Science |
|:--|:--|
| Aplica prácticas conocidas en una empresa. | Diseña y evalúa un artefacto para una clase de problemas. |
| El resultado principal es que PRX mejore. | El resultado principal son principios de diseño transferibles analíticamente. |
| Puede basarse en experiencia profesional. | Debe basarse en literatura, decisiones de diseño trazables y evaluación. |
| No exige evaluación formativa con rediseño. | Exige al menos un ciclo formativo con rediseño y una evaluación sumativa inicial. |
| Termina en una guía interna. | Termina en un marco evaluado y en principios de diseño con condiciones de contorno. |

## Por qué pertenece a Ingeniería de Software

El problema pertenece directamente a Ingeniería de Software porque se ubica en prácticas de gestión técnica del desarrollo: visibilidad del trabajo, control de cambios, trazabilidad, revisión previa, verificación básica y pruebas unitarias. No se trata de administración general de empresas ni de gestión comercial. El artefacto propuesto opera sobre prácticas reconocidas del desarrollo de software y se fundamenta en cuerpos de conocimiento como ISO/IEC 29110, SWEBOK, GitHub Flow, pruebas de software y mejora de procesos en organizaciones pequeñas.

## Por qué corresponde a Design Science

El enfoque principal es Design Science Research porque la pregunta no puede responderse sin construir y evaluar un artefacto. La tesis no busca únicamente describir cómo trabaja PRX ni medir estadísticamente una relación causal. Busca construir un marco, aplicarlo en un contexto real, rediseñarlo a partir de evaluación formativa y evaluar su utilidad inicial.

El problema de diseño es práctico: PRX carece de una ruta ligera, común y verificable para adoptar prácticas mínimas. El problema de investigación —que en el formato institucional se registrará como problema científico— es la brecha sobre cómo diseñar marcos ligeros de adopción inicial para equipos pequeños de desarrollo con baja estandarización. La conexión entre ambos problemas es lo que sostiene el carácter científico del trabajo.

## Respuesta oral sugerida

Si me preguntan por qué esto no es solo adopción de buenas prácticas, responderé:

> Es cierto que las prácticas individuales ya existen. La tesis no pretende inventar GitHub Flow, tareas visibles ni pruebas unitarias. Lo que investiga es cómo diseñar un marco ligero que seleccione, ordene, adapte y verifique esas prácticas para equipos pequeños de desarrollo con baja estandarización. El aporte no es la práctica aislada, sino los principios de diseño que se derivan de construir, aplicar, rediseñar y evaluar el marco en un contexto real. Por eso el trabajo se formula como Design Science y no como consultoría de mejora interna.

## Preguntas probables del tribunal o docente

### ¿Qué tiene de nuevo si esas prácticas ya existen?

Lo nuevo no es la práctica aislada. Lo nuevo es la composición evaluada del marco: qué se adopta primero, bajo qué precondiciones, con qué evidencia mínima, con qué criterios de éxito y con qué condiciones de contorno para equipos pequeños.

### ¿Por qué no usar directamente Scrum, CMMI o ISO/IEC 29110?

Porque esos marcos tienen alcances distintos. Scrum completo no es el objeto del trabajo; CMMI se mantiene como antecedente conceptual y no como objetivo de certificación; ISO/IEC 29110 sustenta la orientación a entidades muy pequeñas, pero no entrega por sí sola una ruta mínima ajustada a las herramientas reales de PRX. El marco propuesto toma elementos pertinentes y los adapta a un problema acotado.

### ¿Cuál es el artefacto?

El artefacto es un marco ligero de adopción inicial de prácticas de Ingeniería de Software. Incluye diagnóstico inicial, ruta de adopción, reglas mínimas, productos de trabajo, criterios de verificación y condiciones de aplicación.

### ¿Cuál es la contribución?

La contribución serán principios de diseño para construir marcos ligeros de adopción inicial en equipos pequeños de desarrollo con baja estandarización. El marco aplicado en PRX será el vehículo de evaluación, no la contribución completa.

### ¿Cómo sabrá que funciona?

Se evaluará con línea base previa, evaluación formativa con rediseño documentado y evaluación sumativa inicial. Los criterios fueron fijados antes de construir: tareas visibles, ramas y commits conformes, solicitudes de integración de cambios, evidencia mínima de verificación y pruebas unitarias iniciales en componentes críticos.

## Frase central para memorizar

La tesis no investiga si las buenas prácticas son buenas; investiga cómo diseñar un marco ligero para que equipos pequeños de desarrollo con baja estandarización puedan adoptarlas de manera gradual, verificable y sostenible, generando principios de diseño transferibles a contextos similares.






