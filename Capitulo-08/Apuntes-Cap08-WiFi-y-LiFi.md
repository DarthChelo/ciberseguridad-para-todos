# 📶 Cheat Sheet: Seguridad en Redes Inalámbricas (Wi-Fi y más allá)

Esta hoja de resumen cubre el Capítulo 8 del curso "Ciberseguridad desde CERO". A diferencia de un cable de red que puedes controlar físicamente, las redes inalámbricas transmiten datos por el aire en todas direcciones. Si no las protegemos correctamente, cualquiera en las cercanías podría "escuchar" lo que enviamos.

## 🔐 La Evolución de la Seguridad Wi-Fi (Protocolos)

A lo largo de los años, la forma de ponerle un "candado" a nuestro Wi-Fi ha ido evolucionando para tapar fallas de seguridad:

1.  **WEP (Wired Equivalent Privacy):** 
    *   *El Abuelo (1997):* Fue el primer intento de asegurar el Wi-Fi. 
    *   *Estado actual:* **Obsoleto y Peligroso**. Un atacante con herramientas gratuitas puede descifrar la contraseña de una red WEP en menos de 3 minutos. Si tu router aún lo usa, cámbialo de inmediato.
2.  **WPA y WPA2 (Wi-Fi Protected Access):**
    *   *El Estándar Actual:* WPA2 introdujo el cifrado AES (muy robusto). Es el candado que usa el 90% de los hogares hoy.
    *   *Vulnerabilidad:* Su punto débil eres tú. Si usas una contraseña fácil (ej. `marcelo123`), los atacantes pueden capturar el "saludo" de conexión (Handshake) y adivinar la contraseña offline mediante ataques de diccionario.
3.  **WPA3:**
    *   *El Nuevo Estándar:* Soluciona el problema de las contraseñas débiles de WPA2. Aunque elijas una mala clave, el sistema bloquea los intentos automáticos de adivinanza. Además, cifra tu conexión incluso en redes públicas abiertas.

---

## 🚀 El Futuro de la Conectividad

La tecnología inalámbrica está dando saltos gigantescos, tanto en velocidad como en seguridad física:

### Wi-Fi 7 (802.11be)
*   **¿Qué es?** La última generación del Wi-Fi. Su objetivo principal no es solo la velocidad, sino la **baja latencia** (reducir el tiempo de respuesta al mínimo) y la capacidad de manejar decenas de dispositivos exigentes a la vez.
*   **Innovación:** Usa una tecnología llamada MLO (Multi-Link Operation). Es como si tu celular, en lugar de conectarse al router por una sola autopista (banda de 5GHz), usara tres autopistas a la vez (2.4GHz, 5GHz y 6GHz) para que los datos nunca se atasquen.

### Li-Fi (Light Fidelity)
*   **¿Qué es?** En lugar de usar ondas de radio (como el Wi-Fi o Bluetooth), el Li-Fi utiliza **pulsos de luz LED** súper rápidos (invisibles al ojo humano) para transmitir internet a los dispositivos.
*   **Ventaja de Ciberseguridad 🛡️:** Las ondas de radio del Wi-Fi atraviesan paredes, permitiendo que un vecino intente hackearte. **La luz no atraviesa paredes.** Con Li-Fi, si cierras la puerta y bajas las persianas de tu habitación, es físicamente imposible que alguien desde afuera intercepte tu red. 

---

## 🛡️ Checklist: Cómo asegurar el Wi-Fi de tu casa o PyME

*   [ ] **Cambia la contraseña del administrador:** Nunca dejes las credenciales que vienen de fábrica para entrar a la configuración del router (ej. `admin/admin`).
*   [ ] **Desactiva el WPS:** Es el botoncito del router para conectarse sin clave. Tiene fallas de diseño graves y los atacantes pueden adivinar su PIN de 8 dígitos muy fácilmente.
*   [ ] **Usa seguridad WPA2 o WPA3:** Verifica en la configuración de tu router que estás usando el protocolo de seguridad más alto disponible, junto con una contraseña larga (mínimo 12-14 caracteres).
*   [ ] **Crea una Red de Invitados:** Si tienes visitas, dales acceso a la "Red de Invitados". Esta red les da internet, pero los aísla, impidiendo que vean tus dispositivos personales o infecten tu computadora si su celular tiene malware.

---
*Material de apoyo desarrollado por Marcelo Bugallo (DarthChelo) para la comunidad de Tu Defensa Digital.*
