# VENTAS

## Listado de entidades y atributos

### clientes **(ED)**

- cliente_id **(PK)**
- nombre
- apellidos
- telefono
- email
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

- pais_id
- nombre
- dominio
