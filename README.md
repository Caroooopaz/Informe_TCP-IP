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

