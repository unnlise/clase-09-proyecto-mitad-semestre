# clase-09-proyecto-mitad-semestre

## acerca de

este proyecto de mitad de semestre fue hecho en el día martes 10 de mayo 2022, como parte del curso  aud5i022-2022-1.
Se pretende crear imágenes a través de la recepción de sonidos mediante Arduino, priorizando ciertos valores especificos. (#definir NOTA_DO4 262)

los integrantes son Valentina Quelca, Dani Reyes.

## lista de materiales

los materiales son:

* Arduino Uno
* protoboard
* cables
* micrófono/parlante
* etc

## armado de circuito

estos son los pasos para armar el circuito.

primero conectamos el microfono al protoboard y al puerto análogo 0 de arduino.

luego conectamos un cable desde GND de Arduino al negativo del protoboard y otro cable desde 5V de Arduino al positivo del protoboard.

## código para microcontrolador Arduino

este código está basado en los ejemplos de Arduino

* https://create.arduino.cc/projecthub/lbf20012001/musical-note-detector-b9a579
* https://create.arduino.cc/projecthub/abhilashpatel121/arduino-music-notes-and-chord-detector-728b14
*  https://processing.org/examples/storinginput.html
  
y en los ejemplos de esta clase en los enlaces
* https://github.com/montoyamoraga/aud5i022-2022-1/blob/main/clases/clase-07/ej_00_probar_parlante/ej_00_probar_parlante.ino
* https://github.com/montoyamoraga/aud5i022-2022-1/tree/main/clases/clase-07/ej_01_melodia

primero creamos las variables "sonido" para almacenar valores. la variable "sonido" es análoga.

primero en setup() definimos los valores en los que un sonido sea reconocible.

luego en loop() leemos las entradas AO para que cada vez que Arduino capte un valor que sea considerado como sonido reconocible, este sea leído. 

Luego importamos el codigo de Arduino a Processing como serial y le añadimos en draw() los comandos de tamaño de lienzo, color de fondo, y draw() para que cada vez que un sonido sea captado por Arduino, una imagen sea generada en el reproductor de Processing.

## conclusiones

Logramos un avance en entender como compatibilizar arduino con processing, al intentar traducir señales analogas en visualizaciones digitales.

Fuimos capaces de aislar un valor en especifico y que arduino trabajara solo con ese valor, ignorando la información que no nos era relevante, planeabamos generar información visual mediante la recepción de los datos analogos especificados, descubrimos de manera tardía que las habilidades para completar la tarea propuesta eran de un nivel mayor al que teníamos.

Nuestro ideal era crear representaciones visuales dinámicas, que cambiaran a medida que Arduino recibiera información.
