# 🌐 Apuntes: Redes, Protocolos y el Viaje de los Datos

Este documento teórico acompaña al Capítulo 4 de "Ciberseguridad desde CERO". Antes de usar herramientas de diagnóstico, es vital entender cómo se comunican las computadoras a través de Internet.

## 📦 Direcciones IP y Puertos (El Edificio y el Departamento)

Para que dos computadoras se hablen, necesitan saber dónde están. 
*   **Dirección IP:** Es como la dirección de un edificio (ej. `190.210.45.12`). Identifica a tu router en internet.
*   **Puertos Lógicos:** Son como los números de los departamentos dentro de ese edificio. Hay 65,535 puertos disponibles.
    *   *Ejemplo:* Cuando navegas por una web segura, te conectas a la IP del servidor en el **Puerto 443** (HTTPS). Si envías un correo, usas el **Puerto 25** (SMTP).

## 🚦 TCP vs. UDP: ¿Cómo viaja la información?

Existen dos formas principales en las que los datos viajan por los puertos:

1.  **TCP (Transmission Control Protocol): El mensajero con acuse de recibo.**
    *   Garantiza que los datos lleguen completos y en orden. Si un paquete de datos se pierde, TCP lo vuelve a pedir.
    *   *Uso:* Páginas web, correos electrónicos, transferencias de archivos. (Prefiere la **seguridad y fiabilidad**).
2.  **UDP (User Datagram Protocol): El mensajero a toda velocidad.**
    *   Envía los datos lo más rápido posible sin importarle si llegan todos. No hay confirmación de entrega.
    *   *Uso:* Videojuegos online, llamadas de Zoom, streaming en vivo. (Prefiere la **velocidad**; si pierdes un fotograma en un video, simplemente sigues viendo el siguiente).

## 📇 DNS (Domain Name System): La Guía Telefónica

Los humanos somos malos recordando números (IPs), pero buenos recordando nombres (`tudefensadigital.com`). 
*   El **DNS** es una red de servidores mundiales que traduce ese nombre en la IP correcta para que tu computadora sepa a dónde conectarse.
*   **Riesgo de Seguridad (DNS Spoofing):** Los atacantes pueden envenenar esta guía telefónica. Si tu equipo es vulnerado, al escribir el nombre de tu banco, el DNS modificado te redirigirá a la IP del servidor del atacante (una web clonada).

## 🔍 Herramientas de Diagnóstico (Repaso)
*   **Ping:** Utiliza el protocolo ICMP (Internet Control Message Protocol) para enviar un "eco" y medir el tiempo de respuesta. Si el servidor responde, sabemos que hay conectividad.
*   **Traceroute:** Muestra cada router (salto) por el que pasa tu paquete de datos hasta llegar a su destino, revelando la ruta física de la información.
