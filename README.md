# Reflexiones sobre la enseñanza de lenguajes de programación en estos tiempos de la IA

Aprender un nuevo lenguaje nunca es el objetivo.
Lo que ocurre es que aprender un lenguaje ahora y siempre ha servido para aprender una **forma distinta de pensar**.

Por ejemplo:

* Lisp enseña metaprogramación y homoiconicidad[^1].
* Haskell enseña programación funcional pura.
* Rust enseña propiedad, préstamos y gestión de memoria.
* Prolog enseña programación lógica.
* Smalltalk y Ruby enseñan orientación a objetos a lo "Alan Kay".

En ese contexto, aprender un nuevo lenguaje sigue teniendo sentido si ese lenguaje te enseña un modelo/paradigma o versión del modelo/paradigma nuevo. Aprender simplemente "otro lenguaje más" porque el mercado lo demanda tiene menos valor que antes.

Sigue una tabla que muestra, para cada uno de los lenguajes anteriores, el paradigma y el concepto central que aportan:

| Lenguaje | Paradigma / forma de pensar | Concepto central que enseña | Mecanismo distintivo |
|---|---|---|---|
| Lisp | Metaprogramación | Homoiconicidad[^1]: el código es dato | Macros que transforman el AST antes de evaluarlo |
| Haskell | Programación funcional pura | Inmutabilidad y razonamiento ecuacional | Tipos con efectos controlados (mónadas), sin estado mutable |
| Prolog | Programación lógica | Especificar el "qué", no el "cómo" | Resolución por unificación y backtracking automático |
| Smalltalk / Ruby | Orientación a objetos "a lo Alan Kay" | Todo es un objeto que responde a mensajes | Despacho dinámico tardío; clases modificables en tiempo de ejecución |
| Rust | Sistemas y gestión de recursos | Propiedad (ownership) y tiempo de vida | El compilador verifica ausencia de data races y use-after-free sin recolector de basura |

Aprender un lenguaje no consiste en memorizar la sintaxis. Consiste **en incorporar un modelo de programación**. Una habilidad esencial en el futuro será **leer** código.

El conocimiento de los contenidos de materias de programación como "Lenguajes y Paradigmas" o "Procesadores de Lenguajes" sigue siendo relevante. Paradójicamente, cuanto mejor genera código la IA, más importante es entender cómo se representa, analiza, transforma y verifica ese código. La necesidad de que el humano entienda el producto generado es consecuencia de que, en el marco legal actual, es este quien tiene la responsabilidad legal sobre las decisiones tomadas. Es por eso que también la investigación en IA/LLMs  debe evolucionar para que puedan explicar, justificar y argumentar mejor sus decisiones de forma comprensible para un humano. Un humano que debe tener suficientes conocimientos de programación para entender la explicación, discernir los puntos débiles, errores y posibles mejoras del código generado y fijar los siguientes objetivos.
Los fundamentos dejan de ser un medio para producir programas manualmente y pasan a ser la base para dirigir, evaluar y mejorar lo que producen las herramientas inteligentes.

[^1]: La homoiconicidad es una propiedad de ciertos lenguajes de programación en los que la estructura del código fuente es una estructura de datos que el programa puede manipular. El código se representa en las mismas estructuras de datos que el propio lenguaje utiliza, lo que permite que un programa pueda tratarse a sí mismo como un dato.

La programación no es sólo escribir código.
Es transformar una idea en un procedimiento preciso haciendo uso de los conceptos y paradigmas que constituyen la ingeniería del software y de las herramientas de desarrollo
que materializan de forma diversa los conceptos de esta rama de la ingeniería.
La IA es un copiloto/herramienta/compañero que interviene en todas las fases de la programación y que escribe código mejor que el humano. El humano debe decidir sobre aspectos como:

* qué problema resolver,
* qué restricciones existen,
* qué algoritmo conviene,
* qué arquitectura será mantenible,
* qué compromisos aceptar.
* si puede asumir la responsabilidad sobre el código generado o necesita mejora.

Enseñar programación tiene sentido, pero no como hace diez años.
Antes el profesor, los libros, internet eran las fuentes de conocimiento, ahora el conocimiento está disponible instantáneamente.
El profesor debe aportar algo distinto: seleccionar qué merece la pena aprender, construir las correspondientes secuencias pedagógicas, enseñar 
técnicas para detectar y corregir errores de razonamiento, 
elaborar la justificación de las  decisiones tomadas y 
la reflexión crítica sobre el código generado.

Dentro de diez años seguiremos enseñando programación, pero de forma distinta.
Habrá menos énfasis en memorizar sintaxis,
escribir código repetitivo,
implementar algoritmos estándar desde cero
y mucho más en
diseñar sistemas,
especificar correctamente problemas,
verificar que una solución es correcta,
comprender los fundamentos de los lenguajes, compiladores, sistemas operativos y algoritmos y 
colaborar eficazmente con herramientas de IA.

