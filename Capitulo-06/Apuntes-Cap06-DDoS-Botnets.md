# 🛑 Cheat Sheet: Ataques DDoS, Botnets y Saturación de Servicios

En este resumen del curso "Ciberseguridad desde CERO", abordamos cómo los ciberdelincuentes logran "tirar abajo" páginas web, videojuegos y servicios enteros, y cómo reclutan ejércitos de dispositivos para lograrlo.

## 🚦 DoS vs. DDoS: El embotellamiento digital

Para entender estos ataques, imagina un servidor web como si fuera la puerta de un supermercado. Tiene una capacidad máxima de personas que pueden entrar por minuto.

*   **DoS (Denial of Service - Denegación de Servicio):** 
    *   Ocurre cuando *un solo atacante* envía demasiadas peticiones al servidor al mismo tiempo, bloqueando la puerta. 
    *   *Solución fácil:* El guardia (Firewall) identifica a esa única persona molesta y le bloquea la entrada.
*   **DDoS (Distributed Denial of Service - Denegación de Servicio Distribuida):** 
    *   Ocurre cuando *miles o millones* de atacantes (ubicados en todo el mundo) intentan entrar al supermercado exactamente al mismo segundo. 
    *   *El problema:* La puerta se bloquea para los clientes legítimos. Como el ataque viene de todas partes, el guardia no puede simplemente bloquear a una persona; no puede distinguir quién es cliente y quién es atacante.

---

## 🧟‍♂️ Botnets: El "Ejército Zombi"

¿De dónde saca un atacante miles de computadoras para lanzar un ataque DDoS? No las compra; las secuestra. A esto se le llama **Botnet** (Red de Robots).

1.  **Infección:** Un usuario descarga malware (ej. por Phishing) o un dispositivo tiene contraseñas débiles por defecto (muy común en cámaras de seguridad o Smart TVs).
2.  **Conversión a Zombi (Bot):** El dispositivo se infecta de forma silenciosa. Sigue funcionando normalmente, por lo que el dueño no nota nada raro.
3.  **Control (C&C):** El dispositivo infectado se conecta a un servidor de Comando y Control manejado por el atacante (el "Botmaster").
4.  **El Ataque:** El atacante presiona un botón y ordena a los millones de dispositivos zombis que visiten una misma página web al mismo tiempo. ¡Boom! Servicio caído.

💡 *Dato clave:* Gran parte de los ataques DDoS actuales no provienen de computadoras tradicionales, sino de dispositivos **IoT** (Internet de las Cosas) mal configurados, como routers domésticos, luces inteligentes o cámaras IP.

---

## 💥 ¿Cómo se saturan exactamente los servicios?

Los servidores tienen recursos limitados (Procesador, Memoria RAM y Ancho de banda). Los ataques buscan agotar uno de esos tres:

*   **Ataques Volumétricos:** El objetivo es saturar el "tubo" de internet. Envían tanta basura que el ancho de banda del servidor se llena y no queda espacio para el tráfico real (como intentar meter un millón de litros de agua por una manguera de jardín).
*   **Ataques de Aplicación (Capa 7):** Son más silenciosos. Hacen que el servidor trabaje demasiado. Por ejemplo, en lugar de enviar basura, envían miles de peticiones de búsqueda complejas a la base de datos de la página. El procesador (CPU) del servidor llega al 100% y colapsa.

---

## 🛡️ Motivos y Defensas

### ¿Por qué lo hacen?
*   **Extorsión:** "Págame en criptomonedas o mantendré tu tienda online caída durante el Black Friday".
*   **Hacktivismo:** Tirar abajo la web de un gobierno o empresa por motivos políticos o de protesta.
*   **Competencia desleal:** Bloquear los servidores del videojuego rival en el día de su lanzamiento.

### ¿Cómo nos defendemos?
Las empresas hoy en día no pueden defenderse solas de ataques tan masivos. Necesitan "escudos" gigantes:
*   **CDNs (Redes de Distribución de Contenido) y WAFs:** Empresas como *Cloudflare* o *Akamai* se ponen delante del servidor de la víctima. Absorben todo el impacto del tráfico malicioso (gracias a sus enormes anchos de banda a nivel global) y solo dejan pasar a los usuarios legítimos.
*   **Anycast:** Una técnica de red que dispersa el tráfico del ataque a través de múltiples centros de datos alrededor del mundo, diluyendo su fuerza.

---
*Material educativo gratuito creado por Marcelo Bugallo (DarthChelo) - Tu Defensa Digital.*
