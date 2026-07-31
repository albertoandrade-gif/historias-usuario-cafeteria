# Casos de prueba — Historia de usuario 7: Historial de pedidos

## TC-013 — Consulta del historial con pedidos anteriores

- **Tipo:** Positivo (flujo normal)
- **Objetivo:** Validar que el usuario autenticado vea únicamente sus pedidos, con los datos requeridos y ordenados del más reciente al más antiguo.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario `cliente.registrado@example.com` ha iniciado sesión.
  - El usuario posee los tres pedidos indicados en los datos de prueba.
  - Existen pedidos de otros usuarios en el sistema.
- **Datos de prueba:**

| Número de orden | Fecha | Total | Estado |
|---|---|---:|---|
| ORD-0003 | 30/07/2026 | $10,50 | En preparación |
| ORD-0002 | 28/07/2026 | $7,00 | Entregado |
| ORD-0001 | 25/07/2026 | $4,50 | Entregado |

- **Pasos:**
  1. Iniciar sesión como `cliente.registrado@example.com`.
  2. Abrir la opción **Historial de pedidos**.
  3. Revisar los números de orden, fechas, totales y estados.
  4. Comprobar el orden cronológico de la lista.
  5. Verificar que no aparezcan órdenes de otros usuarios.
  6. Seleccionar la orden `ORD-0003`.
- **Resultado esperado:** El sistema muestra solo las tres órdenes del usuario, con todos sus datos, en el orden `ORD-0003`, `ORD-0002`, `ORD-0001`, y permite seleccionar una para consultar su detalle.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura completa del historial y de la selección de la orden._

---

## TC-014 — Historial de un usuario sin pedidos

- **Tipo:** Negativo (flujo alterno)
- **Objetivo:** Validar que el sistema maneje correctamente la ausencia de pedidos anteriores.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario `cliente.sin.pedidos@example.com` ha iniciado sesión.
  - La cuenta no posee órdenes registradas.
- **Datos de prueba:**

| Dato | Valor |
|---|---|
| Usuario | cliente.sin.pedidos@example.com |
| Cantidad de pedidos | 0 |

- **Pasos:**
  1. Iniciar sesión como `cliente.sin.pedidos@example.com`.
  2. Abrir la opción **Historial de pedidos**.
  3. Esperar a que finalice la carga.
  4. Revisar el contenido mostrado.
- **Resultado esperado:** El sistema presenta un mensaje informativo como “Aún no tienes pedidos”, no muestra errores técnicos ni órdenes pertenecientes a otros usuarios y mantiene la navegación disponible.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura del estado vacío y, si aplica, respuesta del servicio de historial._
