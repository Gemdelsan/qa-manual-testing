# Casos de Prueba - Inicio de Sesión (Login)

**Módulo:** Autenticación de usuarios (Veterinaria DAW)  
**Tipo de pruebas:** Funcionales (positivas, negativas y de validación)  
**Modalidad:** Diseño de casos de prueba sobre requisitos (sin ejecución en entorno real)

---

### TC-LOG-001: Inicio de sesión con credenciales válidas
* **Precondiciones:** Existe una cuenta previamente registrada y activa con el correo `maria@correo.com`.
* **Pasos:**
  1. Acceder a la pantalla de inicio de sesión (Login) de Veterinaria DAW.
  2. Introducir el correo electrónico registrado.
  3. Introducir la contraseña correcta.
  4. Pulsar el botón «Iniciar sesión».
* **Datos de prueba:**
  * Correo: `maria@correo.com`
  * Contraseña: `Password1234`
* **Resultado esperado:** El sistema valida las credenciales, permite el acceso al área privada y muestra el mensaje de bienvenida.
* **Resultado obtenido:** Pendiente de ejecución.
* **Estado:** Not Run

---

### TC-LOG-002: Inicio de sesión con contraseña incorrecta
* **Precondiciones:** Existe una cuenta previamente registrada y activa con el correo `maria@correo.com`.
* **Pasos:**
  1. Acceder a la pantalla de inicio de sesión (Login) de Veterinaria DAW.
  2. Introducir el correo electrónico registrado.
  3. Introducir una contraseña incorrecta.
  4. Pulsar el botón «Iniciar sesión».
* **Datos de prueba:**
  * Correo: `maria@correo.com`
  * Contraseña: `PasswordErroneo123`
* **Resultado esperado:** El sistema rechaza el acceso, mantiene al usuario en la pantalla de login y muestra el mensaje de error: «Credenciales incorrectas».
* **Resultado obtenido:** Pendiente de ejecución.
* **Estado:** Not Run

---

### TC-LOG-003: Inicio de sesión con correo electrónico no registrado
* **Precondiciones:** El correo `pablo@correo.com` no existe previamente en la base de datos del sistema.
* **Pasos:**
  1. Acceder a la pantalla de inicio de sesión (Login) de Veterinaria DAW.
  2. Introducir un correo electrónico no registrado.
  3. Introducir una contraseña cualquiera.
  4. Pulsar el botón «Iniciar sesión».
* **Datos de prueba:**
  * Correo: `pablo@correo.com`
  * Contraseña: `PasswordPablo1234`
* **Resultado esperado:** El sistema rechaza el acceso y muestra un mensaje de error indicando que las credenciales no son válidas o que el usuario no está registrado.
* **Resultado obtenido:** Pendiente de ejecución.
* **Estado:** Not Run

---

### TC-LOG-004: Intento de inicio de sesión con campos obligatorios vacíos
* **Precondiciones:** El usuario se encuentra en la pantalla de inicio de sesión de Veterinaria DAW.
* **Pasos:**
  1. Dejar vacío el campo del correo electrónico.
  2. Dejar vacío el campo de la contraseña.
  3. Pulsar el botón «Iniciar sesión».
* **Datos de prueba:**
  * Correo: *(vacío)*
  * Contraseña: *(vacío)*
* **Resultado esperado:** El sistema impide enviar el formulario, rechaza el acceso y muestra un mensaje de validación indicando que ambos campos son obligatorios.
* **Resultado obtenido:** Pendiente de ejecución.
* **Estado:** Not Run
