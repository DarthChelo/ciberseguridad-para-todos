# 🧱 Cheat Sheet: Defensa Digital, Firewalls y Honeypots

Esta hoja de resumen corresponde al Capítulo 7 del curso "Ciberseguridad desde CERO". Aquí exploramos cómo construimos las barreras de protección de una red y cómo usamos el engaño para atrapar a los atacantes.

## 🏰 Defensa en Profundidad (Defense in Depth)

En ciberseguridad no existe la herramienta mágica o la "bala de plata" que frene todos los ataques. La **Defensa en Profundidad** es una estrategia basada en el modelo de un castillo medieval: si el atacante logra cruzar el foso, todavía tiene que enfrentarse a la muralla, y si pasa la muralla, lo esperan los guardias en la torre.

*   **Regla principal:** Se usan múltiples capas de seguridad superpuestas (antivirus + firewall + contraseñas fuertes + educación del usuario). Si una capa falla, la siguiente detiene el ataque.

---

## 🔥 Firewalls (Cortafuegos): Los Guardias de la Red

Un **Firewall** es un sistema (puede ser hardware físico o software) que se coloca entre tu red privada y el internet público. Su trabajo es analizar todo el tráfico que intenta entrar o salir y decidir qué pasa y qué se bloquea.

### ¿Cómo toma decisiones un Firewall?
Trabaja basándose en **Reglas de Acceso** (Políticas). Por defecto, la regla más segura y utilizada en la industria es el **"Deny All" (Denegar Todo)**:
*   *Todo lo que no esté explícitamente permitido en una regla, queda automáticamente bloqueado.*

### Tipos de filtrado comunes:
1.  **Por Dirección IP:** "Permitir que la IP de la oficina se conecte al servidor de la base de datos, pero bloquear a cualquier otra IP del mundo."
2.  **Por Puertos (Servicios):** "Permitir tráfico por el Puerto 443 (Navegación web segura HTTPS), pero bloquear el Puerto 23 (Telnet, que es inseguro)."
3.  **Filtrado de Aplicaciones (Next-Gen Firewalls):** Identifican qué programa estás usando. "Permitir el uso de Facebook para leer noticias, pero bloquear el chat o los juegos dentro de Facebook."

---

## 🚨 IDS vs. IPS (Sistemas de Intrusos)

A veces, el tráfico parece legítimo (ej. una conexión web por el puerto 443 permitido por el Firewall), pero el contenido de esa conexión esconde un ataque. Aquí entran los analistas de tráfico:

*   **IDS (Sistema de Detección de Intrusos):** Es como una alarma de humo. Si ve algo sospechoso o un patrón de ataque conocido en la red, grita y avisa a los administradores, pero **no detiene el ataque**.
*   **IPS (Sistema de Prevención de Intrusos):** Es como un sistema de rociadores automáticos. Si detecta un ataque, no solo avisa, sino que corta inmediatamente la conexión para **bloquear la amenaza** en tiempo real.

---

## 🍯 Honeypots (Trampas de Miel)

En lugar de solo defendernos, a veces queremos que el atacante revele sus cartas. Un **Honeypot** es un sistema falso, intencionalmente vulnerable, diseñado para atraer a los ciberdelincuentes.

### ¿Cómo funciona la trampa?
Los administradores colocan un servidor en la red que parece contener información valiosa (ej. "BaseDeDatos_Tarjetas_Clientes"), pero en realidad es un señuelo completamente aislado de los datos reales de la empresa.

### ¿Para qué se utilizan?
1.  **Alerta Temprana:** Como ningún empleado legítimo debería intentar acceder a ese servidor falso, si la alarma del Honeypot suena, sabemos al 100% que hay un intruso en la red.
2.  **Inteligencia (Threat Intel):** Permite estudiar cómo actúan los atacantes, qué herramientas usan y qué contraseñas intentan probar, sin poner en riesgo la infraestructura real.
3.  **Pérdida de Tiempo:** Mantiene al atacante distraído intentando vulnerar un sistema que no sirve para nada, dándole tiempo al equipo de seguridad para reaccionar.

---
*Material educativo gratuito creado por Marcelo Bugallo (DarthChelo) - Tu Defensa Digital.*
