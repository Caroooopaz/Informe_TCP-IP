# Informe_TCP-IP


Conceptos Básicos del Protocolo TCP/IP
Este documento forma parte del módulo introductorio de redes en el bootcamp de desarrollo web. Estos son los fundamentos esenciales del protocolo TCP/IP, necesario para entender cómo viajan los datos por Internet y cómo funcionan los servicios web.

📚 Tabla de Contenidos
💡 ¿Qué es el protocolo TCP/IP y por qué es importante?

🤝 Modelo TCP/IP vs Modelo OSI

🏗️ Las 4 capas del modelo TCP/IP (de forma sencilla)

📡 Direccionamiento IP: IPv4 vs IPv6

🚪 Puertos y Protocolos Comunes para Desarrolladores Web

🔑 Protocolos clave en el día a día web

🔄 Proceso básico de conexión en la web

🔒 Seguridad y capa de transporte

🛠️ Herramientas básicas para ver el protocolo en acción

📖 Glosario esencial de términos

1. 💡 ¿Qué es el protocolo TCP/IP y por qué es importante?
El Protocolo de Control de Transmisión/Protocolo de Internet (TCP/IP) no es un protocolo único, sino un conjunto de protocolos de comunicación que permite a los dispositivos de una red comunicarse entre sí. Es, en esencia, el lenguaje fundamental que usa Internet para que los datos viajen de un punto a otro.

Breve historia y propósito
Desarrollado en la década de 1970 por el Departamento de Defensa de los Estados Unidos, su propósito inicial era crear una red robusta y tolerante a fallos que pudiera funcionar incluso si partes de ella fueran destruidas. Con el tiempo, se convirtió en el estándar global para las comunicaciones de red, impulsando el crecimiento exponencial de Internet.

Su rol en el funcionamiento de Internet
TCP/IP es la columna vertebral de Internet. Cada vez que envías un correo electrónico, visitas un sitio web, reproduces un video en streaming o realizas una videollamada, estás utilizando la suite de protocolos TCP/IP. Permite que la información se divida en pequeños paquetes, se envíe por diferentes rutas y se reensamble correctamente en su destino, garantizando la fiabilidad de la comunicación a escala global.

2. 🤝 Modelo TCP/IP vs Modelo OSI
Para entender cómo funcionan las redes, a menudo se utilizan modelos conceptuales. Los dos más conocidos son el Modelo TCP/IP y el Modelo OSI (Interconexión de Sistemas Abiertos).

Comparación de capas
Mientras que el Modelo OSI tiene siete capas distintas, el Modelo TCP/IP simplifica esto en cuatro capas principales.

Capa del Modelo OSI

Capa del Modelo TCP/IP

Descripción Simplificada

7. Aplicación

4. Aplicación

Proporciona servicios de red a las aplicaciones de usuario.

6. Presentación

(No tiene equivalente directo)

Gestiona la representación de los datos (ej. cifrado/descifrado).

5. Sesión

(No tiene equivalente directo)

Establece, gestiona y finaliza las sesiones de comunicación.

4. Transporte

3. Transporte

Asegura la entrega de datos de extremo a extremo.

3. Red

2. Internet

Direccionamiento y enrutamiento de paquetes.

2. Enlace de Datos

1. Acceso a Red

Transfiere datos entre nodos adyacentes.

1. Física

1. Acceso a Red

Define las especificaciones eléctricas y mecánicas del medio.


Exportar a Hojas de cálculo
¿Por qué usamos TCP/IP en la web?
Aunque el modelo OSI es una excelente herramienta conceptual y pedagógica, el modelo TCP/IP es el que se implementa y utiliza en la práctica en Internet. Su diseño es más robusto y flexible para las complejidades del enrutamiento de paquetes a través de diversas redes interconectadas, lo que lo hace ideal para la infraestructura de la web.
