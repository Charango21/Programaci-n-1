# Programaci-n-1
PLEGADOS VERDINI

# Plegados Verdini – Sistema de Gestión de Pedidos

## Objetivo del proyecto

Este proyecto tiene como objetivo desarrollar una aplicación web para gestionar pedidos de trabajos de plegado de chapa para el negocio **Plegados Verdini**.
La aplicación permitirá que los clientes realicen pedidos, que los empleados gestionen esos pedidos y que los administradores supervisen el sistema.

El sistema estará compuesto por:

* **Frontend:** React
* **Backend:** Django (API REST)
* **Base de datos:** PostgreSQL

La comunicación entre el frontend y el backend se realizará mediante una **API REST**.

---

# Arquitectura del sistema

La aplicación se divide en tres partes principales:

1. **Frontend (React)**
   Interfaz donde los usuarios interactúan con el sistema.

2. **Backend (Django API)**
   Maneja la lógica del sistema, autenticación de usuarios y gestión de pedidos.

3. **Base de datos (PostgreSQL)**
   Almacena la información del sistema.

```
React (Frontend)
       ↓
Django REST API (Backend)
       ↓
PostgreSQL (Base de datos)
```

---

# Modelo de datos simplificado

El sistema utiliza **tres tablas principales**.

## 1. Usuario

Almacena los usuarios del sistema.

Campos principales:

* `id`
* `nombre`
* `email`
* `password`
* `rol`

Roles posibles:

* **Administrador**
* **Empleado**
* **Cliente**

Los permisos dentro del sistema dependen de este rol.

---

## 2. Producto

Representa las **especificaciones técnicas del trabajo solicitado** (la chapa o pieza a fabricar).

Campos principales:

* `id`
* `tipo_chapa`
* `espesor`
* `dimensiones`
* `descripcion_tecnica`

Cada producto describe las características técnicas de una orden.

---

## 3. Pedido

Representa una orden realizada por un cliente.

Campos principales:

* `id`
* `cliente_id`
* `producto_id`
* `estado`
* `fecha_pedido`
* `fecha_entrega_estimada`

Relaciones:

* Un **cliente** puede tener muchos pedidos.
* Cada **pedido** tiene un **producto** con las especificaciones técnicas.

---

# Flujo básico del sistema

1. Un **cliente** inicia sesión en la aplicación.
2. El cliente crea un **pedido** con las especificaciones del producto.
3. El pedido se guarda en la base de datos.
4. Un **empleado** visualiza los pedidos pendientes.
5. El empleado define el **tiempo estimado de entrega**.
6. El cliente puede consultar el estado de su pedido.

---

# Funcionalidades principales

* Registro e inicio de sesión de usuarios
* Gestión de roles (administrador, empleado, cliente)
* Creación de pedidos por parte de clientes
* Visualización y gestión de pedidos por empleados
* Consulta del estado del pedido

---

# Tecnologías utilizadas

### Backend

* Django
* Django REST Framework

### Frontend

* React

### Base de datos

* PostgreSQL

---

# Objetivo académico

Este proyecto tiene como finalidad practicar:

* Desarrollo **full stack**
* Diseño de **API REST**
* Modelado de **bases de datos relacionales**
* Integración entre **React y Django**
* Uso de **PostgreSQL** como base de datos

---

# Estado del proyecto

Proyecto en desarrollo.
