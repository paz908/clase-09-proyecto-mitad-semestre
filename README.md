# clase-09-proyecto-mitad-semestre

## intsrucciones

* hacer login en GitHub.com
* entrar a este repositorio disponible en [https://github.com/aud5i022-2022-1/clase-09-proyecto-mitad-semestre](https://github.com/aud5i022-2022-1/clase-09-proyecto-mitad-semestre)
* hacer click en el botón "Fork" de este repositorio para copiarlo a tu cuenta personal.
* enviar el enlace de tu repositorio y la lista de integrantes a través de u-cursos al instructor.
* ahora puedes editar este archivo siguiendo este enlace [README.md](README.md) y haciendo click en el ícono de lápiz para editar.
* recomendación: grabar tus avances seguido, para que no pierdas tu avance, para esto, baja al final de la sección de edición, elige la opción " Commit directly to the main branch." luego haz click en el botón verde "Commit changes". repite esto cada vez que quieras grabar cambios.
* para subir imágenes, haz click en este enlace a la carpeta [imagenes/](imagenes/), luego haz click en el botón "Add files" y selecciona "Upload files". arrastra tus imágenes o añadelas con el enlace "choose your files". luego elige la opción "Commit directly to the main branch" y haz click en el botón verde "Commit changes"

## contenidos de este repositorio

* carpeta [codigo_arduino/](codigo_arduino/): carpeta para tener el codigo de tu proyecto
  * archivo [odigo_arduino/codigo_arduino.ino](codigo_arduino/codigo_arduino.ino) : debe incluir encabezado y comentarios describiendo tu proyecto
* carpeta [imagenes/](imagenes/): sube aquí las imágenes para tu proyecto.
  * archivo [/imagenes/00-ejemplo.jpg](/imagenes/00-ejemplo.jpg) como ejemplo.
* archivo [README.md](README.md)]: este mismo archivo, aquí escribe tus apuntes durante el proyecto.
* archivo [README.pdf](README.pdf): este archivo pero convertido a PDF, puedes borrarlo.

## ejemplos útiles

cada párrafo es una línea continua de texto. los puntos "." son para punto seguido.
esta línea está escrita en la siguiente línea en el archivo, pero se ve seguida a la anterior.

para hacer un nuevo párrafo, hay que dejar una línea en blanco entremedio.

* las
* listas
* son
* así
  * las sub-listas
  * son así
  * con dos espacios de indentación

los enlaces se hacen con corchetes y después paréntesis. el texto dentro de corchetes es lo que se ve en el enlace, y el texto dentro de paréntesis es dónde va ese enlace. les pido que sea el mismo texto. aquí ejemplos de enlaces a web y a otros archivos dentro de este repositorio.

* [https://www.wikipedia.org/](https://www.wikipedia.org/)
* [https://www.arduino.cc/](https://www.arduino.cc/)
* [imagenes/00-ejemplo.jpg](imagenes/00-ejemplo.jpg)
* [codigo_arduino/codigo_arduino.ino](codigo_arduino/codigo_arduino.ino)

para incluir imágenes que sean visibles en este documento, es igual que un enlace a una imagen, pero con un signo de exclamación antes de los corchetes "!", así:

![texto descripción de la foto](imagenes/00-ejemplo.jpg)

## borrador de muestra

a continuación les dejo un breve borrador con ejemplos, que si completan, tendrán todos los puntos de la pauta, suerte!

## acerca de

Este proyecto de mitad de semestre fue hecho en el día martes 10 de mayo 2022, como parte del curso  aud5i022-2022-1.

Los integrantes son María Jose Pinninghoff, María Paz Figueroa Aedo.
Inicialmente queriamos incorporar un sensor de sonido para prender led en la protoboard, pero no contabamos con uno así que probamos el parlante como sensor.
Primero comprobamos con processing que el computador no tenia microfono incorporado ya que este se podia utilizar para este fin. Luego con el ejemplo Analog Input de arduino comprobamos que el parlante funcionaba como sensor de sonido.

Depues comenzamos a escribir el codigo combinando el codigo ej_03_pulsador_luz_intermitente de la clase 5 y el ejemplo Analog Input modificandolos para que al detectar el sonido se prenda el led en la protoboard.

El led no estaba conectado de manera correcta con el sensor de sonido aunque en el codigo veiamos que si, entonces detectamos que el cable que vinculaba el led con el pin 1 de arduino estaba malo, por lo tanto cambiamos el cable del pin 1 al pin 7, pero seguia sin funcionar, entonces decidimos probar si los elementos de la protoboard estaban buenos y concluimos que el cable estaba malo y ese era el error que impedia el funcinamiento del led.
Despues de verificar todas las variables logramos que el parlante funcionara como sensor de sonido detectandolo y prendiendo el led. 
![ImagenError](https://user-images.githubusercontent.com/101216595/167727246-eaaf8da1-5a82-4979-9a61-320d1d59dad8.jpg)

## lista de materiales

los materiales son:

* Arduino Uno
* protoboard
* cables
* parlante

## armado de circuito

estos son los pasos para armar el circuito.

primero hacemos X y se ve así.

![texto descripción de la foto](imagenes/00-ejemplo.jpg)

después hacemos Y y se ve así.

![texto descripción de la foto](imagenes/00-ejemplo.jpg)

## código para microcontrolador Arduino

el código está hecho para Arduino Uno, y está incluido en este repositorio aquí: [https://github.com/paz908/ProyectoMitadSemestre/blob/main/README.md](https://github.com/paz908/ProyectoMitadSemestre/blob/main/README.md).

este código está basado en los ejemplos de Arduino www.arduino.cc/ ... Examples/AnalogInput y en los ejemplos de esta clase en los enlaces [https://github.com/montoyamoraga/aud5i022-2022-1/blob/main/clases/clase-05/ej_03_pulsador_luz_intermitente/ej_03_pulsador_luz_intermitente.ino](https://github.com/montoyamoraga/aud5i022-2022-1/blob/main/clases/clase-05/ej_03_pulsador_luz_intermitente/ej_03_pulsador_luz_intermitente.ino).


## conclusiones

en este proyecto tuvimos los siguientes aprendizajes: 

* Uso del parlante como sensor de sonido
* Detección de sonido para prender luces led 
Lo más difícil de este proyecto fue escribir el codigo, saber que escribir para lograr que al momento de detectar un sonido el led se prenda.

Cometimos los siguientes errores durante el armado del circuito y en el código, teniamos repetido dos veces el pinMode(pinLed, OUTPUT) y pinMode(pinLed, INPUT) y los solucionamos eliminando uno, eso no permitia al arduino leer el codigo y prender el led que queriamos, pero al eliminar las lineas repetidas y eliminar el pinMode(pinLed, INPUT) el arduino fue capaz de hacer lo que le pediamos.

Nos gustaría expandirlo para muchos led y que se varien en intensidad al ritmo de una canción y hacerlo con un sensor de sonido capaz de detectar más frecuencias.
