# 🔐 Cheat Sheet: Criptografía, Hashes y Pagos Digitales Seguros

Esta hoja de resumen cubre los Capítulos 2 y 3 del curso "Ciberseguridad desde CERO". Aquí desmitificamos cómo viaja segura nuestra información por internet y cómo el sector financiero protege nuestro dinero usando matemáticas.

## 🔏 Criptografía: El arte de ocultar información

La criptografía transforma texto legible (texto plano) en un formato incomprensible (texto cifrado) para que solo las personas con la "llave" correcta puedan leerlo. Garantiza la **Confidencialidad**.

Existen dos tipos principales:

### 1. Cifrado Simétrico (La misma llave)
*   **¿Cómo funciona?** Usas la *misma llave* para cifrar (cerrar) y descifrar (abrir) el mensaje.
*   **Ventaja:** Es rapidísimo.
*   **Desventaja:** Si le tienes que enviar la llave a otra persona por internet y alguien la intercepta, podrá leer todo.
*   **Uso común:** Cifrar el disco duro de tu computadora (BitLocker, FileVault) o un archivo ZIP con contraseña.

### 2. Cifrado Asimétrico (Dos llaves distintas)
*   **¿Cómo funciona?** Tienes un par de llaves matemáticas conectadas entre sí:
    *   **Llave Pública:** La compartes con todo el mundo. Sirve para que otros *cifren* un mensaje dirigido a ti.
    *   **Llave Privada:** La guardas en secreto. Es la *única* que puede *descifrar* lo que se cerró con la pública.
*   **Uso común:** El protocolo HTTPS (el "candadito" del navegador) y los certificados digitales.

---

## 🧬 Hashes: La Huella Dactilar Digital

Un **Hash** es una función matemática de "un solo sentido" (no reversible). Toma cualquier cantidad de datos (una palabra o un video de 10GB) y la convierte en una cadena de texto de longitud fija. Garantiza la **Integridad**.

### Características de un Hash:
*   **Efecto avalancha:** Si cambias una sola coma en un documento de 1000 páginas, el Hash resultante será completamente distinto.
*   **Unidireccional:** No puedes tomar un Hash y "descomprimirlo" para ver el archivo original.

### ¿Para qué se usa en la vida real?
1.  **Guardar Contraseñas:** Las páginas web seguras NO guardan tu contraseña real en sus bases de datos; guardan el *Hash* de tu contraseña. Si un hacker roba la base de datos, solo verá letras y números sin sentido.
2.  **Verificar Archivos:** Para comprobar que el programa que descargaste no fue modificado por un virus en el camino.

---

## 💳 Pagos Digitales y Tokenización

Cuando compras por internet o usas tu celular en un comercio, transmitir tu número de tarjeta de crédito real (PAN) de extremo a extremo es muy riesgoso. Aquí entra la **Tokenización**.

### ¿Qué es la Tokenización?
Es el proceso de sustituir los datos sensibles de tu tarjeta bancaria por un código equivalente no sensible llamado **Token**. 

*   **¿Cómo funciona?** En lugar de enviar los 16 dígitos de tu tarjeta por la red, tu celular (Apple Pay, Google Pay) o tu tarjeta virtual envía un *Token* temporal o de uso limitado al comercio.
*   **¿Por qué es seguro?** Si un ciberdelincuente intercepta ese Token en la red del comercio, **no le sirve para nada**. Ese código solo tiene valor para esa transacción específica o en ese comercio particular, y no puede ser usado para clonar tu tarjeta física.

### 💡 Buenas prácticas para pagos seguros:
*   [ ] Usa **Billeteras Digitales** (Apple Pay, Google Pay) o tecnología **Contactless (NFC)** en lugar de insertar el chip o deslizar la banda magnética, ya que aprovechan la tokenización.
*   [ ] Genera **Tarjetas Virtuales** desechables en la app de tu banco para compras en sitios web que no conoces.
*   [ ] Nunca envíes fotos del frente y dorso de tu tarjeta por WhatsApp o correo electrónico.

---
*Material de apoyo desarrollado por Marcelo Bugallo (DarthChelo) para la comunidad de Tu Defensa Digital.*
