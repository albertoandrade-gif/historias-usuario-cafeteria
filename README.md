# Café Express

## Estudiante

Nombre: Alberto Andrade

## Pre-requisitos

Para revisar este proyecto se requiere tener acceso al repositorio GitHub y visualizar archivos en formato Markdown (.md).

## Descripción breve

Café Express es una aplicación web para la gestión de pedidos en línea de una cafetería. La aplicación permite que los usuarios se registren, inicien sesión, exploren el menú, agreguen productos al carrito, realicen pedidos con un pago simulado y consulten el historial de órdenes anteriores.

## Lista de funcionalidades principales

1. **Registro de usuario:** crear una cuenta con email y contraseña.
2. **Inicio de sesión:** acceder de forma segura mediante validación de credenciales.
3. **Explorar menú:** visualizar cafés, bebidas, postres, precios y descripciones.
4. **Agregar productos al carrito:** seleccionar productos y definir cantidades.
5. **Modificar carrito:** actualizar cantidades o eliminar productos antes de confirmar el pedido.
6. **Realizar pedido:** confirmar la compra, seleccionar un método de pago simulado y generar un número de orden.
7. **Historial de pedidos:** consultar pedidos realizados anteriormente.
8. **Consultar detalle de pedido:** revisar productos, cantidades, total y estado de una orden específica.

## Flujo guiado de funcionalidades

- **Registro de usuario:** el cliente crea una cuenta ingresando nombre, correo electrónico y contraseña.
- **Inicio de sesión:** el cliente ingresa al sistema usando su correo y contraseña registrados.
- **Explorar menú:** el cliente revisa la lista de cafés, bebidas y postres disponibles, junto con sus precios y descripciones.
- **Agregar productos al carrito:** el cliente selecciona uno o varios productos e indica la cantidad deseada.
- **Modificar carrito:** el cliente puede cambiar cantidades o eliminar productos antes de comprar.
- **Realizar pedido:** el cliente confirma su compra, selecciona un método de pago simulado y recibe un número de orden.
- **Historial de pedidos:** el cliente consulta las órdenes realizadas previamente.
- **Consultar detalle de pedido:** el cliente revisa el resumen completo de una orden específica.

## Estructura del repositorio

```text
historias-usuario-cafeteria-main/
├── README.md
├── historias_usuario/
│   ├── historia_1.md
│   ├── historia_2.md
│   ├── historia_3.md
│   ├── historia_4.md
│   ├── historia_5.md
│   ├── historia_6.md
│   ├── historia_7.md
│   └── historia_8.md
└── test/
    ├── casos_historia_1.md
    ├── casos_historia_2.md
    ├── casos_historia_3.md
    ├── casos_historia_4.md
    ├── casos_historia_5.md
    ├── casos_historia_6.md
    ├── casos_historia_7.md
    └── casos_historia_8.md
```

## Casos de prueba

Cada archivo de la carpeta `test/` contiene dos casos asociados a su historia de usuario: un caso positivo para el flujo normal y un caso negativo para un flujo alterno. En total se documentan 16 casos de prueba, identificados desde `TC-001` hasta `TC-016`.
