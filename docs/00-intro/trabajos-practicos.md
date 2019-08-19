# Pautas Generales para trabajos prácticos

Las siguientes son algunas recomendaciones generales para los Trabajos Prácticos.

Como siempre, hay ciertas características generales de programación que evaluamos sin importar si es código de presentación, de dominio, de test o incluso de configuración.

## Codígo

* Código descriptivo: usar (y priorizar) conceptos significativos para variables, métodos y clases
* Prolijidad y formateo
* Eliminar código que no se utilice (correr algún coverage nunca está de más)
* Borrar comentarios innecesarios
* No dejar espacios y lineas en blanco «extras» (se puede usar algún lint o un formatter automático)

## Diseño

* Priorizar la delegación y división del comportamiento entre los objetos
* Evitar código procedural (estructuras de control: if, while, etc…) salvo que la alternativa haga el código más complicado
* No mantener métodos largos: dividir en subtareas
* Favorecer el «Tell, Don’t Ask»
* Evitar objetos anémicos (objetos que solo tiene datos).
* Evitar código duplicado (DRY).
* Simplicidad (KISS)
* Evitar el sobrediseño. O sea, no diseñar todo un modelo de objetos para un problema que todavía no conocemos, pensando que «quizás en un futuro me van a pedir….». Diseñar sólo el mundo conocido.
* No agregar features o funcionalidad extra si existe código a emprolijar o refactorizar.
