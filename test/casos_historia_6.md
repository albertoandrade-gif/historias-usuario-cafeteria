# Casos de prueba — Historia de usuario 6: Realizar pedido

## TC-011 — Confirmación exitosa de un pedido

- **Tipo:** Positivo (flujo normal)
- **Objetivo:** Validar que el cliente pueda revisar el resumen, elegir un método de pago simulado y generar una orden correctamente.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario ha iniciado sesión.
  - El carrito contiene los productos indicados.
  - El servicio de generación de órdenes se encuentra disponible.
- **Datos de prueba:**

| Producto | Precio unitario | Cantidad | Subtotal |
|---|---:|---:|---:|
| Capuchino | $3,00 | 2 | $6,00 |
| Brownie | $2,50 | 1 | $2,50 |

| Dato adicional | Valor |
|---|---|
| Total esperado | $8,50 |
| Método de pago simulado | Tarjeta |

- **Pasos:**
  1. Abrir el carrito.
  2. Seleccionar **Continuar** o **Confirmar pedido**.
  3. Revisar productos, cantidades, subtotales y total del resumen.
  4. Seleccionar **Tarjeta** como método de pago simulado.
  5. Presionar el botón para generar la orden.
  6. Aceptar el mensaje final de confirmación.
  7. Abrir el historial de pedidos.
- **Resultado esperado:** El sistema muestra un total de $8,50, solicita confirmación, genera un número de orden único, presenta un mensaje de éxito y guarda el pedido con sus datos en el historial del usuario.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar capturas del resumen, número de orden, confirmación e historial._

---

## TC-012 — Confirmación sin método de pago

- **Tipo:** Negativo (flujo alterno)
- **Objetivo:** Validar que el sistema no genere una orden si el cliente omite el método de pago simulado.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario ha iniciado sesión.
  - El carrito contiene una unidad de **Latte**.
  - No existe un método de pago seleccionado previamente.
- **Datos de prueba:**

| Producto | Precio unitario | Cantidad | Método de pago |
|---|---:|---:|---|
| Latte | $3,00 | 1 | Sin seleccionar |

- **Pasos:**
  1. Abrir el carrito.
  2. Seleccionar **Continuar** o **Confirmar pedido**.
  3. Verificar el resumen del pedido.
  4. Dejar el método de pago sin seleccionar.
  5. Presionar el botón para generar la orden.
  6. Revisar el historial de pedidos.
- **Resultado esperado:** El sistema informa que el método de pago es obligatorio, mantiene el pedido sin confirmar, no genera un número de orden y no agrega ningún registro al historial.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura de la validación y evidencia de que el historial no cambió._
