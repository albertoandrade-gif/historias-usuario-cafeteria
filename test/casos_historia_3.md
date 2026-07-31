# Casos de prueba — Historia de usuario 3: Explorar menú

## TC-005 — Visualización del menú con productos disponibles

- **Tipo:** Positivo (flujo normal)
- **Objetivo:** Validar que el cliente pueda consultar un menú claro con productos, categorías, descripciones y precios.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario ha iniciado sesión.
  - Existen productos activos y disponibles en distintas categorías.
- **Datos de prueba:**

| Producto | Categoría | Descripción | Precio | Disponibilidad |
|---|---|---|---:|---|
| Capuchino | Cafés | Café con leche espumada | $3,00 | Disponible |
| Brownie | Postres | Brownie de chocolate | $2,50 | Disponible |

- **Pasos:**
  1. Iniciar sesión con un usuario válido.
  2. Abrir la opción **Menú**.
  3. Verificar que se muestren los productos disponibles.
  4. Revisar el nombre, descripción, precio y categoría de cada producto de prueba.
  5. Seleccionar el producto **Capuchino**.
- **Resultado esperado:** El sistema muestra los productos ordenados y diferenciados por categoría, presenta correctamente todos sus datos y permite seleccionar un producto disponible para agregarlo al carrito.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura del menú y de la selección del producto._

---

## TC-006 — Menú sin productos disponibles

- **Tipo:** Negativo (flujo alterno)
- **Objetivo:** Validar la respuesta del sistema cuando no existen productos disponibles para la venta.
- **Precondiciones:**
  - La aplicación Café Express se encuentra disponible.
  - El usuario ha iniciado sesión.
  - Todos los productos están inactivos, agotados o la base de pruebas no contiene productos.
- **Datos de prueba:**

| Condición | Valor |
|---|---|
| Productos disponibles | 0 |

- **Pasos:**
  1. Iniciar sesión con un usuario válido.
  2. Abrir la opción **Menú**.
  3. Esperar a que finalice la carga de la información.
  4. Revisar el contenido y las acciones disponibles en la pantalla.
- **Resultado esperado:** El sistema muestra un mensaje informativo como “No hay productos disponibles”, no presenta datos incompletos y no permite agregar productos inexistentes al carrito.
- **Resultado obtenido:** _Pendiente de completar tras la ejecución._
- **Estado:** Pendiente (Pass / Fail)
- **Notas/Evidencias:** _Pendiente: adjuntar captura del mensaje mostrado y, si aplica, respuesta del servicio de productos._
