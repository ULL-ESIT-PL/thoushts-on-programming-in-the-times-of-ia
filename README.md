# Reflexiones sobre la enseñanza de lenguajes de programación en estos tiempos de la IA

Aprender un nuevo lenguaje nunca es el objetivo. Aprender un lenguaje consiste **en incorporar un modelo de programación**. Aunque actualmente ha disminuído la cantidad de código escrito por humanos, sigue siendo esencial la labor de **leer** el código escrito por las LLMs. Aprender un lenguaje siempre ha servido para aprender una forma distinta (paradigma) de pensar.

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
| Lisp | Metaprogramación | Homoiconicidad: el código es dato | Macros que transforman el AST antes de evaluarlo |
| Haskell | Programación funcional pura | Inmutabilidad y razonamiento ecuacional | Tipos con efectos controlados (mónadas), sin estado mutable |
| Prolog | Programación lógica | Especificar el "qué", no el "cómo" | Resolución por unificación y backtracking automático |
| Smalltalk / Ruby | Orientación a objetos "a lo Alan Kay" | Todo es un objeto que responde a mensajes | Despacho dinámico tardío; clases modificables en tiempo de ejecución |
| Rust | Sistemas y gestión de recursos | Propiedad (ownership) y tiempo de vida | El compilador verifica ausencia de data races y use-after-free sin recolector de basura |


El conocimiento de los contenidos de materias de programación como "Lenguajes y Paradigmas" o "Procesadores de Lenguajes" sigue siendo relevante. Paradójicamente, cuanto mejor genera código la IA, más importante es entender cómo se representa, analiza, transforma y verifica ese código. La necesidad de que el humano entienda el producto generado es consecuencia de que, en el marco legal actual, es este quien tiene la responsabilidad legal sobre las decisiones tomadas. Es por eso que también la investigación en IA/LLMs  debe evolucionar para que puedan explicar, justificar y argumentar mejor sus decisiones de forma comprensible para un humano. Un humano que debe tener suficientes conocimientos de programación para entender la explicación, discernir los puntos débiles, errores y posibles mejoras del código generado y fijar los siguientes objetivos.
Los fundamentos dejan de ser un medio para producir programas manualmente y pasan a ser la base para dirigir, evaluar y mejorar lo que producen las herramientas inteligentes.

Existe un paralelismo útil con la conducción de automóviles. Al principio de la automoción, conducir con seguridad exigía conocimientos casi de mecánico: el conductor debía entender el funcionamiento interno de la máquina para operarla y para reaccionar ante sus fallos. Hoy, el nivel de conocimiento que exige un carnet de conducir basta para circular con seguridad y para asumir la responsabilidad legal ordinaria de un accidente, sin necesidad de saber cómo funciona un motor. El conocimiento mecánico profundo no desapareció: se desplazó del conductor medio al especialista -el mecánico o el ingeniero de automoción- que diseña, repara y certifica el vehículo. Cuanto más sabe el conductor de mecánica, mejor cuida la máquina y más margen tiene para diagnosticar problemas atípicos, pero ese conocimiento extra ya no es la condición para operar el vehículo con seguridad y responsabilidad.

Trasladado a la programación con IA, cabe distinguir el mismo doble papel: el "conductor" que usa código generado por la IA para resolver un problema concreto, y el "mecánico/ingeniero" que construye, mantiene o depura en profundidad los lenguajes, compiladores y sistemas sobre los que se apoya esa generación. Es plausible que, a medida que la IA madure -mejores explicaciones, verificación automática, tests generados, análisis estático- el nivel de conocimiento exigido al "conductor" se reduzca a algo parecido a un carnet: saber leer el código generado, especificar el problema con precisión, verificar el resultado y saber cuándo pedir ayuda a un especialista. El conocimiento profundo de "Procesadores de Lenguajes" seguiría siendo imprescindible, pero para el papel de mecánico/ingeniero, no necesariamente para todo el que programa.

**Reflexión comparativa.** El párrafo anterior sobre la relevancia asume una relación directamente proporcional entre la capacidad de la IA y el conocimiento profundo que necesita el humano: cuanto mejor la IA, más debe saber el humano, apoyado en que la responsabilidad legal recae sobre este. La analogía del automóvil sugiere lo contrario una vez la tecnología madura y se estandariza: la responsabilidad legal ordinaria se cubre con una competencia mucho más básica -un "carnet"-, mientras el conocimiento profundo se concentra en un rol especializado distinto del usuario medio. Ambas ideas pueden ser ciertas a la vez si se leen como dos momentos de la misma curva de madurez: mientras la IA no ofrezca explicaciones fiables y verificables -el "ABS" o los "airbags" del código-, el primer párrafo describe correctamente la situación actual, en la que cualquiera que programe debe poder auditar en profundidad lo que la IA produce. La analogía del automóvil describe, en cambio, el punto de llegada plausible una vez la IA alcance ese nivel de madurez: en ese escenario el conocimiento de compiladores y paradigmas seguirá siendo crítico, pero para menos gente -quienes construyen y certifican las herramientas-, no para todo programador. La pregunta que ninguno de los dos párrafos resuelve es en qué punto de esa curva de madurez estamos hoy, y por tanto a qué perfil de estudiante debe dirigirse la enseñanza.

Esta distinción tiene una consecuencia directa sobre cómo debería cambiar la formación de un ingeniero informático: en lugar de un currículo único, tendría que dividirse en dos capas con objetivos distintos.

**El "carnet"**, común a todo ingeniero informático sea cual sea su especialidad, debería centrarse en especificar problemas con precisión, verificar la corrección de una solución -tests, propiedades, casos límite- y leer y auditar código ajeno, en particular código generado por IA y no sólo el de otros compañeros; en detectar errores de razonamiento y fallos sutiles en esa salida que no siempre son evidentes a simple vista; y en diseñar sistemas y decidir compromisos arquitectónicos, que sigue siendo terreno humano.

**El "ingeniero/mecánico"**, para quien vaya a construir o mantener los cimientos -lenguajes, compiladores, runtimes, frameworks, sistemas críticos-, es donde el conocimiento profundo de "Lenguajes y Paradigmas" o "Procesadores de Lenguajes" sigue siendo imprescindible, no como cultura general sino como oficio: sin esta capa nadie construye ni corrige las herramientas de las que depende la capa del "carnet".

El riesgo de un currículo que se vuelva todo "carnet" por seguir el ritmo del mercado es vaciar la capa de "ingeniero/mecánico" justo cuando más se necesita gente capaz de construir y depurar la próxima generación de herramientas de IA.



[^1]: La homoiconicidad es una propiedad de ciertos lenguajes de programación en los que la estructura del código fuente es una estructura de datos que el programa puede manipular. El código se representa en las mismas estructuras de datos que el propio lenguaje utiliza, lo que permite que un programa pueda tratarse a sí mismo como un dato.

