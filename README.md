# Saber Y Vargar

> El hacedor de trivials para toda la familia.

[Descarga](https://github.com/varguiniano/SaberYVargar/releases/download/0.0.1/SaberYVargar.7z)

## Cómo hacer tu joeguito

Las pantallas que aparecerán en tu juego se encuentrarán dentro de la carpeta Screens. La descarga viene con una carpeta Screens con el último trivial que hice, además de una carpeta Screens-Templates con un ejemplo de cada pantalla disponible. La carpeta Screens que hagas para tu juego debe de tener los siguientes archivos:

- TitleScreen.json.
  En este archivo configurarás el título que se verá en la primera pantalla.
- ScreenLayout.json.
  Este archivo contendrá una lista de todas las pantallas que quieras que tenga el juego (Value) y el tipo de cada pantalla(Key). Los tipos se detallan más adelante.
- Un archivo json por cada pantalla de tu juego.
- Un archivo .jpg por cada imagen que uses. Por el momento las imágenes tienen que ser cuadradas para quedar bien, en un futuro será más flexible. Las puedes apañar en tu editor de imágenes de confianza.


### Tipos de pantalla.
Los tipos disponibles son:

#### Tipo 0
Una pantalla con un único texto.

> Ejemplo: Screens-Templates/InstructionsScreen.json.

Datos a rellenar.
- Title: El título superior de la pantalla.
- MainText: El texto a mostrar.

#### Tipo 1
Una pregunta sencilla con una respuesta.

> Ejemplo: Screens-Templates/Question1.json.

Datos a rellenar.
- Title: El título superior de la pantalla.
- Question: El texto de la pregunta.
- Answer: La respuesta a la pregunta.

#### Tipo 2
Una pregunta sencilla acompañada de una imagen y una respuesta.

> Ejemplo: Screens-Templates/Question2.json.

Datos a rellenar.
- Title: El título superior de la pantalla.
- Question: El texto de la pregunta.
- Image: Imagen que acompaña a la pregunta.
- Answer: La respuesta a la pregunta.

#### Tipo 3
Una pregunta de tipo test.

> Ejemplo: Screens-Templates/Question3.json.

Datos a rellenar.
- Title: El título superior de la pantalla.
- Question: El texto de la pregunta.
- Options: Listado de las opciones disponibles.
- Answer: Un número que indica la opción correcta de entre las anteriores (empezando por 0).

#### Tipo 4
Una pregunta de tipo test con una imagen asociada.

> Ejemplo: Screens-Templates/Question4.json.

Datos a rellenar.
- Title: El título superior de la pantalla.
- Question: El texto de la pregunta.
- Image: Imagen que acompaña a la pregunta.
- Options: Listado de las opciones disponibles.
- Answer: Un número que indica la opción correcta de entre las anteriores (empezando por 0).

#### Tipo 5
Una ráfaga de preguntas con múltiples respuestas que se van eliminando.

> Ejemplo: Screens-Templates/Question5.json.

Datos a rellenar.
- Title: El título superior de la pantalla.
- Questions: Listado de todas las preguntas a mostrar.
- Options: Listado de todas las respuestas.
- Answers: Listado que muestra la equivalencia entre las preguntas y las opciones. El orden de este listado corresponde con el orden de las preguntas (el primer elemento será respuesta a la primera pregunta), el número a indicar es la posición en la que se encuentra la respuesta en las opciones (empezando por 0). Por ejemplo, en el archivo de ejemplo. El plátano está en la primera posición en las preguntas y en el listado de opciones aparece el número 3 en la primera posición, indicando que la respuesta correspondiente al plátano es la número 3 en la lista de opciones, que corresponde con el texto amarillo.

#### Tipo 6
Como la 5 pero con imagenes en vez de preguntas.

> Ejemplo: Screens-Templates/Question6.json.

- Title: El título superior de la pantalla.
- Images: Listado de todas las imágenes (preguntas) a mostrar.
- Options: Listado de todas las respuestas.
- Answers: Listado que muestra la equivalencia entre las preguntas y las opciones. El orden de este listado corresponde con el orden de las preguntas (el primer elemento será respuesta a la primera pregunta), el número a indicar es la posición en la que se encuentra la respuesta en las opciones (empezando por 0).

Una vez hayas terminado de preparar todas tus preguntas y las hayas puesto en el listado del ScreenLayout.json, puedes ejecutar SaberYVargar.exe para empezar tu joeguito.

## Controles.
- Las flechas izquierda y derecha (o los botones en la parte superior de la pantalla) cambian entre pantallas.
- Las flechas arriba y abajo saltarán entre el contenido de cada pantalla. En pantallas sencillas de una pregunta solo mostrarán el texto. En preguntas de test irán mostrando las opciones de una en una. En preguntas de ráfada mostrarán primero las respuestas y luego irán sacando preguntas de una en una.
- La tecla a muestra la respuesta a una pregunta si la hubiese.
- Con el ratón puedes pulsar en todas las cosas que parecen botones.
- Para cerrar la app alt+f4 porque soy un vago.
