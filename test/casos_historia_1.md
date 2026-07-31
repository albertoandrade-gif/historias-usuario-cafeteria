# Casos de prueba — Historia de usuario 1: Registro de usuario

## TC-001 — Registro exitoso de usuario

- **Tipo:** Positivo (flujo normal)
- **Objetivo:** Validar que un cliente nuevo pueda crear una cuenta con datos válidos y quede habilitado para iniciar sesión.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario no ha iniciado sesión.
  - El correo `cliente.nuevo@example.com` no está registrado.
- **Datos de prueba:**

| Campo | Valor |
|---|---|
| Nombre | Cliente Prueba |
| Correo electrónico | cliente.nuevo@example.com |
| Contraseña | CafeExpress#2026 |

- **Pasos:**
  1. Abrir la aplicación Café Express.
  2. Seleccionar la opción **Registrarse**.
  3. Ingresar el nombre, correo electrónico y contraseña indicados.
  4. Presionar el botón **Crear cuenta**.
  5. Cerrar la sesión o regresar a la pantalla de inicio de sesión.
  6. Iniciar sesión con el correo y la contraseña registrados.
- **Resultado esperado:** El sistema crea una sola cuenta, muestra un mensaje de registro exitoso y permite iniciar sesión con las nuevas credenciales.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura del mensaje de confirmación y, si aplica, registro o log de la prueba._

---

## TC-002 — Rechazo de correo ya registrado

- **Tipo:** Negativo (flujo alterno)
- **Objetivo:** Validar que el sistema impida crear una segunda cuenta con un correo electrónico existente.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - Existe una cuenta registrada con el correo `cliente.registrado@example.com`.
  - El usuario no ha iniciado sesión.
- **Datos de prueba:**

| Campo | Valor |
|---|---|
| Nombre | Otro Cliente |
| Correo electrónico | cliente.registrado@example.com |
| Contraseña | NuevaClave#2026 |

- **Pasos:**
  1. Abrir la aplicación Café Express.
  2. Seleccionar la opción **Registrarse**.
  3. Ingresar los datos de prueba.
  4. Presionar el botón **Crear cuenta**.
  5. Revisar el mensaje presentado por el sistema.
- **Resultado esperado:** El sistema no crea una cuenta duplicada, conserva al usuario en el formulario y muestra un mensaje claro indicando que el correo ya se encuentra registrado.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura del mensaje de error y, si aplica, evidencia de que no se creó un registro adicional._
