
## SSH
El protocolo Secure Shell, es un método para enviar comandos de forma segura a un ordenador mediante una red no segura. SSH utiliza criptografía para autenticar y encriptar las conexiones entre dispositivos, también permite la tunelización o redireccionamiento de puertos, que es cuando los paquetes pueden cruzar las redes de otro modo no podrían cruzar, SSH se utiliza a menudo para controlar los servidores a distancia, para la gestión de infraestructuras y transferencia de archivos

**Función de SSH**
Se ejecuta sobre el conjunto de protocolo TCP/IP.
TCP/IP transporta y entrega paquetes de datos. El uso de TCP es una de las diferencias entre SSH y otros protocolos de tunelización, algunos de los cuales utilizan UDP, que es mas rápido pero menos fiable.

**Criptografía en clave publica.**
SSH es "seguro" por su incorporación con encriptación y autenticación; La criptografía de clave publica es una forma de encriptación de datos,  firmar los datos, con las dos claves diferentes.
-La clave publica esta disponible para que cualquiera pueda usarla
-La clave privada la mantiene el propietario secreto.
Las dos claves se relacionan entre si, para establecer la identidad del propietario de la clave es necesario la posesión de ambas claves

Claves "asimétricas"- llamadas así porque tienen valores diferentes, realizan que ambos lados de la conexión negocien claves simétricas idénticas y compartidas para su posterior encriptación a través del canal. Una vez que se finaliza la negociación, las dos partes utilizan las claves simétricas para la encriptación de los datos a intercambiar.
Esto da la diferencia al SSH de HTTPS, que en la mayoría de las implementaciones solo verifica la identidad del servidor web en una conexión cliente-servidor.
	-HTTPS no permite al cliente acceder a la línea de comando del servidor 
	-Los firewalls a veces bloquean SSH, pero casi nunca HTTPS

**AUTENTICACION**

La criptografía de clave publica autentica los dispositivos conectados en SSH, un ordenador debidamente protegido seguirá requiriendo la autenticación de la persona que utiliza el SSH, esto adopta la forma de introducir un nombre de usuario y una contraseña

**Reenvió de puertos SSH o "tunelización**
El reenvió de puertos envía paquetes de datos dirigidos a una dirección IP y a un puerto de maquina a una dirección IP y a un puerto de maquina diferente

**SSH en S.O**
En S.O  Linux y Mac vienen con el SSH incorporado. Las maquinas Windows pueden requerir que se tenga instalada una app de cliente SSH. En Mac y Linux, los usuarios pueden abrir la Terminal e introducir directamente los comandos SSH

**Funciones para SSH**
Puede transmitir cualquier dato arbitrario a través de una red y la tunelización SSH puede configurarse para una infinidad de propósitos, los usos mas comunes de SSH son:

	-Gestión a distancia a servidores, infraestructura y ordenadores de empleados
	-Transferencia de archivos de forma segura (Mas seguro que un protocolo no encriptado como FTP)
	-Acceso a los servicios en la nube sin expones los puertos de una maquina local a internet
	-Conexiones remotas a los servicios de una red privada
	-Evitar restricciones firewalls

**Puerto a SSH**
El puerto 22 es el puerto por defecto para SSH, aun que en ocasiones los firewalls, puede bloquear el acceso a determinados puertos en los servidores detrás del firewall, pero deja abierto el puerto 22, por lo que SSH es útil para acceder a los servidores al otro lado de los firewalls, los paquetes dirigidos al puerto 22 no se bloquean y pueden reenviare a cualquier otro puerto.

**Riesgos asociados a SSH**
SSH suele ir acompañado de privilegios elevados, como la capacidad de instalar apps, en un servidor o eliminar, así como la alteración o extracción de datos.
SSH también pueden atravesar firewalls que dejar desbloqueado el puerto 22, lo que permite a los atacantes a entrar en redes seguras.

https://www.cloudflare.com/es-es/learning/access-management/what-is-ssh/
