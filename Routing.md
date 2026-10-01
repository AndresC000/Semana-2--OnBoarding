## ROUTING

El enrutamiento de redes es el proceso de selección de una ruta a través de una o mas redes, Los principios del enrutamiento se aplica a cualquier tipo de red, en las redes de conmutación de paquetes, como internet, el enrutamiento selecciona las rutas para que los paquetes de LAS IP  vayan desde su origen hasta su destino estas decisiones de enrutamiento en internet las llevan a cabo piezas especializadas desde hardware de red conocidas como enrutadores

**Como funciona el enrutamiento**
Los enrutadores consultan las tablas de enrutamiento internas para tomar decisiones acerca de como enrutar los paquetes por las rutas de red , la tabla de enrutamiento registran las rutas que deben tomar los paquetes para llegar a cada destino del que sea responsable el enrutador.

Las tablas de enrutamiento pueden ser estáticas o dinámicas, las estáticas no cambian, un admin de red configura manualmente las tablas de enrutamiento estáticas (fija las rutas que toman los paquetes de datos a través de la red, a menos que el admin actualice manualmente las tablas).

Las tablas de enrutamiento dinámico se actualizan automáticamente, los enrutadores dinámicos utilizan varios protocolos de enrutamiento para determinar las rutas mas cortas y rápidas, también se toma en cuenta el tiempo que tardan en llegar a su destino.

El enrutamiento dinámico requiere mas potencia informática, por lo que las redes mas pequeñas pueden confiar en el enrutamiento estático, pero para las redes medianas o grandes el enrutamiento dinámico es mucho mas eficaz

**Principales Protocolo de enrutamiento**

Un protocolo de enrutamiento es un protocolo utilizado para identificar o anunciar rutas de red

-**IP:**
Protocolo de Internet Especifica el origen y el destino de cada paquete de datos; Los enrutadores inspeccionan el encabezado IP de cada paquete para identificar a dónde enviarlos

-**BGP: Border Gateway Protocol**
Se utiliza para anunciar que rede controlan que direcciones IP, y que redes se conectan entre si, BGP es un protocolo de enrutamiento dinámico.

-**OSPF: Open Shortest Path Fisrt**
Lo suelen utilizar los enrutadores de red que identifican las rutas mas rápidas  cortas disponible para enviar el paquete a su destino

-**RIP: Protocolo de información de enrutamiento**

Es el "recuento de saltos" para encontrar el camino mas corto de una red a otra,(el recuento de saltos significa el numero de enrutadores por los que debe pasar un paquete en el camino - cuando un paquete va de red a otra se le llama "salto")

**Enrutador**
Pieza de hardware de red responsable de reenviar los paquetes a sus destinos, los enrutadores conectan dos o mas redes o subredes IP, y pasan paquetes de datos entre ellas según sea necesario, los enrutadores se utilizan en casa y oficinas para el establecimiento de conexiones en redes locales, los enrutadores mas potentes funcionan por todo internet, ayudando a que los paquetes de datos lleguen a sus destinos

https://www.cloudflare.com/es-es/learning/network-layer/what-is-routing/
