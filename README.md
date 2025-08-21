# Saber Y Vargar

> El hacedor de trivials para toda la familia.

[Descarga](https://github.com/varguiniano/SaberYVargar/releases/download/0.0.3/SaberYVargar.7z)

## Cómo hacer tu joeguito

Las pantallas que aparecerán en tu juego se encuentrarán dentro de la carpeta Screens. La descarga viene con una carpeta Screens con el último trivial que hice, además de una carpeta Screens-Templates con un ejemplo de cada pantalla disponible. La carpeta Screens que hagas para tu juego debe de tener los siguientes archivos:

- TitleScreen.json.
  En este archivo configurarás el título que se verá en la primera pantalla.
- ScreenLayout.json.
  Este archivo contendrá una lista de todas las pantallas que quieras que tenga el juego (Value) y el tipo de cada pantalla(Key). Los tipos se detallan más adelante.
- Un archivo .json por cada pantalla de tu juego. La forma más sencilla de hacer estos archivos es copiarte el archivo de ejemplo del tipo de pregunta que quieras y modificarlo.
- Un archivo .jpg por cada imagen que uses. Por el momento las imágenes tienen que ser cuadradas para quedar bien, en un futuro será más flexible. Las puedes apañar en tu editor de imágenes de confianza.
- Un archivo .wav por cada audio que uses.


### Tipos de pantalla.
Los tipos disponibles son:

#### Tipo 0
Una pantalla con un único texto.

> Ejemplo: Screens-Templates/InstructionsScreen.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- MainText: El texto a mostrar.

#### Tipo 1
Una pregunta sencilla con una respuesta.

> Ejemplo: Screens-Templates/Question1.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- Question: El texto de la pregunta.
- Answer: La respuesta a la pregunta.

#### Tipo 2
Una pregunta sencilla acompañada de una imagen y una respuesta.

> Ejemplo: Screens-Templates/Question2.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- Question: El texto de la pregunta.
- Image: Imagen que acompaña a la pregunta.
- Answer: La respuesta a la pregunta.

#### Tipo 3
Una pregunta de tipo test.

> Ejemplo: Screens-Templates/Question3.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- Question: El texto de la pregunta.
- Options: Listado de las opciones disponibles.
- Answer: Un número que indica la opción correcta de entre las anteriores (empezando por 0).

#### Tipo 4
Una pregunta de tipo test con una imagen asociada.

> Ejemplo: Screens-Templates/Question4.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- Question: El texto de la pregunta.
- Image: Imagen que acompaña a la pregunta.
- Options: Listado de las opciones disponibles.
- Answer: Un número que indica la opción correcta de entre las anteriores (empezando por 0).

#### Tipo 5
Una ráfaga de preguntas con múltiples respuestas que se van eliminando.

> Ejemplo: Screens-Templates/Question5.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- Questions: Listado de todas las preguntas a mostrar.
- Options: Listado de todas las respuestas.
- Answers: Listado que muestra la equivalencia entre las preguntas y las opciones. El orden de este listado corresponde con el orden de las preguntas (el primer elemento será respuesta a la primera pregunta), el número a indicar es la posición en la que se encuentra la respuesta en las opciones (empezando por 0). Por ejemplo, en el archivo de ejemplo. El plátano está en la primera posición en las preguntas y en el listado de opciones aparece el número 3 en la primera posición, indicando que la respuesta correspondiente al plátano es la número 3 en la lista de opciones, que corresponde con el texto amarillo.

#### Tipo 6
Como la 5 pero con imagenes en vez de preguntas.

> Ejemplo: Screens-Templates/Question6.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- Images: Listado de todas las imágenes (preguntas) a mostrar.
- Options: Listado de todas las respuestas.
- Answers: Listado que muestra la equivalencia entre las preguntas y las opciones. El orden de este listado corresponde con el orden de las preguntas (el primer elemento será respuesta a la primera pregunta), el número a indicar es la posición en la que se encuentra la respuesta en las opciones (empezando por 0).

#### Tipo 7
Como la 5 pero con audios en vez de preguntas.

> Ejemplo: Screens-Templates/Question7.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- Audios: Listado de todos los audios (preguntas) a reproducir.
- Options: Listado de todas las respuestas.
- Answers: Listado que muestra la equivalencia entre las preguntas y las opciones. El orden de este listado corresponde con el orden de las preguntas (el primer elemento será respuesta a la primera pregunta), el número a indicar es la posición en la que se encuentra la respuesta en las opciones (empezando por 0).

#### Tipo 8
Una frase en blanco que ha de resolverse como un ahorcado, con un botón para cada letra del abecedario.

> Ejemplo: Screens-Templates/Question8.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- Text: La frase que ha de adivinarse.

#### Tipo 9
Como la 8 pero en vez un botón para cada letra del abecedario, hay una "ruleta de la suerte" con diferentes opciones.

> Ejemplo: Screens-Templates/Question9.json.

Datos a rellenar.
- BackButtonOverride: Si es diferente de -1, en vez de ir a la pantalla anterior al dar al botón de atrás irá a la pantalla con el íncide indicado en este campo.
- Title: El título superior de la pantalla.
- Text: La frase que ha de adivinarse.

Una vez hayas terminado de preparar todas tus preguntas y las hayas puesto en el listado del ScreenLayout.json, puedes ejecutar SaberYVargar.exe para empezar tu joeguito.

## Controles.
- Las flechas izquierda y derecha (o los botones en la parte superior de la pantalla) cambian entre pantallas.
- Las flechas arriba y abajo saltarán entre el contenido de cada pantalla. En pantallas sencillas de una pregunta solo mostrarán el texto. En preguntas de test irán mostrando las opciones de una en una. En preguntas de ráfada mostrarán primero las respuestas y luego irán sacando preguntas de una en una. En la pantalla de ruleta activará la ruleta.
- La tecla A muestra la respuesta a una pregunta si la hubiese.
- La tecla P vuelve a reproducir el audio actual en la pregunta de tipo 7.
- Con el ratón puedes pulsar en todas las cosas que parecen botones.
- Para cerrar la app alt+f4 porque soy un vago.
