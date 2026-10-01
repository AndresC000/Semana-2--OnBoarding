## NSG - Network Security Group 

Servicio de Azure que actúa como firewall de red y permite el control de trafico entrante (Inbound) y saliente (Outbound) de los recursos de Azure.

**Reglas de seguridad**
Dentro de un grupo de seguridad de rede se deben de contener reglas de seguridad de red según sean necesarias, dentro de los limites de Azure, cada regla especifica las siguientes propiedades.

-**NOMBRE:**
Un nombre único dentro del grupo de seguridad de red, el nombre puede tener hasta 80 caracteres, este debe de comenzar con un carácter de palabra y terminar con un carácter de palabra o con (_).
Este nombre puede  contener caracteres de palabra (.,-,\_)

-**PROPIEDAD:**
Un numero entre 100 y 4096, las reglas se procesan en orden de prioridad con números mas bajos procesados antes de números mas altos ya que lo números mas bajos tienen mayor prioridad, cuando el trafico coincide con un regla, el procesamiento se detiene, por lo que las reglas con prioridad mas baja (números mas altos ) que tienen los mismos atributos con prioridades altas no se procesan
 **Las reglas predeterminadas de Azure reciben las prioridades mas bajas para asegurar que las reglas personalizadas siempre se procesen primero.

-**Origen o Destino:**

NSG es el filtrado de trafico de AZ, con una función similar a una ACL o firewall básico de red, permitiendo o denegando comunicaciones según origen, destino, puerto, protocolo y prioridad de la regla 

-**PROTOCOLO**
TCP, UDP, ICMP, ESP, AH o cualquiera, los protocolos ESP y AH no se encuentran disponibles actualmente en Azure Porta pero se pueden integrar mediante plantillas de ARM.

-**DIRECCION**
Si la regla se aplica al trafico entrante o saliente 

-**Intervalo de puertos**
Se puede especificar un puerto individual o intervalos de puertos, estos podrían especificar 80,  10000-10005, o para una combinación de puertos e intervalos individuales se pueden separar por comas (80,  10000-10005); Especificar intervalos y separación de comas permite crear menos reglas de seguridad.

Las reglas de seguridad aumentadas solo se pueden generar en los grupos de seguridad de red creados mediante el modelo de implantación de Resource Manager, No puede especificar múltiples puertos o intervalos de puertos en la misma regla de seguridad dentro de los grupos de seguridad de red creados mediante el modelo de implementación clásica.

-**ACCION**
Permite o deniega el trafico especificado

Las reglas de seguridad se evalúan y aplican en función del quinteto de origen, puerto origen, destino, puerto destino y protocolo; No puede crear dos reglas de seguridad con la misma prioridad y dirección, si se realiza esta puede generar conflicto en la forma en la forma en que el sistema procesa el trafico,  Se crea un registro de flujo para las conexiones existentes, esta permite o deniega la comunicación en función de estado de conexión del registro de flujo.
El registro de flujo permite que un grupo de seguridad de red sea con estado.

Si se quita una regla de seguridad que permita una conexión, las conexiones existentes permaneces interrumpidas, las reglas de grupo de seguridad de red solo afectan a las nuevas conexiones, las reglas nuevas o actualizadas de un grupo de seguridad de red se aplican exclusivamente a las nuevas conexiones, lo que deja las conexiones existentes no afectadas por los cambios.

**REGLAS DE SEGURIDAD AUMENTADA**
Simplifican la definición de seguridad de las redes virtuales, lo que permite definir directivas de seguridad de red mas grandes y complejas con menos reglas. Puede combinar varios puertos y varias direcciones IP explicitas e intervalos en una única regla e seguridad de fácil comprensión.
Hay limites para el numero de direcciones, intervalos y puertos que puede especificar en una regla de seguridad.

**Etiqueta de servicio**

Representa un grupo de prefijos de direcciones IP de un servicio de Azure determinado, el cual ayuda a minimizar la complejidad de las actualizaciones frecuentes en las reglas de seguridad de red.

**Grupos de seguridad de aplicaciones**
Permiten la configuración de seguridad en la red como una extensión natural de la estructura de una aplicación, lo cual permite agrupar MV y directivas de seguridad de red basadas en esos grupos; Estos pueden reutilizar la directica de seguridad a escala sin un mantenimiento manual de direcciones IP explicitas.

**Reglas de Administrador de seguridad**

Reglas de seguridad de red globales las cuales se aplican directivas de seguridad en redes virtuales, las reglas de administración de seguridad se originan en Azure Virtual Network Manager, un servicio de administración que permite a los administradores de red agrupar, configurar, implementar y administrar redes virtuales globalmente entre suscripciones.

Las reglas de administración de seguridad siempre tienen una prioridad mas alta que las reglas del grupo de seguridad de red, por tanto se evalúan primero; las reglas de administración de seguridad (PERMITIR),(PERMITIR SIEMPRE),(DENEGAR),(ALWAYS ALLOW) Y (DENEGAR).

https://learn.microsoft.com/es-es/azure/virtual-network/network-security-groups-overview#security-rules
