# SWIIIRodriguezAlquiler

# IDENTIFICACIÓN DE SUBDOMINIOS

## Subdominio Principal

### GestionAlquileres
Este subdominio es core, ya que es la función principal de la empresa. Se encarga de gestionar las reservas de vehículos, y los documentos asociados a los alquileres.

### GestionPagos
Este subdominio es core, y se encarga de gestionar los pagos de los alquileres que realizan los clientes y es un subdominio en el cual la empresa tiene que aplicar sus propias políticas de pagos.

## Subdominio de apoyo

### GestionClientes
Este subdominio es de apoyo, ya que es necesario para gestionar la información de los clientes, como sus datos personales, sus preferencias, y su historial de alquileres; pero no genera una ventaja competitiva a la empresa.

### GestionVehiculos
Este subdominio es de apoyo, ya que es necesario para gestionar el inventario de vehículos, el mantenimiento de los vehículos, y los seguros de los vehículos así como el estado para el alquiler, pero tampoco genera una ventaja para la empresa.

## Subdominio genérico

### GestionSeguridad
Este subdominio es genérico, que se va a encargar de la seguridad del sistema y de los datos personales de los clientes como el de sus tarjetas asociados al sistema. Puede ser implementado de diferentes maneras, dependiendo de las necesidades de la empresa.

# BOUNDED CONTEXTS
### GestionAlquileres
Este bonded context abarca las reservas de los vehículos y la documentación de los alquileres

### GestionPagos


### GestionClientes
Este bonded context abarca la gestión de los datos personales de los clientes, las preferencias de los clientes para futuras transacciones y el historial de alquileres de los clientes para que estos puedan conocer de lo que hicieron.
### GestionVehiculos
Este bonded context abarca la gestion del inventario de vehículos, la gestin de mantenimiento de vehiculos y los seguros asociados a ellos

### GestionSeguridad
Este bonded contex abarca todo el procesamiento de pagos y la gestión de devoluciones cuando un alquiler se cancela.

# PATRONES DE RELACIÓN
GestionClientes -> GestionAlquileres
GestionVehiculos -> GestionAlquileres
GestionClientes [U]->[D,ACL] GestionPagos
GestionAlquileres [U]->[D,ACL] GestionPagos
GestionVehiculos [U] -> [D,CF] GestionClientes
GestionClientes [U]->[D,ACL] GestionSeguridad
GestionPagos [U]->[D,ACL] GestionSeguridad