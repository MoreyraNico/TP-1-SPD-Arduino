![Tinkercad](./img/ArduinoTinkercad.jpg)


## Integrantes 
Nicolas Moreyra,
Jonathan Murray
y Juan Paredes


## Proyecto: Contador binario.
Contador de 0 a 99 con Display 7 Segmentos y Multiplexación
![Tinkercad](./img/ContadorBinario.png)


## Descripción
Contador de 0 a 99 utilizando dos displays de 7 segmentos y tres botones para
controlar la cuenta. Se utiliza técnica de multiplexación para mostrar los dígitos
en los displays. 


Función Principal:
	Mediante la técnica de multiplexación podemos reutilizar los pines que alimentan un display (7 a 11), 
 para alimentar también otro display.
Cuando enviamos la información desde los pins 7-11 (dependiendo del digito que queramos formar)
para imprimir el digito en el display de unidades, debemos enviar un “0” desde A4 al COMMON de DisplayUnidad,
y un “1” desde A5 al COMMON de DisplayDecena (generando la diferencia de potencial que activara los segmentos
del display). Y al revés, para que se imprima en el display de las decenas. Se ajustan los delays en las funciones 
correspondientes para que sea imperceptible a la vista y de la sensación de que ambos están prendidos a la vez.
Se implementarán contadores que lleven la cuenta, a medida que se presionen los botones de incremento de cuenta 
(ButtomUp), de decrecimiento (ButtomDown), y un botón de reseteo (ButtomReset) que vuelve la cuenta a 0.
FUNCIONES PRINCIPALES DEL CODIGO:
void loop()
// Control de los pulsadores y contadores.
// Recibe: Toma los datos de la función "ControladorPulsadores". Incrementará/disminuirá/reseteará contadores.
// Devuelve: Dato del contador para la función ControlUnidadDecena
*para más detalle revisar código comentado línea por linea
ControladorPulsadores()
// FUNCION CONTROL DE PULSADORES 
// Recibe: Lees el estado de los pulsadores
// Devuelve: Identifica que pulsador se presionó, para ser procesados en el loop
*para más detalle revisar código comentado línea por linea
ControlUnidadDecena()
// FUNCION CONTROL DE UNIDAD Y DECENAS
// Procesa el dato del contador, para que sea proyectado en los displays
// Dispara los pulsos para el multiplexado
*para más detalle revisar código comentado línea por linea
ControladorMultiplexado()
//FUNCION CONTROLADORA DE MULTIPLEXADO
// Se encarga del multiplexado
// Controla los tiempos de encendido de los display, alternando sus encendidos con un tiempo de delay bajo para que sea imperceptible.
*para más detalle revisar código comentado línea por linea
ControladorDisplay()
// FUNCION CONTROLADOR DE DISPLAYS
// Control de encendido de cada segmento que imprime el digito deseado.
*para más detalle revisar código comentado línea por linea
