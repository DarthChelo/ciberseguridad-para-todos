# 🏭 Cheat Sheet: Infraestructuras Críticas y Ciberataques a Nivel País

Este apunte corresponde al Capítulo 9 del curso "Ciberseguridad desde CERO". Aquí dejamos de lado la seguridad personal y empresarial para entender qué sucede cuando los ciberataques apuntan a los servicios vitales que mantienen funcionando a una nación.

## ⚙️ ¿Qué es una Infraestructura Crítica?

Son las instalaciones, sistemas y redes (físicas o virtuales) que proporcionan servicios absolutamente esenciales para el funcionamiento de un país, su economía y el bienestar de sus ciudadanos. 

**Ejemplos principales:**
*   Plantas de energía y redes eléctricas.
*   Sistemas de distribución y tratamiento de agua.
*   Hospitales y sistemas de salud pública.
*   Oleoductos y refinerías.
*   Sistemas de transporte (trenes, control de tráfico aéreo).

### El problema de la conectividad:
Históricamente, estos sistemas industriales (conocidos como **OT - Operational Technology**) estaban aislados (Air-gapped) y no conectados a internet. Hoy en día, para mejorar la eficiencia y el monitoreo remoto, se han conectado a las redes corporativas (IT) y a internet, exponiéndolos a los mismos ciberataques que sufre una computadora común.

---

## 🦠 Stuxnet: El arma cibernética que cambió la historia (2010)

Stuxnet no fue un virus para robar dinero; fue el primer ejemplo público de un **arma cibernética** diseñada para causar daño físico a instalaciones en el mundo real.

*   **El Objetivo:** El programa nuclear de Irán, específicamente las instalaciones de enriquecimiento de uranio en Natanz.
*   **¿Cómo funcionaba?** Stuxnet era un gusano extremadamente sofisticado (se cree que desarrollado por EE. UU. e Israel). Aprovechaba vulnerabilidades "Día Cero" (Zero-Day) en Windows para propagarse, pero su objetivo final eran los sistemas de control industrial (PLCs) de la marca Siemens.
*   **El Daño:** Una vez dentro del sistema industrial, Stuxnet alteraba silenciosamente la velocidad de las centrifugadoras nucleares, haciéndolas girar demasiado rápido hasta que se rompían físicamente, mientras le mostraba a los operadores en sus pantallas que todo funcionaba con normalidad.

**La Lección:** Demostró que un código informático podía destruir hardware militar e industrial sin disparar una sola bala.

---

## 🛢️ El Ataque a Colonial Pipeline: El caos por un Ransomware (2021)

Mientras que Stuxnet fue un sabotaje estatal, el incidente de Colonial Pipeline en EE. UU. demostró cómo el cibercrimen motivado por el dinero puede paralizar un país.

*   **¿Qué es Colonial Pipeline?** Es el oleoducto más grande de Estados Unidos, responsable de transportar casi la mitad del combustible consumido en la costa este.
*   **El Ataque:** El grupo criminal *DarkSide* logró infiltrarse en la red de la empresa (aparentemente a través de una antigua cuenta de VPN comprometida que no tenía doble factor de autenticación - 2FA). Desplegaron un **Ransomware** que cifró los sistemas informáticos de facturación e IT.
*   **El Impacto:** Aunque el ransomware afectó las computadoras de las oficinas (IT) y no directamente a las válvulas del oleoducto (OT), la empresa decidió apagar todo el oleoducto por precaución. Esto provocó escasez de gasolina, compras de pánico, filas kilométricas en las gasolineras y la declaración de estado de emergencia en varios estados.
*   **El Rescate:** La empresa pagó casi 5 millones de dólares en Bitcoin para recuperar sus sistemas (gran parte fue recuperado después por el FBI).

**La Lección:** La seguridad de la red corporativa (IT) está directamente ligada a la seguridad de la infraestructura crítica (OT). Un fallo básico (falta de 2FA) puede generar una crisis nacional.

---

## 🛡️ ¿Cómo se protegen estos sistemas?

Para defender las infraestructuras críticas, los gobiernos y empresas implementan estrategias estrictas:

*   **Segmentación de Red:** Separar completamente la red de las oficinas (donde los empleados leen correos) de la red industrial (donde se controlan las turbinas).
*   **Monitoreo de Anomalías OT:** Herramientas especializadas que analizan el tráfico industrial. Si una turbina que siempre gira a 500 RPM recibe una orden por red para girar a 5000 RPM, el sistema levanta una alerta.
*   **Sistemas redundantes (Backups físicos):** Capacidad para operar de forma manual, mediante válvulas mecánicas y procesos analógicos, en caso de que los sistemas digitales se vean comprometidos.

---
*Material educativo gratuito creado por Marcelo Bugallo (DarthChelo) - Tu Defensa Digital.*
