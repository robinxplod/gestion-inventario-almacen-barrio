# gestion-inventario-almacen-barrio
Diseño de una solución interactiva para la gestión de inventario en un almacén de barrio.
# Cuaderno Digital

Prototipo académico para la Unidad 2 de Interacción Humano Computador. Representa un inventario de almacén de barrio con una lista de productos y botones grandes.

## Abrir el prototipo

Abre `dist/index.html` con Chrome o Edge. No requiere instalación. Conserva `index.html`, `styles.css` y `app.js` juntos dentro de `dist/`.

## Qué permite hacer

- Buscar productos por nombre, con o sin tildes.
- Consultar productos frecuentes mediante “Más vendidos” (selección fija de ejemplo; no es un ranking calculado).
- Registrar ventas y reposiciones con cantidades enteras.
- Ver las existencias actualizadas y deshacer un movimiento inmediatamente después de registrarlo.
- Consultar “Por reponer” e historial de movimientos.
- Corregir el conteo real y modificar el mínimo de existencias.
- Agregar productos y descargar el historial en CSV.
- Consultar la ayuda y reiniciar la demostración con confirmación previa.

## Recorrido para la demostración

1. Abre “Mis productos”. El arroz tiene 12 unidades.
2. Toca “Arroz”, luego “Vendí” y confirma una unidad.
3. Comprueba el resultado: quedan 11 unidades.
4. Vuelve a los productos, abre “Aceite vegetal”, elige “Llegó mercadería”, indica 6 y confirma.
5. El aceite pasa de 3 a 9 unidades y deja de aparecer en “Por reponer”.
6. Abre “Movimientos” para revisar ambos registros.
7. Para repetir exactamente el ejemplo, usa “Reiniciar demostración”.

## Alcance y limitaciones

Los productos y cantidades son ficticios. Los datos se guardan en el almacenamiento local del navegador; no se sincronizan entre usuarios o dispositivos. Si el navegador impide el almacenamiento, los cambios solo duran durante la sesión y la pantalla lo indica. Abrir la versión local y la versión alojada utiliza almacenamientos independientes.

El prototipo implementa los recorridos principales con detalles visuales y comportamiento funcional. No es un sistema comercial: no procesa pagos, no calcula ventas monetarias ni utiliza base de datos, cámara o autenticación propia. “Mi negocio” es una etiqueta del ejemplo.

Se modelan unidades enteras de presentaciones de productos. La venta a granel por peso y cantidades decimales queda como mejora futura. El escáner también queda fuera de esta versión.

Si una venta supera las existencias registradas, se muestra una advertencia y se pide corregir primero el conteo. Esta decisión evita inventarios negativos y modifica la propuesta inicial de permitir la venta tras advertir. Debe coordinarse con los integrantes 2 y 3 y reflejarse en el informe.

Deshacer anula el movimiento y conserva su anotación en el historial. Desde la confirmación se puede anular ese movimiento si no hay otro posterior activo del mismo producto. La corrección del mínimo no se revierte al deshacer una corrección de existencias.

## Organización para GitHub

Se puede subir la carpeta `dist/` como `prototipo/` al repositorio del equipo. Agregar este README, las capturas en `evidencias/` y el informe en `documentos/`. No se ha modificado el repositorio GitHub del equipo.

Los commits y acuerdos deben corresponder al trabajo real de cada integrante. Este paquete no incluye historial ficticio de colaboración ni resultados de pruebas con usuarios.

## Coordinación con el integrante 3

Navegación: Mis productos / Por reponer / Movimientos. Flujo principal: producto → Vendí o Llegó mercadería → cantidad → confirmar → resultado. Apoyos: búsqueda, controles grandes, texto junto al color, confirmación, deshacer y corrección del conteo. El flujo de una unidad parte de una tarjeta visible y requiere tres toques; buscar un producto o cambiar la cantidad agrega acciones.

## Clasificación del prototipo

Se entrega un prototipo navegable con apariencia definida e interacción funcional local, cercano a alta fidelidad en sus recorridos principales. Si el informe anterior indicaba “fidelidad media”, debe actualizarse para describir el resultado construido. Esta clasificación no implica que sea una aplicación lista para uso comercial.
