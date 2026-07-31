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

Existe un paralelismo útil con la conducción de automóviles. Al principio de la automoción, conducir con seguridad exigía conocimientos casi de mecánico: el conductor debía entender el funcionamiento interno de la máquina para operarla y para reaccionar ante sus fallos. Hoy, el nivel de conocimiento que exige un carnet de conducir basta para circular con seguridad y para asumir la responsabilidad legal ordinaria de un accidente, sin necesidad de saber cómo funciona un motor. El conocimiento mecánico profundo no desapareció: se desplazó del conductor medio al especialista -el mecánico o el ingeniero de automoción- que diseña, repara y certifica el vehículo. Cuanto más sabe el conductor de mecánica, mejor cuida la máquina y más margen tiene para diagnosticar problemas atípicos, pero ese conocimiento extra ya no es la condición para operar el vehículo con seguridad y responsabilidad.

Trasladado a la programación con IA, cabe distinguir el mismo doble papel: el "conductor" que usa código generado por la IA para resolver un problema concreto, y el "mecánico/ingeniero" que construye, mantiene o depura en profundidad los lenguajes, compiladores y sistemas sobre los que se apoya esa generación. Es plausible que, a medida que la IA madure -mejores explicaciones, verificación automática, tests generados, análisis estático- el nivel de conocimiento exigido al "conductor" se reduzca a algo parecido a un carnet: saber leer el código generado, especificar el problema con precisión, verificar el resultado y saber cuándo pedir ayuda a un especialista. El conocimiento profundo de "Procesadores de Lenguajes" seguiría siendo imprescindible, pero para el papel de mecánico/ingeniero, no necesariamente para todo el que programa.

**Reflexión comparativa.** El párrafo anterior sobre la relevancia asume una relación directamente proporcional entre la capacidad de la IA y el conocimiento profundo que necesita el humano: cuanto mejor la IA, más debe saber el humano, apoyado en que la responsabilidad legal recae sobre este. La analogía del automóvil sugiere lo contrario una vez la tecnología madura y se estandariza: la responsabilidad legal ordinaria se cubre con una competencia mucho más básica -un "carnet"-, mientras el conocimiento profundo se concentra en un rol especializado distinto del usuario medio. Ambas ideas pueden ser ciertas a la vez si se leen como dos momentos de la misma curva de madurez: mientras la IA no ofrezca explicaciones fiables y verificables -el "ABS" o los "airbags" del código-, el primer párrafo describe correctamente la situación actual, en la que cualquiera que programe debe poder auditar en profundidad lo que la IA produce. La analogía del automóvil describe, en cambio, el punto de llegada plausible una vez la IA alcance ese nivel de madurez: en ese escenario el conocimiento de compiladores y paradigmas seguirá siendo crítico, pero para menos gente -quienes construyen y certifican las herramientas-, no para todo programador. La pregunta que ninguno de los dos párrafos resuelve es en qué punto de esa curva de madurez estamos hoy, y por tanto a qué perfil de estudiante debe dirigirse la enseñanza.



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

