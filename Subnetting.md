## ¿Qué es Subnetting?
El subnetting (o subdivisión de redes) es la práctica de dividir una red IP física o lógica en dos o más subredes  más pequeñas. Este proceso se logra modificando la **máscara de subred**, la cual determina qué parte de una dirección IP identifica a la red y qué parte a los hosts.


**Optimización del tráfico y rendimiento:** Reduce el tamaño de los dominios de difusión, evitando el colapso por tráfico innecesario en la red.* 
**Seguridad mejorada:** Permite aislar segmentos de red (por ejemplo, separar el tráfico de servidores, empleados y visitantes) mediante listas de acceso (ACLs) o firewalls entre subredes. **Gestión eficiente de direcciones:** Evita el desperdicio de direcciones IP ajustando el tamaño de cada subred al número exacto o proyectado de dispositivos necesarios.

## Tipos de Subnetting
**FLSM (*Fixed Length Subnet Mask*):** Todas las subredes creadas tienen exactamente el mismo tamaño y la misma máscara de subred, independientemente de la cantidad de hosts que requiera cada una. Es más fácil de configurar, pero puede generar desperdicio de IP.
**VLSM (*Variable Length Subnet Mask*):** Permite asignar máscaras de subred de diferente longitud según las necesidades específicas de cada subred. Optimiza al máximo el direccionamiento IP y es la norma en redes modernas.
## Componentes Clave de una Subred

Para cualquier dirección IP y máscara de subred (por ejemplo, 192.168.1.0/24):
**Dirección de Red:** Primera IP del rango; identifica la subred completa (no asignable a hosts).
**Dirección de Broadcast:** Última IP del rango; se utiliza para enviar paquetes a todos los hosts de la subred.
**Rango de Host Usables:** Direcciones IP entre la de red y la de broadcast que se pueden asignar a dispositivos (2^h - 2, donde h es el número de bits de host).

**Información obtenida desde mi cuenta personal/escolar de Cisco Networking Academy**
