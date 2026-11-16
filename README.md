# 🧪 QA Manual Testing — Veterinaria DAW

Repositorio de prácticas de **Aseguramiento de la Calidad (QA Manual)** enfocado en el análisis de requisitos, diseño de pruebas funcionales y documentación técnica de incidencias.

> **Nota sobre el alcance del proyecto:** Este repositorio corresponde a un ejercicio práctico de aprendizaje basado en los requisitos funcionales simulados de una aplicación ficticia (*Veterinaria DAW*). Las pruebas no han sido ejecutadas sobre una aplicación desplegada en un entorno real; los casos de prueba se presentan en estado `Not Run` y los informes de defectos corresponden a escenarios simulados para demostrar criterio técnico y estándar de documentación.

---

## 📂 Estructura del Repositorio

    qa-manual-testing/
    ├── README.md
    ├── test-plans/
    │   └── authentication-test-plan.md
    ├── test-cases/
    │   ├── register-test-cases.md
    │   └── login-test-cases.md
    └── bug-reports/
        ├── bug-001.md
        └── bug-002.md

---

## 📋 Contenido y Entregables

### 1. Planificación de Pruebas
* **[Plan de Pruebas de Autenticación](test-plans/authentication-test-plan.md):** Define el objetivo, alcance (*In Scope / Out of Scope*), requisitos funcionales a validar, estrategia de pruebas y criterios de entrada y salida.

### 2. Diseño de Casos de Prueba (9 Test Cases)
* **[Casos de Prueba de Registro](test-cases/register-test-cases.md)** (`TC-REG-001` a `TC-REG-005`):
  * Validación de campos obligatorios y formato de correo electrónico.
  * Comprobación de coincidencia en la confirmación de contraseña.
  * Control de unicidad (correo electrónico ya registrado).
  * Pruebas de longitud mínima de contraseña aplicando análisis de valores límite (7 y 8 caracteres).
* **[Casos de Prueba de Inicio de Sesión](test-cases/login-test-cases.md)** (`TC-LOG-001` a `TC-LOG-004`):
  * Flujo positivo con credenciales válidas.
  * Pruebas negativas con contraseña incorrecta y usuario no registrado.
  * Validación de envío con campos obligatorios vacíos.

### 3. Gestión de Defectos Simulados (Bug Reports)
* **[BUG-001](bug-reports/bug-001.md):** *El formulario de registro rechaza contraseñas válidas de 8 caracteres* (Defecto funcional de validación en el límite inferior — Severidad Mayor / Prioridad Alta).
* **[BUG-002](bug-reports/bug-002.md):** *El sistema permite iniciar sesión a un usuario existente con una contraseña incorrecta* (Brecha crítica de seguridad en autenticación — Severidad Crítica / Prioridad Máxima).

---

## 🛠️ Metodología y Técnicas Aplicadas

* **Pruebas de Caja Negra (Black-Box Testing):** Diseño basado estrictamente en los requisitos funcionales y reglas de negocio.
* **Cobertura Positiva y Negativa:** Verificación tanto del camino feliz (*Happy Path*) como del manejo controlado de errores.
* **Particiones de Equivalencia:** Agrupación de datos de entrada válidos e inválidos para evitar redundancias.
* **Análisis de Valores Límite (BVA):** Evaluación de las fronteras críticas de validación (ej. contraseñas de 7 frente a 8 caracteres).
* **Documentación Estándar de Incidencias:** Redacción de pasos reproducibles, aislamiento de variables y diferenciación entre **Severidad** (impacto técnico) y **Prioridad** (urgencia de negocio).

---

## 👩‍💻 Autora

**Gema** — Desarrolladora de Aplicaciones Web (DAW) enfocada en Quality Assurance (QA) y Software Testing.
