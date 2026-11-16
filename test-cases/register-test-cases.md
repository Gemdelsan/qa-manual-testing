# Casos de Prueba - Registro de Usuarios

**Módulo:** Autenticación de usuarios (Veterinaria DAW)  
**Tipo de pruebas:** Funcionales (positivas, negativas, particiones de equivalencia y valores límite)  
**Modalidad:** Diseño de casos de prueba sobre requisitos (sin ejecución en entorno real)

---

### TC-REG-001: Intentar registrarse con un correo electrónico inválido
* **Precondiciones:** El usuario no está registrado previamente en el sistema[cite: 33].
* **Pasos:**
  1. Acceder al formulario de registro de Veterinaria DAW[cite: 33].
  2. Introducir un nombre válido[cite: 33].
  3. Introducir un correo electrónico con formato incorrecto[cite: 33].
  4. Introducir una contraseña válida[cite: 33].
  5. Repetir la contraseña correctamente en el campo de confirmación[cite: 33].
  6. Pulsar el botón «Registrarse»[cite: 33].
* **Datos de prueba:**
  * Nombre: `María`[cite: 33]
  * Correo: `maria@correo`[cite: 33]
  * Contraseña: `Prueba123`[cite: 33]
  * Confirmación: `Prueba123`[cite: 33]
* **Resultado esperado:** El sistema muestra un mensaje indicando que el correo electrónico no tiene un formato válido y no permite completar el registro[cite: 33].
* **Resultado obtenido:** Pendiente de ejecución[cite: 33].
* **Estado:** Not Run[cite: 33]

---

### TC-REG-002: Intentar registrarse cuando la confirmación de contraseña no coincide
* **Precondiciones:** El usuario no está registrado previamente en el sistema[cite: 34].
* **Pasos:**
  1. Acceder al formulario de registro de Veterinaria DAW[cite: 34].
  2. Introducir un nombre válido[cite: 34].
  3. Introducir un correo electrónico válido[cite: 34].
  4. Introducir una contraseña válida[cite: 34].
  5. Introducir una confirmación de contraseña diferente a la contraseña original[cite: 35].
  6. Pulsar el botón «Registrarse»[cite: 34].
* **Datos de prueba:**
  * Nombre: `María`[cite: 34]
  * Correo: `maria@correo.com`[cite: 34]
  * Contraseña: `Prueba123`[cite: 34]
  * Confirmación: `Prueba124`[cite: 34]
* **Resultado esperado:** El sistema muestra un mensaje indicando que las contraseñas no coinciden, impide completar el registro y no crea la cuenta del usuario[cite: 35].
* **Resultado obtenido:** Pendiente de ejecución[cite: 34].
* **Estado:** Not Run[cite: 34]

---

### TC-REG-003: Intentar registrarse con un correo electrónico que ya existe
* **Precondiciones:** Existe en la base de datos una cuenta activa registrada previamente con el correo `maria@correo.com`[cite: 35].
* **Pasos:**
  1. Acceder al formulario de registro de Veterinaria DAW.
  2. Introducir un nombre válido.
  3. Introducir el correo electrónico registrado con anterioridad.
  4. Introducir una contraseña válida.
  5. Repetir la contraseña válida en el campo de confirmación.
  6. Pulsar el botón «Registrarse».
* **Datos de prueba:**
  * Nombre: `María`
  * Correo: `maria@correo.com`
  * Contraseña: `Prueba123`
  * Confirmación: `Prueba123`
* **Resultado esperado:** El sistema muestra un mensaje indicando que el correo electrónico ya está registrado y no permite crear una cuenta duplicada.
* **Resultado obtenido:** Pendiente de ejecución.
* **Estado:** Not Run

---

### TC-REG-004: Intentar registro con contraseña de 7 caracteres (valor límite no válido)
* **Precondiciones:** El usuario no está registrado previamente en el sistema[cite: 28].
* **Pasos:**
  1. Acceder al formulario de registro de Veterinaria DAW.
  2. Introducir un nombre válido.
  3. Introducir un correo electrónico válido.
  4. Introducir una contraseña de exactamente 7 caracteres[cite: 28].
  5. Repetir la contraseña en el campo de confirmación.
  6. Pulsar el botón «Registrarse».
* **Datos de prueba:**
  * Nombre: `María`
  * Correo: `maria@correo.com`
  * Contraseña: `Prueba1`
  * Confirmación: `Prueba1`
* **Resultado esperado:** El sistema muestra un mensaje indicando que la contraseña debe tener al menos 8 caracteres y no permite completar el registro[cite: 28, 31].
* **Resultado obtenido:** Pendiente de ejecución.
* **Estado:** Not Run

---

### TC-REG-005: Registro exitoso con contraseña de 8 caracteres (valor límite válido)
* **Precondiciones:** El usuario no está registrado previamente en el sistema[cite: 28].
* **Pasos:**
  1. Acceder al formulario de registro de Veterinaria DAW.
  2. Introducir un nombre válido.
  3. Introducir un correo electrónico válido.
  4. Introducir una contraseña de exactamente 8 caracteres[cite: 28].
  5. Repetir la contraseña en el campo de confirmación.
  6. Pulsar el botón «Registrarse».
* **Datos de prueba:**
  * Nombre: `María`
  * Correo: `maria@correo.com`
  * Contraseña: `Prueba12`
  * Confirmación: `Prueba12`
* **Resultado esperado:** El sistema valida los datos correctamente, crea la cuenta y muestra la confirmación de registro exitoso[cite: 28].
* **Resultado obtenido:** Pendiente de ejecución.
* **Estado:** Not Run
