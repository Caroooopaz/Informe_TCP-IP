# Informe_TCP-IP

Conceptos Básicos del Protocolo TCP/IP Este documento forma parte del módulo introductorio de redes en el bootcamp de desarrollo web. Estos son los fundamentos esenciales del protocolo TCP/IP, necesario para entender cómo viajan los datos por Internet y cómo funcionan los servicios web.

📚 Tabla de Contenidos 💡 ¿Qué es el protocolo TCP/IP y por qué es importante?

🤝 Modelo TCP/IP vs Modelo OSI

🏗️ Las 4 capas del modelo TCP/IP (de forma sencilla)

📡 Direccionamiento IP: IPv4 vs IPv6

🚪 Puertos y Protocolos Comunes para Desarrolladores Web

🔑 Protocolos clave en el día a día web

🔄 Proceso básico de conexión en la web

🔒 Seguridad y capa de transporte

🛠️ Herramientas básicas para ver el protocolo en acción

📖 Glosario esencial de términos

💡 ¿Qué es el protocolo TCP/IP y por qué es importante? El Protocolo de Control de Transmisión/Protocolo de Internet (TCP/IP) no es un protocolo único, sino un conjunto de protocolos de comunicación que permite a los dispositivos de una red comunicarse entre sí. Es, en esencia, el lenguaje fundamental que usa Internet para que los datos viajen de un punto a otro.
Breve historia y propósito Desarrollado en la década de 1970 por el Departamento de Defensa de los Estados Unidos, su propósito inicial era crear una red robusta y tolerante a fallos que pudiera funcionar incluso si partes de ella fueran destruidas. Con el tiempo, se convirtió en el estándar global para las comunicaciones de red, impulsando el crecimiento exponencial de Internet.

Su rol en el funcionamiento de Internet TCP/IP es la columna vertebral de Internet. Cada vez que envías un correo electrónico, visitas un sitio web, reproduces un video en streaming o realizas una videollamada, estás utilizando la suite de protocolos TCP/IP. Permite que la información se divida en pequeños paquetes, se envíe por diferentes rutas y se reensamble correctamente en su destino, garantizando la fiabilidad de la comunicación a escala global.

🤝 Modelo TCP/IP vs Modelo OSI Para entender cómo funcionan las redes, a menudo se utilizan modelos conceptuales. Los dos más conocidos son el Modelo TCP/IP y el Modelo OSI (Interconexión de Sistemas Abiertos).
Comparación de capas Mientras que el Modelo OSI tiene siete capas distintas, el Modelo TCP/IP simplifica esto en cuatro capas principales.

Cada capa del modelo TCP/IP tiene una responsabilidad específica en el proceso de comunicación. Piensa en ellas como diferentes departamentos en una empresa, cada uno con una tarea única pero interdependiente.

1. Capa de Acceso a Red
Esta es la capa inferior y se encarga de la interacción directa con el hardware de red. Define cómo los datos son enviados físicamente a través de un medio de red (cables, ondas de radio, etc.). Aquí es donde operan estándares como Ethernet y Wi-Fi. También incluye los drivers de la tarjeta de red que permiten al sistema operativo comunicarse con el hardware.

2. Capa de Internet
También conocida como Capa de Red. Su función principal es el enrutamiento de paquetes de datos a través de diferentes redes. Aquí es donde el Protocolo de Internet (IP) es fundamental. Define cómo se direccionan los paquetes y cómo se enrutan de un origen a un destino, utilizando las direcciones IP de los dispositivos. Los enrutadores operan en esta capa para dirigir el tráfico.

3. Capa de Transporte
Esta capa es responsable de la comunicación de extremo a extremo entre procesos que se ejecutan en diferentes hosts. Sus dos protocolos principales son TCP (Transmission Control Protocol) y UDP (User Datagram Protocol). TCP proporciona una comunicación fiable y ordenada (como para la navegación web), mientras que UDP ofrece una comunicación más rápida pero sin garantías de entrega (como para el streaming de video).

4. Capa de Aplicación
Esta es la capa más cercana al usuario. Aquí residen los protocolos que las aplicaciones utilizan para comunicarse a través de la red. Cuando abres un navegador web, envías un correo electrónico o resuelves un nombre de dominio, la Capa de Aplicación entra en juego con protocolos como HTTP, HTTPS, DNS, FTP, y SMTP.

¿Por qué usamos TCP/IP en la web? Aunque el modelo OSI es una excelente herramienta conceptual y pedagógica, el modelo TCP/IP es el que se implementa y utiliza en la práctica en Internet. Su diseño es más robusto y flexible para las complejidades del enrutamiento de paquetes a través de diversas redes interconectadas, lo que lo hace ideal para la infraestructura de la web.

## 3. 🏗️ Las 4 capas del modelo TCP/IP (de forma sencilla)

El modelo TCP/IP está compuesto por cuatro capas fundamentales, cada una con una responsabilidad específica en el proceso de comunicación. Piensa en ellas como diferentes departamentos en una empresa, cada uno con una tarea única pero interdependiente.

### Capa de Aplicación (HTTP, HTTPS, DNS, etc.)

Esta es la capa más cercana al usuario. Aquí residen los protocolos que las aplicaciones utilizan para comunicarse a través de la red. Cuando abres un navegador web, usas un cliente de correo electrónico o te conectas a una base de datos, la capa de Aplicación entra en juego.

**Protocolos principales:**
- **HTTP (Hypertext Transfer Protocol)**: El protocolo para la World Wide Web, utilizado para solicitar y enviar páginas web.
- **HTTPS (Hypertext Transfer Protocol Secure)**: La versión segura de HTTP, que cifra la comunicación.
- **DNS (Domain Name System)**: Traduce nombres de dominio legibles por humanos (ej. google.com) a direcciones IP numéricas.
- **FTP (File Transfer Protocol)**: Para la transferencia de archivos.
- **SMTP (Simple Mail Transfer Protocol)**: Para el envío de correos electrónicos.

### Capa de Transporte (TCP vs UDP)

Esta capa es responsable de la comunicación de extremo a extremo entre procesos que se ejecutan en diferentes hosts. Sus dos protocolos principales son TCP y UDP.

**TCP (Transmission Control Protocol):**
- Proporciona una comunicación fiable, ordenada y con control de errores
- Es "orientado a la conexión" porque establece una conexión antes de enviar datos
- Asegura que todos los datos lleguen correctamente
- Ideal para aplicaciones donde la integridad de los datos es crucial (ej. navegación web, transferencia de archivos)

**UDP (User Datagram Protocol):**
- Ofrece una comunicación más rápida pero "sin conexión" y sin garantías de entrega
- No verifica si los paquetes llegan ni en qué orden
- Ideal para aplicaciones donde la velocidad es más importante que la fiabilidad (ej. streaming de video, juegos en línea, llamadas VoIP)

### Capa de Internet (IP, direcciones IP, routing)

También conocida como Capa de Red. Su función principal es el enrutamiento de paquetes de datos a través de diferentes redes. Aquí es donde el Protocolo de Internet (IP) es fundamental.

**Componentes clave:**
- **IP (Internet Protocol)**: Define cómo se direccionan los paquetes y cómo se enrutan de un origen a un destino. Cada dispositivo conectado a Internet necesita una dirección IP única.
- **Direcciones IP**: Identificadores numéricos únicos asignados a cada dispositivo en una red. Permiten que los paquetes sepan a dónde ir.
- **Routing (Enrutamiento)**: El proceso de determinar la mejor ruta para que un paquete de datos viaje de un origen a un destino a través de una o más redes. Los enrutadores son los dispositivos clave en esta capa.

### Capa de Acceso a Red (Ethernet, Wi-Fi)

Esta es la capa inferior y se encarga de la interacción directa con el hardware de red. Define cómo los datos son enviados físicamente a través de un medio de red (cables, ondas de radio, etc.).

**Tecnologías principales:**
- **Ethernet**: El estándar más común para redes de área local (LAN) cableadas
- **Wi-Fi (IEEE 802.11)**: El estándar para redes inalámbricas
- **Drivers de tarjeta de red**: El software que permite que el sistema operativo se comunique con la tarjeta de red (NIC)

## 4. 📡 Direccionamiento IP: IPv4 vs IPv6

Las direcciones IP son esenciales para que los dispositivos se encuentren en Internet. Sin ellas, sería imposible enviar información a la máquina correcta.

### ¿Qué es una dirección IP?

Una dirección IP es una etiqueta numérica única asignada a cada dispositivo (computadora, servidor, impresora, teléfono móvil, etc.) que participa en una red informática que utiliza el Protocolo de Internet para la comunicación. Su función principal es identificar un dispositivo y su ubicación en la red.

### Estructura Básica de una IP

Existen dos versiones principales de direcciones IP:

#### IPv4 (Internet Protocol version 4)
- La versión original y más común
- Las direcciones IPv4 son números de 32 bits
- Generalmente representados en notación decimal con puntos (ej. 192.168.1.1)
- Permite aproximadamente 4.3 mil millones de direcciones únicas

#### IPv6 (Internet Protocol version 6)
- La versión más reciente, diseñada para reemplazar a IPv4 debido al agotamiento de direcciones
- Las direcciones IPv6 son números de 128 bits
- Representadas en formato hexadecimal con dos puntos (ej. 2001:0db8:85a3:0000:0000:8a2e:0370:7334)
- Proporciona un número casi ilimitado de direcciones (aproximadamente 3.4×10³⁸)

### Diferencia entre IP Pública y Privada

#### IP Pública
- Es una dirección IP única y globalmente enrutable en Internet
- Los servidores web, servicios en la nube y tu enrutador doméstico (que representa tu red ante Internet) tienen una IP pública
- Es la dirección que ven los demás dispositivos en Internet cuando te conectas

#### IP Privada
- Son direcciones reservadas para uso dentro de redes locales (LANs), como tu red doméstica u oficina
- No son enrutables en Internet
- Los dispositivos dentro de tu red local (tu computadora, teléfono, impresora) tendrán IPs privadas:
  - 192.168.x.x
  - 10.x.x.x
  - 172.16.x.x a 172.31.x.x
- Tu enrutador utiliza NAT (Network Address Translation) para permitir que múltiples dispositivos con IPs privadas compartan una única IP pública para acceder a Internet
