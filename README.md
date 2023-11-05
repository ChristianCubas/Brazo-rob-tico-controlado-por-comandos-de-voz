El brazo robótico desarrollado aplica los conceptos de sensores y actuadores algunos de forma indirecta; es decir, en este caso se hace de uso la librería de reconocimiento de voz quien hace uso de micrófono de la computadora para poder analizar e identificar el mensaje por voz realizado, este micrófono es nuestro sensor indirectamente este al igual que los sensores sirve como entrada de datos del exterior en este caso de nuestra voz este micrófono como el periférico que es sirve de entrada de datos quien a su vez usa el bus de datos para transmitir los datos recibidos del micrófono al programa quien a su vez es analizado por la librería reconocimiento de voz que sirve como una especie de filtro para interpretar el significado del comando en base a esto el programa tiene programado una serie de condicionales las cuales a su vez mediante pyserial emiten un mensaje al monitor serial de arduino quien finalmente al recibir el valor enviado por python mediante pyserial y lo que hace es que en base al valor recibido por el puerto serial realiza una determinada acción (mover mediante el servomotor(actuador) un determinado dedo o un conjunto de ellos).

Resumen de lo que ocurre:

microfono del computador (recibe datos) --> reconocimiento de voz (analiza el mensaje emitido por voz)-->pyserial(envia mediante monitor serie la instruccion a realizar)--> arduino (recibe el valor del monitor serie, la evalúa y ejecuta la instrucción correspondiente) Fin

Sugerencias que se podrían implementar:
-Podría en el código arduino podría aplicarse rutinas para controlar el giro, con la finalidad de ahorrar unas cuantas líneas de código
-De no querer depender de la computadora para que el brazo responda a los comandos de voz podría optarse por adquirir un sensor de reconocimiento de voz,
aunque debido al presupuesto con el que contaba no me pude dar el lujo de comprar ;)
