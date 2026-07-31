# Casos de prueba — Historia de usuario 5: Modificar carrito

## TC-009 — Actualizar y eliminar productos del carrito

- **Tipo:** Positivo (flujo normal)
- **Objetivo:** Validar que el cliente pueda cambiar cantidades, eliminar productos y obtener la actualización automática de los totales.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario ha iniciado sesión.
  - El carrito contiene los productos indicados en los datos de prueba.
- **Datos de prueba:**

| Producto | Precio unitario | Cantidad inicial | Acción |
|---|---:|---:|---|
| Espresso | $2,00 | 2 | Aumentar a 3 |
| Brownie | $2,50 | 1 | Eliminar |

- **Pasos:**
  1. Abrir el carrito.
  2. Comprobar que el total inicial sea $6,50.
  3. Cambiar la cantidad de **Espresso** de `2` a `3`.
  4. Verificar el nuevo subtotal del producto.
  5. Eliminar el producto **Brownie**.
  6. Revisar el contenido y el total final del carrito.
- **Resultado esperado:** El sistema muestra únicamente tres unidades de **Espresso**, actualiza su subtotal a $6,00, elimina **Brownie** y presenta un total final de $6,00 sin recargar datos incorrectos.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar capturas del carrito antes y después de las modificaciones._

---

## TC-010 — Intento de confirmar un carrito vacío

- **Tipo:** Negativo (flujo alterno)
- **Objetivo:** Validar que el sistema impida confirmar un pedido después de eliminar el último producto del carrito.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario ha iniciado sesión.
  - El carrito contiene únicamente una unidad de **Té negro**.
- **Datos de prueba:**

| Producto | Precio unitario | Cantidad | Acción |
|---|---:|---:|---|
| Té negro | $1,75 | 1 | Eliminar |

- **Pasos:**
  1. Abrir el carrito.
  2. Eliminar el producto **Té negro**.
  3. Verificar el contenido del carrito.
  4. Intentar seleccionar la opción **Confirmar pedido**.
- **Resultado esperado:** El sistema muestra que el carrito está vacío y deshabilita o bloquea la confirmación; no crea ninguna orden ni calcula un total distinto de $0,00.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura del mensaje de carrito vacío y del bloqueo de la confirmación._
