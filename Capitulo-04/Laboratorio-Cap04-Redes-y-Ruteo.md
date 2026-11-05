# 🔬 Laboratorio: Explorando la Red (Ping, Traceroute y DNS)

Bienvenido al laboratorio del Capítulo 4 del curso "Ciberseguridad desde CERO". En esta práctica, dejaremos la teoría de lado y utilizaremos herramientas reales de diagnóstico de red integradas en tu sistema operativo.

**Objetivo:** Comprender cómo viaja la información por Internet, cómo los nombres (ej. google.com) se traducen a direcciones IP, y cómo medir la latencia y los saltos de conexión.

---

## 🛠️ Preparación: Abriendo la Terminal (Línea de Comandos)

Antes de empezar, necesitamos abrir nuestra herramienta de trabajo:

*   **En Windows:** Presiona la tecla `Windows`, escribe `cmd` y presiona Enter para abrir el "Símbolo del sistema".
*   **En macOS:** Presiona `Comando (⌘) + Espacio`, escribe `Terminal` y presiona Enter.
*   **En Linux:** Presiona `Ctrl + Alt + T`.

---

## 🟢 Ejercicio 1: `ping` (Comprobando la conectividad y latencia)

El comando `ping` envía un pequeño paquete de datos a un destino y espera una respuesta (como el sonar de un submarino). Sirve para saber si un servidor está vivo y cuánto tarda la respuesta (latencia).

1. En tu terminal, escribe el siguiente comando y presiona Enter:
   ```bash
   ping 1.1.1.1
