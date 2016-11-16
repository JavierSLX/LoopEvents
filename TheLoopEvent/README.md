#The loop Event

###Programacíon Síncrona vs Asíncrona
En cuestión de todo el video, se nos presenta como de manera general se trabaja de esta forma.  

El experto nos habla o más bien nos expone que *no es fácil* encontrarnos con este tipo de programación por primera vez, ver los beneficios de la asincronía en un servidor  y mas difícil es aun entender el funcionamiento interno que esta representa.

Comenzando con un aspecto importante, se nos  muestra la gran ventaja que representa la asincronía, "**mantener un flujo natural en el navegador**". No permitir bloqueos innecesarios de código (eventos lentos) y peor aun, acumulativos, en lugar de actuar de manera asíncrona pero en muchos casos mas rapida. 

Particularmente la presentación aborda una cuestión interesante, el reto de entender la asincronía surge al preguntarnos: cómo es que javascript maneja la asincronía por si solo, si realmente no lo hace.

El evento loop como ya lo menciona el titulo del video, es una manera de manejar las respuestas de la asincronía, si nuestro stack se encuentra vacío las funciones asincronas pueden ser procesadas por Javascript en orden desde el task queue, y no necesariamente de manera síncrona, dejando el stack libre para procesar código síncrono pero listo y delegando funciones a webapis, Aumentando así el flujo del navegador al no bloquear respuestas por esperar por algún bloque de código.

