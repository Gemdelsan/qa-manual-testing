# Plan de Pruebas - Módulo de Autenticación (Veterinaria DAW)

**Proyecto:** Veterinaria DAW (Aplicación ficticia de gestión veterinaria)[cite: 20, 31]  
**Módulo:** Registro e Inicio de Sesión de Usuarios[cite: 20, 31]  
**Autora:** Gema  
**Modalidad:** Ejercicio práctico de diseño de pruebas sobre requisitos funcionales (sin ejecución en entorno real)

---

## 1. Objetivo
Verificar que las funcionalidades de **registro de nuevos usuarios** e **inicio de sesión** cumplen con los requisitos funcionales y reglas de validación definidos, garantizando que únicamente los usuarios con datos válidos y credenciales autorizadas puedan crear cuentas y acceder al sistema[cite: 20, 31].

---

## 2. Alcance

### Dentro del alcance (In Scope)
* **Formulario de Registro:** Validación de campos obligatorios, formato de correo electrónico, longitud mínima de contraseña, coincidencia en la confirmación de clave y control de correos duplicados[cite: 31].
* **Formulario de Inicio de Sesión (Login):** Validación de campos obligatorios, acceso con credenciales registradas y rechazo de accesos con contraseñas erróneas o usuarios inexistentes[cite: 20].

### Fuera del alcance (Out of Scope)
* Recuperación o restablecimiento de contraseña olvidada.
* Pruebas no funcionales (rendimiento, carga, estrés o auditoría avanzada de seguridad)[cite: 8, 17].
* Pruebas automatizadas (reservadas para una fase posterior del proyecto)[cite: 6].

---

## 3. Requisitos Funcionales a Validar

### 3.1. Registro de Usuario
1. **Nombre:** Campo obligatorio[cite: 31].
2. **Correo electrónico:** Campo obligatorio y debe respetar un formato válido (`usuario@dominio.ext`)[cite: 31].
3. **Contraseña:** Campo obligatorio con una longitud mínima de **8 caracteres**[cite: 31].
4. **Confirmación de contraseña:** Debe coincidir exactamente con la contraseña introducida[cite: 31].
5. **Unicidad:** No se permite registrar dos cuentas con el mismo correo electrónico[cite: 31].

### 3.2. Inicio de Sesión (Login)
1. **Campos obligatorios:** Tanto el correo electrónico como la contraseña deben estar informados[cite: 20].
2. **Formato:** El correo electrónico debe tener un formato válido[cite: 20].
3. **Autenticación:** Si las credenciales son válidas y pertenecen a una cuenta activa, se permite el acceso al área privada[cite: 20, 27].
4. **Control de errores:** Si las credenciales son incorrectas o el usuario no existe, se deniega el acceso y se muestra un mensaje informativo[cite: 20].

---

## 4. Enfoque y Técnicas de Prueba
* **Pruebas Funcionales (Caja Negra):** Verificación del comportamiento del sistema a partir de entradas y salidas esperadas según los requisitos[cite: 8].
* **Pruebas Positivas y Negativas:** Comprobación tanto del flujo exitoso como del manejo de errores y datos inválidos[cite: 2].
* **Particiones de Equivalencia:** Agrupación de datos válidos e inválidos para optimizar la cobertura sin redundancias[cite: 28].
* **Análisis de Valores Límite (BVA):** Evaluación específica de las fronteras en la longitud de la contraseña (7 caracteres frente a 8 caracteres)[cite: 28].

---

## 5. Entorno y Modalidad de Ejecución
* **Estado del entorno:** Proyecto de aprendizaje basado en el análisis de requisitos simulados. No se ha ejecutado sobre una aplicación desplegada ni en navegadores reales.
* **Estado de los casos:** Todos los casos diseñados permanecen en estado `Not Run` (pendientes de ejecución)[cite: 27, 33].
* **Incidencias:** Los reportes de defectos incluidos (`BUG-001` y `BUG-002`) corresponden a escenarios simulados para practicar la documentación técnica y la clasificación de severidad y prioridad[cite: 28, 29].

---

## 6. Criterios de Entrada y Salida

### Criterios de Entrada (Entry Criteria)
* Requisitos funcionales de registro y login definidos y revisados[cite: 20, 31].
* Casos de prueba documentados y revisados antes de su ejecución[cite: 26].

### Criterios de Salida / Aceptación (Exit Criteria)
* Ejecución del 100 % de los casos de prueba planificados (`TC-REG-001` a `TC-REG-005` y `TC-LOG-001` a `TC-LOG-004`).
* Cero defectos abiertos de severidad **Crítica** o **Mayor** que comprometan la seguridad de acceso o impidan el alta de usuarios válidos.

---

## 7. Entregables del Proyecto
* `test-cases/register-test-cases.md`: Suite de 5 casos de prueba para el registro[cite: 33, 34, 35].
* `test-cases/login-test-cases.md`: Suite de 4 casos de prueba para el inicio de sesión.
* `bug-reports/bug-001.md` y `bug-002.md`: Ejemplos de informes de defectos simulados.
