#Expressjs

##Web aplication framework  for node

Espress.js es un 
>"framework de desarrollo de aplicaciones web minimalista y flexible para Node.js"

Es robusto, rápido, flexible y muy simple. Entre otras características, ofrece Router de URL (Get, Post, Put …), facilidades para motores de plantillas (Jade, EJS, JinJS …)

Express.js está basado en Connect, que es un framework extensible de manejo de servidores HTTP, el cual provee plugins de alto rendimiento conocidos como middleware.

Middleware es un software que asiste a una aplicación para interactuar o comunicarse con otras aplicaciones, software, redes, hardware y/o sistemas operativos
______________________

Una aplicación escrita con express posee ciertos rasgos y cosas que no se pueden obviar, en app.js existe una estructura interna bien definida y es como sigue:

> app.js
var express = require('express')
 routes = require('./routes')
 var app = module.exports = express.createServer();

En esta primera parte se requieren los módulos o archivos externos necesarios para ejecutar la aplicación.
De igual forma, en esta parte se crea el servidor, mediante: express.createServer(), y es asignado a la variable app y de igual forma se “exporta” para que este disponible en caso de que sea necesario ejecutarla como secundario.

###Configuración  

La segunda parte y una muy importante es la configuración:

> app.configure(function(){
  app.set('views', __dirname + '/views');
  app.set('view engine', 'jade');
  app.use(express.bodyParser());
  app.use(express.methodOverride());
  app.use(app.router);
  app.use(express.static(__dirname + '/public'));
});

Es aqui donde se defines aspectos muy importantes para el funcionamiento correcto de nuestra aplicación, comumente conocido como middleware.
