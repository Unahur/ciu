# Mejores prácticas

Este documento contiene las convenciones y prácticas recomendadas en la materia. El contenido se basa en el documento creado por [undefinedschool](https://undefinedschool.io/) para su programa de Full Stack JavaScript Developer.

## Contenido

- [Mejores prácticas](#mejores-prácticas)
  - [Contenido](#contenido)
  - [Disclaimer](#disclaimer)
  - [General](#general)
  - [HTML5](#html5)
  - [CSS3](#css3)
  - [Git](#git)
  - [Comentarios](#comentarios)
  - [JavaScript](#javascript)

## Disclaimer

Las buenas prácticas son convenciones que adoptamos para _estandarizar_ nuestra forma de desarrollar, utilizar ciertos patrones que nos permitan evitar algunos errores comunes y escribir código de mayor calidad, legible, mantenible, escalable, etc.

- **No son reglas**. Siempre debemos tener en cuenta el _contexto_ y no aplicarlas ciegamente.
- **Son subjetivas y muchas veces arbitrarias**.

Esta es sólo una guía general que toma ciertas prácticas comunes. Resulta fundamental, seguir las guías de buenas prácticas y estilos del proyecto en el que estemos trabajando y si no las tuviese, buscar la oportunidad de discutirlas y definirlas.

## General

- Para nombrar archivos y carpetas, utilizá *lowercase* (minúsculas), separando palabras con guiones medios. Ej: `index.html`, `common-styles.css`.
- Usá _[soft tabs](https://opensourcehacker.com/2012/05/13/never-use-hard-tabs/)_ (2 espacios) para indentar el código.
- **LCS:** para cualquier código que escribamos, intentá, en lo posible, *optimizarlo* para que sea
  - **L**egible
  - **C**onsistente
  - **S**imple

- Nunca olvidar que escribimos código para otras personas. Debería ser *[simple de entender](https://www.oreilly.com/library/view/the-art-of/9781449318482/ch01.html)*. Como diría el gran Kyle Simpson, _[Code is for Humans](https://frontendmasters.com/teachers/kyle-simpson/code-is-for-humans/)_. Salvo que estemos programando compiladores, claro.
- Utilizar _styleguides_ para estandarizar y normalizar la forma en que escribimos código. Ejemplos: [Mark Otto - HTML & CSS Styleguide](http://codeguide.co/), [AirBnB - CSS Styleguide](https://github.com/airbnb/css), [AirBnB -  JavaScript Styleguide](https://github.com/airbnb/javascript).
- Utilizar herramientas tales como [linters](https://eslint.org/) y [formateadores de código](https://prettier.io/). [Esta es una guía](https://www.youtube.com/watch?v=lHAeK8t94as) para realizar el setup de `Eslint + Prettier`. Existen alternativas similares, lo importante es fijar alguna convención y _styleguide_ para el proyecto.

## HTML5

- Definí/planificá la estructura de tu sitio en secciones o *componentes*, **antes de empezar a escribir el código**. Lápiz y papel!
- Separá el *contenido/estructura* de la *presentación*. Para los estilos usa CSS, evitá tags como `b`ó `i` por ejemplo.
- Usá HTML5 y tags *semánticos*. No abuses del `div`.
- Usá los distintos tipos de *headings* cuando corresponda (`h1`...`h6`), para darle jerarquía al contenido de tu sitio y facilitarle el trabajo a screen-readers y buscadores.
- Evitá, en lo posible, los contenedores genéricos. No abuses del `div`.
- Siempre declará el `DOCTYPE`.
- Agregá al tag `html`el atributo `lang`, con el valor correspondiente.
- Siempre agregá el atributo `alt` a las imágenes, con un texto descriptivo.
- Indentá tu código apropiadamente en el editor, para escribir código más legible, facilitar la colaboración y el trabajo en equipo.

## CSS3

- Estilá, en lo posible, usando clases. De esta forma obtenes mayor control sobre la _especificidad_ y resulta más fácil componer estilos.
- Para los nombres de las clases utilizá *lowercase* (minúsculas), separando palabras con guiones medios. Ej: `.custom-btn`.
- Evitá utilizar selectores de ID. Introducen un alto nivel de especificidad a nuestras reglas y no son reutilizables.
- Evitá, en lo posible, utilizar estilos *inline* e `!important` para [no alterar la _especificidad_](https://csswizardry.com/2014/07/hacks-for-dealing-with-specificity/) y dificultar el mantenimiento posterior.
- Si utilizas selectores múltiples para definir una regla de estilo, escribí cada uno en su propia línea.
- Separá cada regla de estilo con 1 línea en blanco.
- Si usas HTML5, con tags más semánticos y no genéricos, vas a escribir menos CSS, más legible y mantenible.
- Reutilizá estilos comunes entre componentes, utilizando la cascada.
- Componé estilos usando clases (ver, por ejemplo, cómo aplica esto [Tachyons](https://github.com/dwyl/learn-tachyons)).
- Reset: utilizá `box-sizing: border-box` para todos los elementos del sitio, al igual que empezar con `margin` y `padding` en 0.
- Es recomendable escribir los selectores más genéricos al principio para evitar pisar estilos.
- En lo posible, definí alguna convención para el nombre de los selectores y tratar de mantenerla. Sé consistente.

❌ **Evitemos esto...**

```css
.avatar{
    border-radius:50%;
    border:2px solid white; }
.no, .nope, .not_good {
    // ...
}
#lol-no {
  // ...
}
```

✅ **De esta manera es mejor**

```css
.avatar {
  border-radius: 50%;
  border: 2px solid white;
}

.one,
.selector,
.per-line {
  // ...
}
```

## Git

- Escribí mensajes de commits en inglés.
- Escribí mensajes de commits descriptivos.
- En lo posible, _comitea_ de forma frecuente.
- Intentá, en lo posible, realizar *[commits](https://seesparkbox.com/foundry/atomic_commits_with_git) [atómicos](http://www.pauline-vos.nl/atomic-commits/)*.
- Escribí los mensajes de commits en *[tiempo presente, modo imperativo](https://stackoverflow.com/a/3580764)*.
- Más tips para escribir mejores mensajes de commit [acá](https://github.com/RomuloOliveira/commit-messages-guide).
- Eliminá los branches que ya no utilices, tanto localmente como de GitHub.
- Antes de hacer un `pull` para traer los cambios nuevos, hacé `commit` de tus cambios locales

## Comentarios

- Utilizá, en lo posible, _comentarios minimales_, es decir, los necesarios, ni más ni menos. Para ver mejor de qué se trata esto, leé la sección _Minimal Comments_ del artículo _[The Exceptional Beauty of Doom 3's Source Code](https://kotaku.com/the-exceptional-beauty-of-doom-3s-source-code-5975610)_.
- Los comentarios deberían hablarnos, en lo posible, del _por qué_, no del _qué_. El _por qué_ implica darle información sobre el contexto del problema y las decisiones que tomaste a tus lectores, que para vos es evidente pero no para el resto. El código _debería ser lo suficientemente claro_ para describir el _qué_.
- Si tu código está demasiado comentado, podes tomarlo como indicador de que quizás no sea lo suficientemente claro.

## JavaScript

- El código que escribís no es para la máquina, sino para _comunicar ideas a otras personas_. Por eso, querés que sea lo más claro posible. Mirá _[Code is for Humans](https://frontendmasters.com/teachers/kyle-simpson/code-is-for-humans/)_ y _[Don’t be clever](https://www.simplethread.com/dont-be-clever/)_.
- Utilizá **nombres descriptivos** para constantes, variables y funciones. Volvé a leer el ítem anterior.
- En lo posible, escribí 1 instrucción por línea de código.
- Utilizá `const` por defecto.
- Si querés definir algo **explícitamente como variable**, utilizá `let`.
- Evitá usar `var`.
- Utilizá [igualdad/desigualdad estricta](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness#Strict_equality_using) para las comparaciones, para evitar caer en las trampas del _[type coercion](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness)_.
- Utilizá, en lo posible, _[funciones puras](https://twitter.com/housecor/status/1122832091413209089)_ en tu código.
- Utilizá los [métodos de Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) para operaciones que hagas con los mismos.
- Evitá el uso de [variables globales](https://www.youtube.com/watch?v=vGZGvNgZJMo).
