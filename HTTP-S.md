# HTTP/S

El protocolo de transferencia de hipertexto seguro (HTTPS) es la versión segura de HTTP, que es protocolo principal utilizado para enviar datos entre un navegador web y un sitio web. el HTTPS esta encriptado para aumentar la seguridad de las transferencias de datos, fundamental para cuando lo usuarios transmiten datos confidenciales, tales como iniciar sesión es una cuenta bancaria, servicios de e-mail o proveedores de seguros médicos.

HTTPS utiliza un protocolo de encriptación para las comunicaciones, el cual se conoce como Transport Layer Security (TLS), anteriormente conocida como Secure Socket Layer (SSL), protocolo de seguridad de comunicaciones  mediante el uso de Infraestructura de Clave publica simertrica, esta se usa con dos claves diferentes para la encriptación de comunicaciones en dos partes.

1- Clave privada: Es la clave que controla el propietario de un sitio web y se mantiene; Esta clave esta ubicada en un servidor web y se utiliza para desencriptar la información encriptada por la clave pubica

2- Clave pública: Esta clave esta disponible para todos los que quieran interactuar con el servidor de forma segura. La información encriptada por la clave publica solo puede ser desencriptada por la clave privada


**Importancia de HTTPS**

Evita que los sitios web difundan la información que sea fácilmente visible para que este divulgado por la red, cuando a información se envía sobre HTTP normal, la información se divide en paquetes de datos que se pueden divulgar con el uso de software libre; Esto genera que la comunicación a través de un medio inseguro, como WI-FI publico sea muy vulnerable a la interceptación, todas las comunicaciones que se producen sobre HTTP ocurren en texto plano, lo cual genera que sean muy accesibles a cualquiera con las herramientas adecuadas y vulnerables a ataques en ruta

**Puerto que utiliza HTTPS**
HTTPS utiliza el puerto 443, esto distingue HTTPS de HTTP, el cual utiliza el puerto 80

**Diferencia HTTPS de HTTP**
HTTPS no es un protocolo distinto de HTTP, utiliza la encriptación TLS/SSL en el protocolo HTTP, mientras que HTTPS se basa en la transmisión de los datos Certificados TLS/SSL, que regula y verifica que un determinado proveedor es quien dice ser

Cuando un usuario se conecta a una pagina web, esta le envia su cetificado SSL, que contiene la clave publica necesaria para el inicio de sesión segura, luego los dos ordenadores, el cliente y el server, pasan por el proceso llamado protocolo de enlace SSL/TLS (serie de comunicaciones de ida y vuelta utilizadas para establecer conexiones seguras)

**Comienzo de utilización HTTPS en un sitio web**

Muchos proveedores de alojamiento de sitios web y otros servers ofrecen certificados TSL/SSL de pago, estos certificados suelen compartirse entre muchos clientes, ya que hay certificados mas caros que se pueden registrar individuamente para determinadas propiedades web

https://www.cloudflare.com/es-es/learning/ssl/what-is-https/
