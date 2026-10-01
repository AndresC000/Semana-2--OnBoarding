# TCP/IP

Divide la información en paquetes, las cuales se envían de manera independiente las cuales se reconstruyen en el destino para formas el mensaje completo, esto permite que las comunicaciones sean fiables y eficientes, esto porque cad paquete llegase a tomar rutas diferentes, este protocolo **TCP**, asegura su llegada de forma ordenada y sin errores, además esta incluye modos de seguridad y autenticación.

## CAPAS DE MODELO TCP/IP

-**Capa de acceso al medio(enlace)**
Traduce la transmisión dentro de la red local y traduce las Ip´s a MAC

-**Capa de Internet**
Enrutamiento de los paquetes entre redes diferentes usando direcciones IP

-**Capa de transporte**
Asegura la entrega confiable de los datos, controla errores y el orden de los paquetes -- TCP

-**Capa de aplicación**
Proporciona servicios a las apps, incluyendo protocolos como:
	-**HTTP**
	-**FTP**
	-**SMTP**
	-**DHCP**
La cual nos permite la comunicación entre programas y usuarios.

TCP/IP es necesario para la interoperabilidad entre sistemas heterogéneos, la cual nos permite que los Host se comuniquen sin conflictos, asegurando su función confiable y segura.

##Diferencia entre el modelo TCP/IP y el Modelo OSI

Son dos formas distintas de describir como se comunican los sistemas en red; Mientras que TCP/IP se centra en los protocolos reales y en como funciona internet, OSI es mas teórico y detallado.

##Como configurar TCP/IP en Windows y Linux

-Windows, la configuración básica de TCP/IP se realiza desde las propiedades del adaptador de la red, desde donde se definen direcciones IP, mascaras, puertas de enlace y servers DNS
-Linux, Estos parámetros con recurrencia se gestionan mediante archivos de configuración o herramientas especificas de cada distro.

https://www.soloingenieria.org/ingenieria-informatica/tcp-ip/

