<nav style="background-color: #fff712;"><nav style="width: 90%; display: block; margin-left: auto; margin-right: auto;">
<h2 style="text-align: center;">&nbsp;</h2>
<h2 style="text-align: center;"><span style="color: #000000;"><strong>Matriz LED</strong></span></h2>
<p style="text-align: justify;"><span style="color: #000000;">El LED es una fuente de luz constituida por un material semiconductor dotado de dos terminales. Es una alternativa rentable de bajo consumo en comparaci&oacute;n con otras fuentes de luz como los bombillos o las l&aacute;mparas fluorescentes.</span></p>
<p style="text-align: justify;"><span style="color: #000000;">Para este proyecto utilizamos LEDs blancos ultra brillantes que funcionan con un voltaje de 3.5v a 20mA dise&ntilde;amos una matriz bastante sencilla que necesita una fuente de alimentaci&oacute;n de 12v y 600mA para funcionar.</span></p>
<p style="text-align: justify;"><span style="color: #000000;">Usamos este simple circuito para encender 2 LEDs su corriente es de 22mA y nuestro reflector ser&aacute; de 50 LEDs as&iacute; que pusimos el circuito 25 veces de la misma fuente, la corriente total de la matriz es de 550mA.</span></p>
<p style="text-align: justify;"><span style="color: #000000;">Usamos una placa fen&oacute;lica de 5cm x 10cm donde acomodamos los LEDs con el programa proteus hicimos el dise&ntilde;o para la placa fen&oacute;lica.</span></p>
<p>&nbsp;</p>
<p>&nbsp;<img style="display: block; margin-left: auto; margin-right: auto;" src="https://github.com/LuisQuiroga30/reflector_led/blob/master/circuito_led.jpg?raw=true" alt="" width="30%" /></p>
<p>&nbsp;</p>
</nav></nav><nav style="background-color: #46ba34;"><nav style="width: 90%; display: block; margin-left: auto; margin-right: auto;">
<h2 style="text-align: center;">&nbsp;</h2>
<h2 style="text-align: center;"><span style="color: #ffffff;"><strong>APP Android</strong></span></h2>
<p style="text-align: justify;"><span style="color: #ffffff;">Para poder controlar cualquier proyecto con un Smartphone es necesario dise&ntilde;ar una app que tenga la tarea de enviar datos al microcontrolador.</span></p>
<p style="text-align: justify;"><span style="color: #ffffff;">Se usar&aacute; una herramienta web creada por Google labs para crear la app que vamos a utilizar, APP inventor es una p&aacute;gina web donde se puede dise&ntilde;ar una app de manera muy sencilla para despu&eacute;s programarla con diagrama de bloques.</span></p>
<p style="text-align: justify;"><span style="color: #ffffff;">La app que dise&ntilde;amos cuenta con 1 bot&oacute;n de conexi&oacute;n bluetooth este nos sirve para establecer una conexi&oacute;n entre el m&oacute;dulo HC-05 y nuestro Smartphone, 1 bot&oacute;n ON que env&iacute;a un valor &ldquo;A&rdquo; al m&oacute;dulo HC-05, 1 bot&oacute;n OFF que env&iacute;a un valor &ldquo;B&rdquo; y 1 slider que env&iacute;a valores de entre &ldquo;0&rdquo; y &ldquo;9&rdquo;.</span></p>
<p>&nbsp;<img style="display: block; margin-left: auto; margin-right: auto;" src="https://github.com/LuisQuiroga30/reflector_led/blob/master/dimer_bt.png?raw=true" alt="" width="50%" /></p>
<p>&nbsp;</p>
</nav></nav><nav style="background-color: #139c9c;"><nav style="width: 90%; display: block; margin-left: auto; margin-right: auto;">
<h2 style="text-align: center;">&nbsp;</h2>
<h2 style="text-align: center;"><span style="color: #ffffff;"><strong>Arduino + BT</strong></span></h2>
<p><span style="color: #ffffff;">Arduino es una placa electr&oacute;nica de c&oacute;digo abierto basada en hardware y software f&aacute;ciles de usar. Las placas Arduino pueden leer entradas (comandos recibidos por un m&oacute;dulo HC-05) y convertirla en una salida: encender un LED y variar la intensidad de luz del mismo.</span></p>
<p><span style="color: #ffffff;">Usaremos un microcontrolador Arduino para la realizaci&oacute;n de nuestro proyecto este se encargar&aacute; de recibir por medio de comunicaci&oacute;n serial comandos del m&oacute;dulo HC-05. El m&oacute;dulo HC-05 es ideal para utilizar en todo tipo de proyectos donde necesites una conexi&oacute;n inal&aacute;mbrica bluetooth fiable y sencilla de utilizar.</span></p>
<p><br /><span style="color: #ffffff;"> La conexi&oacute;n con el microcontrolador es muy sencilla:</span></p>
<p><span style="color: #ffffff;"><img style="display: block; margin-left: auto; margin-right: auto;" src="https://github.com/LuisQuiroga30/reflector_led/blob/master/conexion.png?raw=true" alt="" width="80%" /></span></p>
<p><span style="color: #ffffff;">&nbsp;</span></p>
<p><span style="color: #ffffff;">Para accionar el LED usaremos una salida PWM del microntrolador. Es una se&ntilde;al cuadrada de alta frecuencia a la que se le puede cambiar el ancho de pulso, para un LED esta se&ntilde;al es como si encendiera y apagara a alta velocidad tan alta que no es visible para el ojo humano, sin embargo, se aprecia la disminuci&oacute;n de luz en el LED.</span></p>
<p><span style="color: #ffffff;">Como la matriz que vamos a manejar funciona con 12v y la salida que maneja el microcontrolador es de 5v es necesario utilizar un transistor, para este proyecto usaremos un transistor MOSFET Tipo-n este tipo de transistor funciona como un interruptor que permanece abierto si no se le aplica voltaje a la compuerta, y se cierra al energizar la compuerta.</span></p>
<p><span style="color: #ffffff;">Esto nos sirve por que la PWM enviara una se&ntilde;al cuadrada al transistor y este funcionara como un interruptor encendiendo y apagando la se&ntilde;al GND de la matriz a la misma frecuencia que el arduino.</span></p>
<p><span style="color: #ffffff;">Como se menciona anteriormente es necesario una fuente de 12v para el matriz led, sin embargo, no se recomienda encender el microcontrolador con este voltaje, para seguridad usaremos un regulador de 5v para encender nuestro microcontrolador.</span></p>
<p><span style="color: #ffffff;">Las conexiones quedar&iacute;an de la siguiente manera:</span></p>
<p>&nbsp;</p>
<h3 style="text-align: center;"><span style="color: #ffffff;">Programaci&oacute;n</span></h3>
<p><span style="color: #ffffff;">Es necesario un c&oacute;digo muy simple para la realizaci&oacute;n de este proyecto, el c&oacute;digo utilizado fue el siguiente:</span></p>
<p><span style="color: #ffffff;"><textarea style="margin: 0px; width: 95%;" cols="40" name="comentarios" rows="10">int ledPin = 9; // usamos un pin PWM de salida al LED
byte lectura; // Declaramos una variable para guardar las lecturas del módulo hc-05

void setup() {
    pinMode(ledPin, OUTPUT);   //Declara pin de Salida
    digitalWrite(ledPin, LOW); //Normalmente Apagado
    Serial.begin(9600);
}
 
void loop() {
  
  if(Serial.available() &gt; 0){ //Si se recibe cualquier valor
       lectura = Serial.read(); //Guardar el valor en lectura
       if(lectura == 'A'){ //si la lectura es igual a "A"
        digitalWrite(ledPin, HIGH);//Encender el LED
       }
       else if(lectura == 'B'){ //si la lectura es igual a "B"
        digitalWrite(ledPin, LOW); //Apagar el LED
       }
       else{ //si se recibe cualquier valor excepto "A" y "B"
        lectura = map(lectura, 48, 57, 0, 9); //convertir valores de lectura de entre 48 y 57 a valores enteros entre 0 y 9
        Serial.print("Lectura: "); //escribir "Lectura: " en el monitor serial
        Serial.println(lectura); //escribir el valor de lectura en el monitor serial
        lectura = map(lectura, 48, 57, 0, 255); //convertir valores de lectura de entre 0 y 9 a valores enteros entre 0 y 255
        analogWrite(ledPin, lectura); //escribir analogamente en el pin de salida
      }
  }
}</textarea></span></p>
</nav></nav>
<p>&nbsp;</p>
<h2 style="text-align: center;">Dise&ntilde;o de Carcasa</h2>
<p>Para crear el dise&ntilde;o de la carcasa para nuestro proyecto utilizamos el programa solidwork dise&ntilde;amos las piezas por partes&nbsp; comenzando con la base. Principalmente comenzamos midiendo la baquelita y el arduino y as&iacute; saber la medida &nbsp;que nuestro circuito necesita para estar fijo, la medida de profundidad es de 60 mm, &nbsp;despu&eacute;s calcular la distancia en que colocar&iacute;amos la l&aacute;mpara led y el arduino con una altura de 35 mm para la l&aacute;mpara y al fondo, que son 55 mm colocamos el arduino. Para la mica dise&ntilde;amos dos pesta&ntilde;as haci&eacute;ndolas parecer un riel de 4 mm de altura para insertar la mica de la cual las medidas son de largo 10.5 mm, de ancho 7.5 mm y de grosor de 3 mm, para finalizar las extruimos a 120 mm de largo.</p>
<p>Despu&eacute;s dise&ntilde;amos las tapas de la carcasa con una longitud que cubriera toda la carcasa de 80 mm&nbsp; de ancho de la parte de superior, 55 mm&nbsp; en la parte inferior y una con una altura de 60 mm&nbsp; y luego lo extruimos con un grosor de 4 mm.</p>
<p>Para finalizar con todo&nbsp; el dise&ntilde;o creamos al &uacute;ltimo el arco que sostiene la carcasa de la l&aacute;mpara con una longitud de 130 mm, una altura de 70mm y una anchura de 3 mm, para finalizar la extruimos&nbsp; a 20mm.</p>
<p>&nbsp;Este fue el proceso para crear el dise&ntilde;o de la carcasa que cubre la l&aacute;mpara de led y el arduino.&nbsp;&nbsp;</p>
