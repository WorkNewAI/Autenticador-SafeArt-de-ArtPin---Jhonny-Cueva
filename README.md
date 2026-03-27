# 🛡️ SafeArt v3 — Autenticador de ArtPin

**SafeArt v3** es una plataforma avanzada de simulación de acceso seguro y gestión de identidades (IAM). El proyecto demuestra la implementación de múltiples capas de seguridad, desde el hashing de contraseñas en el cliente hasta mecanismos de respuesta ante incidentes en tiempo real.

## 👤 Autor
**Jhonny Rolando Cueva Alburqueque**
*Estudiante de  Sistemas de Información y Ciberseguridad*

---

## 🚀 Características Principales

### 1. Autenticación de Múltiples Factores (MFA)
El acceso no solo depende de una contraseña. SafeArt implementa un flujo de 4 pasos:
- **Paso 1:** Identidad (Usuario y Contraseña) con protección CAPTCHA.
- **Paso 2:** Código PIN de 4 dígitos.
- **Paso 3:** Pregunta de seguridad personalizada.
- **Paso 4:** **TOTP (Time-based One-Time Password)**: Un código dinámico que expira cada 30 segundos.

### 2. Seguridad Criptográfica
- **Hashing Robusto:** Utiliza el algoritmo **PBKDF2-SHA512** con 310,000 iteraciones.
- **Salt Único:** Cada usuario posee un *salt* aleatorio de 32 bytes para prevenir ataques de tablas arcoíris.
- **Zero-Knowledge (Simulado):** Las contraseñas en texto plano nunca se almacenan; solo se guardan los hashes resultantes.

### 3. Monitoreo SIEM en Tiempo Real
Incluye un panel de **Security Information and Event Management (SIEM)** que registra:
- Intentos de inicio de sesión (exitosos y fallidos).
- Bloqueos por *Rate Limiting*.
- Creación de usuarios y alertas de seguridad.
- Capacidad de exportar logs y base de datos a formato **JSON**.

### 4. Respuesta ante Incidentes (Alerta de Correo)
Al iniciar sesión, el sistema simula el envío de un correo de alerta. 
- Si el usuario marca **"No fui yo"**, el sistema bloquea la cuenta inmediatamente y fuerza un cambio de contraseña mediante un flujo de recuperación seguro.

---

## 🛠️ Tecnologías Utilizadas
- **Lenguaje:** HTML5 / CSS3 (Diseño moderno con Space Grotesk).
- **Lógica:** JavaScript (Vanilla JS).
- **Seguridad:** Web Crypto API para procesos de hashing y derivación de claves.
- **Almacenamiento:** LocalStorage para persistencia de la base de datos simulada.

## 📂 Instalación y Uso
1. Descarga el archivo `safeart_v8.html`.
2. Ábrelo en cualquier navegador moderno (Chrome, Firefox, Edge).
3. Utiliza las credenciales por defecto para pruebas:
   - **Usuario:** `Admin`
   - **Contraseña:** `P@ssword123`
   - **PIN:** `El que ponga en su smartphone (CELULAR) en mi caso fue 1996`
   - **Mascota:** `cerbero`
