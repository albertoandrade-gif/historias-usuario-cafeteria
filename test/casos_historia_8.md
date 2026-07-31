# Casos de prueba — Historia de usuario 8: Consultar detalle de pedido

## TC-015 — Visualización del detalle de una orden propia

- **Tipo:** Positivo (flujo normal)
- **Objetivo:** Validar que el cliente pueda consultar todos los datos de una orden propia y regresar al historial.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario `cliente.registrado@example.com` ha iniciado sesión.
  - La orden `ORD-0003` pertenece al usuario y aparece en su historial.
- **Datos de prueba:**

| Dato de la orden | Valor |
|---|---|
| Número | ORD-0003 |
| Fecha | 30/07/2026 |
| Estado | En preparación |

| Producto | Precio unitario | Cantidad | Subtotal |
|---|---:|---:|---:|
| Capuchino | $3,00 | 2 | $6,00 |
| Brownie | $2,50 | 1 | $2,50 |
| **Total** |  |  | **$8,50** |

- **Pasos:**
  1. Abrir **Historial de pedidos**.
  2. Seleccionar la orden `ORD-0003`.
  3. Revisar el encabezado y el estado de la orden.
  4. Verificar los productos, precios unitarios, cantidades y subtotales.
  5. Verificar el total pagado.
  6. Presionar **Volver al historial**.
- **Resultado esperado:** El sistema muestra exactamente el número, fecha, estado, productos, cantidades, precios, subtotales y total de la orden `ORD-0003`, y permite regresar al historial sin perder la sesión.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar capturas del detalle completo y del retorno al historial._

---

## TC-016 — Acceso denegado a una orden de otro usuario

- **Tipo:** Negativo (flujo alterno)
- **Objetivo:** Validar que un usuario no pueda consultar el detalle de una orden asociada a otra cuenta.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario `cliente.registrado@example.com` ha iniciado sesión.
  - La orden `ORD-0100` existe, pero pertenece a `otro.cliente@example.com`.
- **Datos de prueba:**

| Dato | Valor |
|---|---|
| Usuario autenticado | cliente.registrado@example.com |
| Orden solicitada | ORD-0100 |
| Propietario real | otro.cliente@example.com |

- **Pasos:**
  1. Iniciar sesión como `cliente.registrado@example.com`.
  2. Intentar abrir directamente la ruta o solicitud correspondiente a la orden `ORD-0100`.
  3. Revisar la respuesta y la información visible.
  4. Regresar al historial del usuario autenticado.
- **Resultado esperado:** El sistema deniega el acceso y muestra un mensaje genérico de orden no encontrada o acceso no autorizado; no revela productos, valores ni datos del propietario de la orden y permite regresar al historial propio.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura del mensaje y, si aplica, código de respuesta o log sin datos sensibles._
