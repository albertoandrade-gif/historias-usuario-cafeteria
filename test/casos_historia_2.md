# Casos de prueba — Historia de usuario 2: Inicio de sesión

## TC-003 — Inicio de sesión con credenciales válidas

- **Tipo:** Positivo (flujo normal)
- **Objetivo:** Validar que un usuario registrado pueda autenticarse y acceder al menú principal.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - Existe una cuenta activa con las credenciales indicadas.
  - El usuario no ha iniciado sesión.
- **Datos de prueba:**

| Campo | Valor |
|---|---|
| Correo electrónico | cliente.registrado@example.com |
| Contraseña | CafeExpress#2026 |

- **Pasos:**
  1. Abrir la pantalla de inicio de sesión.
  2. Ingresar el correo electrónico registrado.
  3. Ingresar la contraseña válida.
  4. Presionar el botón **Iniciar sesión**.
  5. Navegar a otra sección disponible de la aplicación.
- **Resultado esperado:** El sistema autentica al usuario, lo dirige a la pantalla principal o menú y mantiene activa su sesión durante la navegación.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura del acceso al menú y, si aplica, log de autenticación._

---

## TC-004 — Rechazo de contraseña incorrecta

- **Tipo:** Negativo (flujo alterno)
- **Objetivo:** Validar que el sistema deniegue el acceso cuando la contraseña no corresponde al correo registrado.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - Existe una cuenta con el correo `cliente.registrado@example.com` y una contraseña diferente de la usada en la prueba.
  - El usuario no ha iniciado sesión.
- **Datos de prueba:**

| Campo | Valor |
|---|---|
| Correo electrónico | cliente.registrado@example.com |
| Contraseña inválida | ClaveIncorrecta#99 |

- **Pasos:**
  1. Abrir la pantalla de inicio de sesión.
  2. Ingresar el correo electrónico registrado.
  3. Ingresar la contraseña inválida.
  4. Presionar el botón **Iniciar sesión**.
  5. Revisar la respuesta del sistema.
- **Resultado esperado:** El sistema no inicia la sesión ni muestra contenido protegido; permanece en el formulario y presenta un mensaje de credenciales incorrectas sin revelar cuál dato falló.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura del mensaje de error y, si aplica, log del intento rechazado._
