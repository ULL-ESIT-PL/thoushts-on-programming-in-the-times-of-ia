# Reflexiones sobre la enseñanza de la programación en los tiempos de la IA Generativa

Aprender un lenguaje de programación consiste en incorporar los paradigmas y modelos de programación en los que se sostiene. Aunque actualmente ha disminuido la cantidad de código escrito por humanos, sigue siendo esencial la labor de leer el código escrito por las LLMs. Aprender un lenguaje siempre ha servido para aprender una forma distinta (paradigma) de pensar.

Por ejemplo:

* Lisp enseña metaprogramación y homoiconicidad[^1].
* Haskell enseña programación funcional pura.
* Rust enseña propiedad, préstamos y gestión de memoria.
* Prolog enseña programación lógica.
* Smalltalk y Ruby enseñan orientación a objetos a lo "Alan Kay".

La hipótesis que plantea que el lenguaje natural influye en la forma en la que pensamos y resolvemos problemas se conoce formalmente como la **hipótesis de la relatividad lingüística** o **hipótesis de Sapir-Whorf**. En su versión fuerte sostiene que el lenguaje determina la forma en que pensamos y resolvemos problemas[^2]. Con los lenguajes de programación ocurre algo similar: aprender un lenguaje enseña a pensar de una manera distinta.

[^2]: El cuento "Story of Your Life" de Ted Chiang, adaptado al cine como "Arrival", explora esta idea en el contexto de la comunicación con una especie alienígena. 

Sigue una tabla que muestra, para cada uno de los lenguajes anteriores, el paradigma y el concepto central que aportan:

| Lenguaje | Paradigma / forma de pensar | Concepto central que enseña | Mecanismo distintivo |
|---|---|---|---|
| Lisp | Metaprogramación | Homoiconicidad: el código es dato | Macros que transforman el AST antes de evaluarlo |
| Haskell | Programación funcional pura | Inmutabilidad y razonamiento ecuacional | Tipos con efectos controlados (mónadas), sin estado mutable |
| Prolog | Programación lógica | Especificar el "qué", no el "cómo" | Resolución por unificación y backtracking automático |
| Smalltalk / Ruby | Orientación a objetos "a lo Alan Kay" | Todo es un objeto que responde a mensajes | Despacho dinámico tardío; clases modificables en tiempo de ejecución |
| Rust | Sistemas y gestión de recursos | Propiedad (ownership) y tiempo de vida | El compilador verifica ausencia de data races y use-after-free sin recolector de basura |

Existe un paralelismo útil con la conducción de automóviles. Al principio de la automoción, conducir con seguridad exigía conocimientos casi de mecánico: el conductor debía entender el funcionamiento interno de la máquina para operarla y para reaccionar ante sus fallos. Hoy, el nivel de conocimiento que exige un carnet de conducir basta para circular con seguridad y para asumir la responsabilidad legal ordinaria de un accidente, sin necesidad de saber cómo funciona un motor. El conocimiento mecánico profundo no desapareció: se desplazó del conductor medio al especialista -el mecánico o el ingeniero de automoción- que diseña, repara y certifica el vehículo. Cuanto más sabe el conductor de mecánica, mejor cuida la máquina y más margen tiene para diagnosticar problemas atípicos, pero ese conocimiento extra ya no es la condición para operar el vehículo con seguridad y responsabilidad.

Trasladado a la programación con IA, cabe distinguir el mismo doble papel: el "conductor" que usa código generado por la IA para resolver un problema concreto, y el "mecánico/ingeniero" que construye, mantiene o depura en profundidad los lenguajes, compiladores y sistemas sobre los que se apoya esa generación. Es plausible que, a medida que la IA madure -mejores explicaciones, verificación automática, tests generados, análisis estático- el nivel de conocimiento exigido al "conductor" se reduzca a algo parecido a un carnet: saber leer el código generado, especificar el problema con precisión, verificar el resultado y saber cuándo pedir ayuda a un especialista. El conocimiento profundo de "Procesadores de Lenguajes" seguiría siendo imprescindible, pero para el papel de mecánico/ingeniero, no necesariamente para todo el que programa.

La analogía del automóvil sugiere que una vez la tecnología madura y se estandariza la responsabilidad legal ordinaria podría cubrirse con una competencia mucho más básica -un "carnet"-, mientras el conocimiento profundo se concentra en un rol especializado distinto del usuario medio. 
Ambas ideas pueden ser ciertas a la vez si se leen como dos momentos de la misma curva de madurez: mientras la IA no ofrezca explicaciones fiables y verificables -el "ABS" o los "airbags" del código-, que se corresponden con la situación actual, en la que cualquiera que programe debe poder auditar en profundidad lo que la IA produce. 
La analogía del automóvil describe, en cambio, el punto de llegada plausible una vez la IA alcance ese nivel de madurez: en ese escenario el conocimiento profundo de la programación seguirá siendo crítico, pero para menos gente -quienes construyen y certifican las herramientas-, no para todo programador. ¿En qué punto de esa curva de madurez estamos hoy?, ¿A qué perfil de estudiante debe dirigirse la enseñanza?.

Esta distinción tiene una consecuencia directa sobre cómo debería cambiar la formación de un ingeniero informático: en lugar de un currículo único, tendría que dividirse en dos títulos (algo como una ingeniería técnica y una superior) con objetivos distintos.

**El "carnet"**, común a todo "usuario avanzado de IA", sea cual sea su especialidad, debería centrarse en especificar problemas con precisión, verificar la corrección de una solución -tests, propiedades, casos límite- y leer y auditar código ajeno, en particular código generado por IA y no sólo el de otros compañeros; en detectar errores de razonamiento y fallos sutiles en esa salida que no siempre son evidentes a simple vista; y en diseñar sistemas y decidir compromisos arquitectónicos, que sigue siendo terreno humano.

**El "ingeniero superior/mecánico"**, para quien vaya a construir o mantener los cimientos -lenguajes, compiladores, runtimes, frameworks, sistemas críticos-, es donde el conocimiento profundo de "Lenguajes y Paradigmas" o "Procesadores de Lenguajes" sigue siendo imprescindible, no como cultura general sino como oficio: sin esta capa nadie construye ni corrige las herramientas de las que depende la capa del "carnet".

El conocimiento de los contenidos de materias de programación como "Fundamentos de la Programación", "Estructuras de Datos", "Lenguajes y Paradigmas" o "Procesadores de Lenguajes" sigue siendo relevante en este contexto. Paradójicamente, cuanto mejor genera código la IA, más importante es entender cómo se representa, analiza, transforma y verifica ese código. La necesidad de que el ingeniero entienda el producto generado es consecuencia de que, en el marco legal actual, es su empresa quien tiene la responsabilidad legal sobre las decisiones tomadas. Es por eso que también la investigación en IA/LLMs  debe evolucionar para que puedan explicar, justificar y argumentar mejor sus decisiones de forma comprensible para un ingeniero. Un ingeniero que debe tener suficientes conocimientos de programación para entender la explicación, discernir los puntos débiles, errores y posibles mejoras del código generado y fijar los siguientes objetivos.
Los fundamentos dejan de ser un medio para producir programas manualmente y pasan a ser la base para dirigir, evaluar y mejorar lo que producen las herramientas inteligentes.



[^1]: La homoiconicidad es una propiedad de ciertos lenguajes de programación en los que la estructura del código fuente es una estructura de datos que el programa puede manipular. El código se representa en las mismas estructuras de datos que el propio lenguaje utiliza, lo que permite que un programa pueda tratarse a sí mismo como un dato.

