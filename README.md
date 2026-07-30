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

Sigue una **tabla comparativa de ejemplos de conceptos OOP que solo se aprenden conociendo en profundidad diferentes lenguajes**

| Característica | Alan Kay[](https://www.google.com/search?q=alan+kay&kgmid=/m/0q0x#sv=CBwS1AMKpQMSogMK4gJBSmlUNHRJQ0NOSWdzbEZIZVotc29WX2w5c3BIUGlmQUlKbmd0UklGcE1oWVJXZldqbjFjWTdfVS15bVIzdjZCejRmQ2RFekxxb25HQlpLdmk5X21udjBKZlhGV1gxMEgwR1ZydV9MUjY0blJlcnZuRElMb1B6Ymp3X2I1UjRnTTZjcElZNkEzWFpWTFBWNnY5QkNXWHpFYmJBNmhyMHlaSG5SNmprN080MDhLU28yX21kY0lTeTM0NGhxZ1NkTGZad1k0WUx3aTZjS0ozNkhxbGVFWmp4Tl8tYlY2RWhUM2tid0czM3l3Wlp0bW9kZU4yMnVma0FhZEhaaWdkdkU3OGZUUEhMX1RGTkdzUWZmVWtiODRwRlhuQVc2NlJCbGxzd3Ytc0J1OUp0MzRBRGtJUDBTRDdwQkdiMEp3YjhzTDJPandLU25TeTI3QXZ3eHpfQmY3ZjFjUVFzRy1idlNCN1ESF2ZnRnJhdE9MSXVHLW5zRVA5SkRmeVFnGiJBRHNyOWZST3lveG9SZEx3Rzc5VDVoMkd5X3I0U1lwM3BnEgQ3ODU0GgEzIg0KAXESCGFsYW4ga2F5IhAKBWtnbWlkEgcvbS8wcTB4KAAYRSDA8PniDw) (Smalltalk) | Simula | Java | Rust (No es OOP puro) |
|---|---|---|---|---|
| Foco Principal | Mensajes y comunicación | Bloques de datos y simulación | Clases y seguridad de tipos | Datos, Comportamiento (traits) y Propiedad |
| Despacho de Métodos | Dinámico (Tardío/Late binding) | Estático / Dinámico (virtual) | Dinámico por defecto | Estático (Estático/Generics) o Dinámico (dyn) |
| Herencia | Simple (basada en clases) | Simple | Simple (Clases) + Múltiple (Interfaces) | No existe (Se usan traits y composición) |
| Manejo de Memoria | Recolector de Basura (Garbage Collector) | Recolector de Basura automático | Recolector de Basura (JVM) | Sistema de Propiedad (Ownership) en compilación |

Aprender un lenguaje no consiste en memorizar la sintaxis. Consiste **en incorporar un modelo de programación**. Una habilidad esencial en el futuro será **leer** código.

Materias como "Lenguajes y Paradigmas" o "Procesadores de Lenguajes" pueden ganar relevancia. Paradójicamente, cuanto mejor genera código la IA, más importante es entender cómo se representa, analiza, transforma y verifica ese código. Los fundamentos dejan de ser un medio para producir programas manualmente y pasan a ser la base para dirigir, evaluar y mejorar lo que producen las herramientas inteligentes.

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

