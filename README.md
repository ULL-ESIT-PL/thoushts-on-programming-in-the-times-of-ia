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

Paradójicamente, cuanto mejor genera código la IA, más importante es entender cómo se representa, analiza, transforma y verifica ese código. La necesidad de que este profesional entienda el producto generado es en parte consecuencia de que, en el marco legal actual, es el humano quien tiene la responsabilidad legal sobre las decisiones tomadas. 

> The programmer remains essential. Not as a vessel of knowledge but as the orchestrating agent who understands the parts and how they fit together, maintains the integrity of the system, and who decides what matters. This shift has profound implications for how we understand programming expertise. The most capable developers of this new era will not be those who type the fastest or remember the most, but those who can hold deep mental models while offloading everything that interferes with that. They will combine strong systems reasoning with AI-augmented recall and will treat the model almost like a cognitive prosthetic: useful, fast, but incapable of finally determining subjective-semantic correctness or coherence. 

- Jeremy Osborn. 2026. AI Didn’t Make Programming Easier. It Just Made It Differently Difficult. Commun. ACM 69, 8 (August 2026), 18–21. https://doi.org/10.1145/3795534

Existe un paralelismo útil con la conducción de automóviles. Al principio de la automoción, conducir con seguridad exigía conocimientos casi de mecánico: el conductor debía entender el funcionamiento interno de la máquina para operarla y para reaccionar ante sus fallos. Hoy, el nivel de conocimiento que exige un carnet de conducir basta para circular con seguridad y para asumir la responsabilidad legal ordinaria de un accidente, sin necesidad de saber cómo funciona un motor. El conocimiento mecánico profundo no desapareció: se desplazó del conductor medio al especialista -el mecánico o el ingeniero de automoción- que diseña, repara y certifica el vehículo. Cuanto más sabe el conductor de mecánica, mejor cuida la máquina y más margen tiene para diagnosticar problemas atípicos, pero ese conocimiento extra ya no es la condición para operar el vehículo con seguridad y responsabilidad.

Trasladado a la programación con IA, cabe distinguir el mismo doble papel: el "conductor" que usa código generado por la IA para resolver un problema concreto, y el "mecánico/ingeniero" que construye, mantiene o depura en profundidad los lenguajes, compiladores y sistemas sobre los que se apoya esa generación. Es plausible que, a medida que la IA madure -mejores explicaciones, verificación automática, tests generados, análisis estático- el nivel de conocimiento exigido al "conductor" se reduzca a algo parecido a un carnet: saber leer el código generado, especificar el problema con precisión, verificar el resultado y saber cuándo pedir ayuda a un especialista. El conocimiento profundo seguiría siendo imprescindible, pero para el papel de mecánico/ingeniero, no necesariamente para todo el que programa.

La analogía del automóvil sugiere que una vez la tecnología madura y se estandariza la responsabilidad legal ordinaria podría cubrirse con una competencia mucho más básica -un "carnet"-, mientras el conocimiento profundo se concentra en un rol especializado distinto del usuario medio. Mientras la IA no ofrezca explicaciones fiables y verificables -el "ABS" o los "airbags" del código- cualquiera que programe un producto comercial debería tener preparación suficiente para poder auditar en profundidad lo que la IA produce. 
También describe un punto de llegada plausible en que la IA alcance un nivel de madurez. En ese escenario el conocimiento profundo de la programación seguirá siendo importante, pero para menos gente -quienes construyen y certifican las herramientas-, no para todo programador. ¿En qué punto de esa curva de madurez estamos hoy?.

Esta distinción sugiere cómo podría cambiar la formación de un ingeniero informático: en lugar de un currículo único, se podría concebir un sistema en dos niveles con objetivos distintos.

**El "carnet"**, común a todo "ingeniero". Debería centrarse en especificar problemas con precisión, verificar la corrección de una solución -tests, propiedades, casos límite- y leer y auditar código ajeno, en particular código generado por IA; en detectar errores de razonamiento y fallos sutiles en esa salida que no siempre son evidentes a simple vista; y en diseñar sistemas y decidir compromisos arquitectónicos, que sigue siendo terreno humano. Una persona con este título debe tener suficientes conocimientos de programación para entender la explicación, discernir los puntos débiles, errores y posibles mejoras del código generado y fijar los siguientes objetivos.


**El "ingeniero/mecánico"**, para quien vaya a construir o mantener los cimientos -lenguajes, compiladores, runtimes, frameworks, sistemas críticos-, es donde el conocimiento profundo de la programación sigue siendo imprescindible, no como cultura general sino como oficio: sin esta capa nadie construye ni corrige las herramientas de las que depende la capa del "carnet".


Los fundamentos dejan de ser un medio para producir programas manualmente y pasan a ser la base para dirigir, evaluar y mejorar lo que producen las herramientas inteligentes.



[^1]: La homoiconicidad es una propiedad de ciertos lenguajes de programación en los que la estructura del código fuente es una estructura de datos que el programa puede manipular. El código se representa en las mismas estructuras de datos que el propio lenguaje utiliza, lo que permite que un programa pueda tratarse a sí mismo como un dato.

## Curriculum del Carnet

No es necesariamente una titulación aparte, sino un conjunto de competencias que cualquier persona que programe con apoyo de IA debería dominar para poder asumir con garantías la responsabilidad sobre el código que pone en producción.

| Competencia | Qué cubre | Por qué importa |
|---|---|---|
| Fundamentos de programación y estructuras de datos | Tipos, control de flujo, complejidad básica, estructuras de datos elementales | Lo justo para leer y razonar sobre código ajeno, no para producirlo todo a mano |
| Especificación de problemas | Ingeniería de requisitos, casos de uso, invariantes | Sin una especificación precisa no se puede pedir bien a la IA ni juzgar si el resultado es correcto |
| Fundamentos de dirección de IA (prompting) | Redactar instrucciones efectivas, descomponer tareas grandes en pasos verificables, iterar sobre el resultado, gestionar contexto y herramientas del agente | Es el mecanismo concreto con el que el "conductor" maneja el vehículo: una instrucción vaga o mal descompuesta produce un resultado tan malo como una buena instrucción sin verificar |
| Verificación y testing | Tests unitarios y de propiedades, casos límite, cobertura | Comprobar que el código generado hace lo que dice hacer, no solo que "parece" correcto |
| Lectura y auditoría de código generado por IA | Revisión de código (code review) aplicada a salidas de IA | Leer se vuelve más importante que escribir |
| Control de versiones y trazabilidad | Commits atómicos, diffs, ramas, revisión de cambios (PRs), bisect, revertir | Es el mecanismo con el que se audita, aprueba y responde de cada cambio -propio o generado por IA-; sin un historial trazable no hay responsabilidad verificable |
| Pensamiento crítico sobre IA | Detectar alucinaciones, razonamientos plausibles pero erróneos, sesgos | La IA se equivoca con apariencia de seguridad; hay que saber dónde desconfiar |
| Diseño y arquitectura de sistemas | Trade-offs, patrones, mantenibilidad | Sigue siendo terreno humano |
| Responsabilidad profesional y marco legal/ético | Qué implica asumir la autoría de código que uno no ha escrito línea a línea | Conecta con la responsabilidad legal sobre las decisiones tomadas |
| Paradigmas de programación (nivel de reconocimiento) | Reconocer, al leer código, las marcas distintivas de cada paradigma: mutación de estado vs. inmutabilidad, mensajes vs. llamadas a función, unificación/backtracking, macros/código-como-dato, propiedad y préstamo | Cada paradigma trae consigo garantías y errores típicos propios (p. ej. Rust descarta data races, Haskell descarta efectos ocultos); basta con identificar el modelo mental, sin necesidad de dominarlo a fondo |

Quien complete este currículo puede especificar, dirigir, verificar y responsabilizarse del código que la IA produce, aunque no sepa construir el compilador, el runtime o el modelo que lo genera.

