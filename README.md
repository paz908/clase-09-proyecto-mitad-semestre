# clase-09-proyecto-mitad-semestre





## acerca de

Este proyecto de mitad de semestre fue hecho en el día martes 10 de mayo 2022, como parte del curso  aud5i022-2022-1.

Los integrantes son María Jose Pinninghoff, María Paz Figueroa Aedo.
Inicialmente queriamos incorporar un sensor de sonido para prender led en la protoboard, pero no contabamos con uno así que probamos el parlante como sensor.
Primero comprobamos con processing que el computador no tenia microfono incorporado ya que este se podia utilizar para este fin. Luego con el ejemplo Analog Input de arduino comprobamos que el parlante funcionaba como sensor de sonido.

Depues comenzamos a escribir el codigo combinando el codigo ej_03_pulsador_luz_intermitente de la clase 5 y el ejemplo Analog Input modificandolos para que al detectar el sonido se prenda el led en la protoboard.

El led no estaba conectado de manera correcta con el sensor de sonido aunque en el codigo veiamos que si, entonces detectamos que el cable que vinculaba el led con el pin 1 de arduino estaba malo, por lo tanto cambiamos el cable del pin 1 al pin 7, pero seguia sin funcionar, entonces decidimos probar si los elementos de la protoboard estaban buenos y concluimos que el cable estaba malo y ese era el error que impedia el funcinamiento del led.
Despues de verificar todas las variables logramos que el parlante funcionara como sensor de sonido detectandolo y prendiendo el led. 

![Parlante Sensor](https://user-images.githubusercontent.com/101216595/167727737-02aa84fb-0b0c-47c4-b22f-e75d1d29978f.jpg)

![Circuito](https://user-images.githubusercontent.com/101216595/167728098-d402c381-aa43-4965-bb1b-fd61e275dfa7.jpg)






## lista de materiales

los materiales son:

* Arduino Uno
* protoboard
* cables
* parlante

## armado de circuito

estos son los pasos para armar el circuito.

paso 1.  
![Circuito en la protoboard](https://user-images.githubusercontent.com/101216595/167728110-0b3df127-2f29-4fd1-8caf-0d99decc95b1.jpg)



paso 2 y se ve así.

![Circuito en el arduino](https://user-images.githubusercontent.com/101216595/167728126-cdb60a41-c0d0-4bf5-bc66-0d7158eb976e.jpg) 



## código para microcontrolador Arduino

el código está hecho para Arduino Uno, y está incluido en este repositorio aquí: [https://github.com/paz908/ProyectoMitadSemestre/blob/main/README.md](https://github.com/paz908/ProyectoMitadSemestre/blob/main/README.md).

este código está basado en los ejemplos de Arduino www.arduino.cc/ ... Examples/AnalogInput y en los ejemplos de esta clase en los enlaces [https://github.com/montoyamoraga/aud5i022-2022-1/blob/main/clases/clase-05/ej_03_pulsador_luz_intermitente/ej_03_pulsador_luz_intermitente.ino](https://github.com/montoyamoraga/aud5i022-2022-1/blob/main/clases/clase-05/ej_03_pulsador_luz_intermitente/ej_03_pulsador_luz_intermitente.ino).


## conclusiones

en este proyecto tuvimos los siguientes aprendizajes: 

* Uso del parlante como sensor de sonido
* Detección de sonido para prender luces led 
Lo más difícil de este proyecto fue escribir el codigo, saber que escribir para lograr que al momento de detectar un sonido el led se prenda.

Cometimos los siguientes errores durante el armado del circuito y en el código, teniamos repetido dos veces el pinMode(pinLed, OUTPUT) y pinMode(pinLed, INPUT) y los solucionamos eliminando uno, eso no permitia al arduino leer el codigo y prender el led que queriamos, pero al eliminar las lineas repetidas y eliminar el pinMode(pinLed, INPUT) el arduino fue capaz de hacer lo que le pediamos.

![Error](https://user-images.githubusercontent.com/101216595/167727246-eaaf8da1-5a82-4979-9a61-320d1d59dad8.jpg)

Nos gustaría expandirlo para muchos led y que se varien en intensidad al ritmo de una canción y hacerlo con un sensor de sonido capaz de detectar más frecuencias.
