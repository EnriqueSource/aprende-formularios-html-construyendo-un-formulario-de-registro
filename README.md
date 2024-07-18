# Aprende formularios HTML construyendo un formulario de registro

Formulario web creado en el curso "Aprende formularios HTML construyendo un
formulario de registro", perteneciente a la certificación "Diseño Web
Responsivo" de freeCodeCamp.

- - -

[Enlace al Formulario](https://registration-form-bde.netlify.app/)

- - -
> **Nota:** Puedes hacer uso de formularios HTML para recopilar información de
> las personas que visitan tu página web. En este curso, aprenderás formularios
> de HTML construyendo una página de registro. Aprenderás cómo controlar qué tipo
> de datos pueden colocarse en tu formulario, y herramientas nuevas de CSS para
> cambiar el diseño de tu página.
> 
>   -- freeCodeCamp

> **Nota:** Un viewport representa la región poligonal (normalmente rectangular)
> en gráficas de computación que está siendo visualizada en ese instante. En
> términos de navegadores web, se refiere a la parte del documento que usted está
> viendo, la cual es actualmente visible en su ventana (o la pantalla, si el
> documento está siendo visto en modo pantalla completa). El contenido fuera del
> viewport no es visible en la pantalla hasta que sea desplazado dentro de él.
> 
>   — Mozilla Developer Network

- La unidad `vh` (viewport height) representa la altura de la ventana gráfica o `
  viewport` . Por defecto es igual al 1% de la altura del `viewport` . eso lo
  hace relativo a la altura del `viewport` . \!!!!!!!!!esta oración no se
  entiende muy bien. intentar arreglarla después.
- Podemos deshacernos de la barra de desplazamiento lateral de nuestra pagina
  dándole al `body`  un `margin: 0;` .
- Si en CSS, con `background-color`  podemos cambiar el color de fondo del `body`
  , con la propiedad `color`  podemos cambiar el color de los elementos que hay
  dentro del `body` , como por ejemplo texto. Todo esto podemos hacerlo desde el
  mismo bloque CSS del siguiente modo:

  ```
  body {   
    background-color: back;   
    color: white;   
    }
  ```
- Formularios (atributos):
- `action` : dirección a la cual se envían los datos introducidos por el usuario.
- `method` : especifica como enviar los datos a la dirección indicada en `action`
  .
-    Mediante el atributo `method` podemos enviar los datos con las solicitudes:
-     `get` :  los datos se envían como parámetros dentro de la **URL**
-     `post` : los datos son enviados en el **cuerpo** de la solicitud.
- Con el elemento `\\\<fieldset>` agregamos diferentes secciones a nuestro
  formulario.
- El elemento `\\\<label>`  alberga los diferentes campos del formulario como *
  nombre* , *dirección de e-mail* , etc.
- Los elementos `\\\<label>` son por defecto **inline** . Para que se vean en
  lineas diferentes, debemos agregar el atributo `display: block;` al elemento `
  label` .
- La unidad de medida `rem` significa: root em. Esta unidad es relativa al
  tamaño de fuente del elemento `\\\<html>` .
- Con el elemento `\\\<input />` creamos los campos de entrada de datos.
- con el atributo `for` conectamos cada `\\\<input />` con su respectivo `
  \\\<label>` .
- Con el atributo `type` el navegador puede saber que datos esperar de ese
  campo. Si no se especifica ningún atributo `type` , el navegador utilizará por
  defecto `text` .
- Atributos type son:
  - text
  - email
  - password

- El primer elemento `\\\<input />` que contenga un `type`  de `submit` se
  establece **automáticamente** para enviar a su elemento `\\\<form>` más
  cercano.
- Para que el formulario sea mas interactivo, añadimos el atributo `required` a
  los elementos `\\\<input />` . De ese modo, si el usuario intenta enviar el
  formulario con campos sin rellenar, aparecerá un mensaje indicando que faltan
  campo por rellenar.
- Los valores del atributo `type` pueden contener validación. Algunos, como el
  valor `email` , tienen validación por defecto, evitando la entrada de una
  dirección de email invalida. A otros, como `password` , se les puede agregar
  validación mediante un atributo. Un ejemplo para que la contraseña no sea
  inferior a 8 caracteres es:
- `\\\<inputid="new-password"type="password" minlength="8" required />`
- En este caso, el atributo agregado es `minlength="8"`
- Para `type="password"` existe también el atributo `pattern` . Mediante `pattern`
  podemos hacer uso de **expresiones regulares** para requerir un determinado
  patrón para la contraseña.
- `\\\<label for="new-password">Create a New Password:
  \\\<inputid="new-password" type="password" pattern="\\\[a-z0-5]{8,}
  "required/>`
- En el código de arriba especificamos que los datos introducidos en el campo
  por el usuario, pueden ser caracteres desde la `a` hasta la `z` , números
  desde el `0` hasta el `5` y que la serie de la contraseña debe de tener al
  menos 8 caracteres o más de longitud
- Recuerda: para hacer que dos botones de tipo `radio` no puedan ser
  seleccionados a la vez, debemos de añadir un atributo nombre a cada uno de
  ellos, dándole el mismo valor (el mismo nombre) a los dos.
- Aunque hemos solucionado el problema de la selección única del tipo `radio` ,
  el usuario aún puede enviar un `submit` sin haber seleccionado ninguno de los
  dos `radio` . Anteriormente hemos usado el atributo `required` , pero en este
  caso no es buena idea usarlo, ya que  habilitar ambos `radio` como requeridos `
  required` no permite al usuario seleccionar un solo `radio` , ya que ambos
  serán requeridos.
- Para solucionar el problema anterior, podemos dar algo de contexto al
  usuario. Agregamos el titulo `Account type (required)` a dicha sección y le
  damos el atributo `checked` al primero de los dos `radio` .
- Recuerda: por motivos de buenas practicas, recuerda siempre vincular a un 
  `\\\<input />` con su correspondiente `label` mediante los atributos `for`
  para el elemento `label`  e `id` para el elemento `\\\<input />` .
- Mediante un `\\\<input />` de tipo `file` permitimos al usuario que suba un
  archivo, como por ejemplo una foto.
- Con los atributos `min`  y `max` podemos asignar unos valores por defecto a
  los introducidos por el usuario en el `\\\<input />` . Esto es muy útil por
  ejemplo, en un `\\\<input />` de tipo `number` con el que queremos saber si el
  usuario es mayor de edad o no.
- Podemos añadir un menú desplegable al formulario con el elemento `\\\<select>`
  . El elemento `\\\<select>` es un contenedor para un grupo de elementos `
  \\\<option>` . El elemento `\\\<optio>` actúa como una etiqueta para cada
  opción desplegable.
- Para la introducción de textos mas largos por parte del usuario, tenemos el
  elemento `\\\<textarea>` . A diferencia del `\\\<input />` de tipo `text` , `
  \\\<textarea>` puede recibir **texto de varias líneas** y un número inicial de
  \** filas** y **columnas** .
- Es buena practica \**vincular todos los elementos de formulario ** (
  `\\\<select>` , `\\\<textarea>` , …) no solo los `\\\<input />` . Como ya
  sabemos, el vinculo lo creamos con los atributos `for` para `\\\<label>` e `id`
  para el elemento.
- Podemos modificar el tamaño inicial de `\\\<textarea>` . Para ello tenemos las
  propiedades `rows` (filas) y `cols` (columnas)
- `\\\<textarea id="bio" rows="3" cols="30" >\\\</text area>`
- También es una buena practica agregar el atributo `name` a todos los elementos
  de un formulario.
- La propiedad `text-align` posiciona un elemento horizontalmente.
- La unidad `vw` (viewport width) representa la anchura de la ventana gráfica o  `
  viewport` .
- La pseudo-clase CSS `:last-of-type{}` nos permite seleccionar el ultimo
  elemento de un tipo especifico:
- `fieldset:last-of-type { border-bottom:none; }`
- Al dar un `width` del `100%` a todos los `\\\<fieldset>` , puede que alguno de
  los mismos no quede bien alineado (por ejemplo en un `\\\<input />` de tipo `
  radio` ). Para solucionar ese `radio` en especifico, haremos uso de la
  propiedad `unset` . Añadiendo una clase al o a los elementos <`input />` que
  queremos modificar en el HTML , llamaremos a dicha clase desde el CSS y le
  daremos la propiedad `width` con el valor `unset`
- La propiedad `verticla-align` de CSS especifica el alineado vertical de un **
  elemento en línea**  o una celda de una tabla. — Mozilla Developer Network
- Con la propiedad `min-height` hacemos que el elemento especificado no sea mas
  pequeño (en altura) del `min-height` dado.
- Otro **selector CSS** que podemos utilizar es el selector de atributos
  (attribute). Este selecciona un elemento basado en el valor del atributo
  dado. Un ejemplo sería:
- `input\\\[type="submit"] {}`
- Con un `display: block` el elemento se sitúa a ras del borde izquierdo de su
  elemento padre. Podemos centrarlo con un `margin: 0 auto`
- Fin
