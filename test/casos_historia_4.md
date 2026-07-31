# Casos de prueba — Historia de usuario 4: Agregar productos al carrito

## TC-007 — Agregar un producto con cantidad válida

- **Tipo:** Positivo (flujo normal)
- **Objetivo:** Validar que el cliente pueda agregar un producto, definir su cantidad y obtener los cálculos correctos en el carrito.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario ha iniciado sesión.
  - El carrito está vacío.
  - El producto **Latte** se encuentra disponible.
- **Datos de prueba:**

| Producto | Precio unitario | Cantidad | Subtotal esperado |
|---|---:|---:|---:|
| Latte | $3,00 | 2 | $6,00 |

- **Pasos:**
  1. Abrir el menú de productos.
  2. Seleccionar el producto **Latte**.
  3. Establecer la cantidad en `2`.
  4. Presionar **Agregar al carrito**.
  5. Abrir el carrito y revisar sus valores.
  6. Volver a agregar una unidad del mismo producto.
- **Resultado esperado:** El sistema confirma visualmente la adición, muestra una sola línea para **Latte**, calcula inicialmente $6,00 y, al agregar otra unidad, actualiza la cantidad a `3` y el total a $9,00 sin duplicar el producto.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar capturas de la confirmación y de los valores del carrito._

---

## TC-008 — Rechazo de cantidad no permitida

- **Tipo:** Negativo (flujo alterno)
- **Objetivo:** Validar que el sistema no permita agregar un producto con una cantidad igual a cero.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario ha iniciado sesión.
  - El carrito está vacío.
  - El producto **Latte** se encuentra disponible.
- **Datos de prueba:**

| Producto | Precio unitario | Cantidad inválida |
|---|---:|---:|
| Latte | $3,00 | 0 |

- **Pasos:**
  1. Abrir el menú de productos.
  2. Seleccionar el producto **Latte**.
  3. Intentar establecer la cantidad en `0`.
  4. Presionar **Agregar al carrito** si la acción se encuentra habilitada.
  5. Abrir o revisar el carrito.
- **Resultado esperado:** El sistema rechaza la cantidad, muestra un mensaje de validación, no agrega el producto y mantiene el total del carrito en $0,00.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura de la validación y del carrito sin modificaciones._
