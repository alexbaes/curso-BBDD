# VENTAS

## Listado de entidades y atributos

### clientes **(ED)**

- cliente_id **(PK)**
- nombre
- apellidos
- telefono **(UQ)**
- email **(UQ)**
- direccion
- cp
- ciudad
- pais **(FK)**

### productos **(ED|EC)**

- producto_id **(PK)**
- nombre
- descripcion
- foto
- precio
- cantidad_stock

### ventas

- venta_id **(PK)**
- cliente_id **(FK)**
- fecha
- importe

### articulos_x_venta **(EP)**

- articulo_id **(PK)**
- ventas_id **(FK)**
- producto_id **(FK)**
- cantidad

### paises **(EC)**

- pais_id **(PK)**
- nombre
- dominio **(UQ)**

## Relaciones

- **Un cliente** pertenece a **un país** (_1 - 1_).
- **Un cliente** genera **varias ventas** (_1 - M_).
- **Una venta** tiene **varios artículos** (_1 - M_).
- **Un artículo** es **un producto** (\_1 - 1).
