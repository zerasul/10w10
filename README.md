# Internet Of Everything W10
============================

Proyecto presentado en el hackaton 10w10 celebrado el día 8 de Julio en Almería y Organizado por el [Club .NET de Almería](https://twitter.com/dotnetalmeria). Este proyecto trata de aplicar a la nueva tecnología de Universal Windows Platform a "el Internet del Todo". En este caso se trata de un dispositivo por el cual podemos comprobar y actuar sobre distintos sensores y/o actuadores que utilizaremos para comunicarnos con el mundo. Gracias a la tecnología UWP de Microsoft, podremos controlar todo esto a traves de todos los dispositivos que integren Windows 10. Como puede ser nuestro ordenador de sobremesa, portatil, tablet, phone y incluso nuestra Xbox One.

![10w10](http://i.imgur.com/gRFSQOg.png)

Como podemos ver en el esquema, tenemos que nuestro sistema se compone de las siguientes partes:
* la primera parte se compone de distintos sensores y actuadores, como puede ser un sensor de humedad, sensor de temperatura y un actuador de Infrarojos con el que podemos por ejemplo encender el aire acondiconado. Todos estos sensores estan conectados a una placa Arduino(incluso puede ser una placa INtel Galileo) que realizará las medidas y las enviara por medio de un puerto Serie(en este caso USB) a una Raspberry Pi 2.
* La siguiente parte es una Raspberry Pi 2 con Windows 10 IOT core instalado; utilizando un programa realizado con .NET recogeremos los datos que el arduino nos envia y seremos capaz de comunicarnos con este.
* Por último tenemos una aplicación realizada con UWP(Universal Windows Platform) que es capaz de ejecutarse en distintos sistemas. Como por ejemplo una Xbox One y poder saber la temperatura y humedad de casa y poder activar el aire acondicionado por medio del actuador de Infrarojos. La comunicación de los dispositivos con Windows 10 y la Raspberry Pi 2 se realiza por medio de una llamada http.

En breve dejaremos el código de cada una de las partes del sistema.
