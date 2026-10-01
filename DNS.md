## DNS (DOMAIN NAME SYSTEM)

Son los directorios telefónicos de internet, donde las personas pueden acceder a a información en línea a través de nombre de domino como (Google.com), los navegadores web tienen que interactuar mediante las direcciones IP; El DNS traduce los nombres de dominio a direcciones IP, esto para que los navegadores puedan cargar los recursos de internet.

Cada dispositivo conectado a internet tiene una dirección IP única la cual otros equipos pueden usar para encontrarlos, los servers DNS eliminan la necesidad de memorizar las direcciones IP, cómo en IPv4-IPv6

## Servidores DNS implicados en la carga de un sitio web:

-**Recursor de DNS**
Servidor diseñado para recibir consultas desde equipos cliente mediante aplicaciones como navegadores web, el recursor será el responsable de realizar las solicitudes adicionales para satisfacer la consulta de DNS del cliente.
-**Servidor de nombre de raíz**
Primera acción para la traducción de los nombres de servidor legibles en direcciones IP, Generalmente sirven como referencia de otras ubicaciones más especificas.
-**Servidor de nombres TLD**
Siguiente paso en la búsqueda de direcciones IP especificas, las cuales alojan a ultima parte de un nombre de servidor (ejemplo Google.com- TLD es "com").
-**Servidor de nombres autoritativo**
Es el ultimo punto en la consulta del servidor de nombres, si se cuenta con acceso al registro solicitado, nos devolverá la dirección IP del nombre del servidor solicitado al recursor de DNS que hizo la solicitud inicial.

##DNS AUTORITATIVO - DNS RECURSICO
Ambos son servers (grupo de servers), los cuales son fundamentales para la infraestructura de DNS, pero cada desempeña un papel diferente las cuales se encuentran en diferentes ubicaciones dentro del trayecto de una consulta de DNS.
	-DNS RECURSIVO -INICIAL
	-DNS AUTORITATICO -FINAL

**Solucionador de DNS recursivo**
Equipo que responde a una solicitud recursiva del cliente, la cual dedica tiempo a detectar el registro de DNS, la cual se realiza mediante una serie de solicitudes hasta que alcanza al servidor de nombres DNS autoritativo, para el registro solicitado (vuelve inactivo o devuelve error si no encuentra ningún error); No siempre tienen que hacer varias solicitudes para inspeccionar los registros necesarios para responder al cliente, eso nos da el **Almacenamiento en caché**, el cual es un proceso de persistencia de datos que nos ayudan a saltarse las solicitudes necesarias sirviendo ante el registro del recurso solicitado en la búsqueda DNS.
 
**Servidor DNS autoritativo**
Es un servidor que alberga realmente registros de recursos DNS y es responsable de los mismos, es el servidor final de la cadena de búsqueda DNS la cual responderá con el registro del recurso consultado, esto  nos permite que e navegador web haga solicitud para llegar a la  dirección IP necesaria para poder acceder al sitió web o a los recursos web, estos servers pueden satisfacer solicitudes de sus propios datos sin necesidad de consultar a otros recursos, ya que esta es la fuente final para ciertos registros de DNS

##Solucionador de DNS
Es la primera parada en las búsquedas de DNS, la cual se encarga de tratar con el cliente que hizo la solicitud inicial; El solucionador inicia la secuencia de consultas que llevan en ultima instancia a que la URL se traduzca a la IP necesaria

**Tipos de Consulta de DNS**
Al usar una combinación de consulta, se crea un proceso optimizado para la solución de DNS la cual puede llevar una reducción de la distancia recorrida, en una situación ideal, los datos de registro almacenados en la memoria cache estarán disponibles, lo cual generara que un server de nombres DNS devuelvan una consulta no recursiva

1- Consulta recursiva: Un cliente DNS requiere que un servidor DNS (generalmente un solucionador de DNS recursivo) responda al cliente con el registro del  recurso solicitado o un  mensaje de error si el solucionador no puede encontrar el registro

2- Consulta Iterativa: el cliente DNS requiere que un servidor DNS devuelva la mejor respuesta posible, si el servidor DNS consultado no cuenta con un nombre que corresponda con el de la consulta, devolverá una referencia a un servidor DNS autoritativo para un nivel inferior del espacio de nombres del dominio. Este proceso continuara con servidores DNS adicionales que siguen en la cadena de consulta hasta que se produzca un error o se supere el tiempo de espera.

3. Consulta NO Recursiva: Se producen cuando un cliente solucionador de DNS consulta a un servidor DNS por un registro al que tiene acceso ya que es autoritario para el registro o e registro existe dentro de su caché, generalmente, el servidor DNS almacenara en caché registros DNS para prevenir el consumo de ancho de banda adicional y la carga en los servers que preceden en la cadena

## DNS público - DNS privado

-**DNS público**
Es un servicio abierto que cualquier persona puede utilizar, gestionado por proveedores externos como Google o Cloudflare, la cual ofrece una Infra robusta y conocida por su velocidad y fiabilidad

-**DNS Privado**
Es un servicio cerrado que se utiliza dentro de una red corporativa o domestica, la cual nos permite un mayor control y personalización, la cual nos proporciona seguridad adicional al reducir la exposición a terceros filtrando sitios maliciosos

https://www.cloudflare.com/es-es/learning/dns/what-is-dns/

https://www.palotintonetworks.com/blog-user-protect/que-es-un-dns-privado-seguridad-navegacion-empresas/

