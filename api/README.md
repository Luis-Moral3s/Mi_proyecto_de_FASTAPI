# API

La carpeta `api` contiene los endpoints y rutas que forman parte de la API REST del proyecto.

Su función principal es recibir las solicitudes HTTP, procesar los datos utilizando los esquemas correspondientes y ejecutar las operaciones necesarias con los modelos y la base de datos.

## Estructura

```text
api/
│
├── README.md
│
└── v1/
    ├── README.md
    └── user_api.py
```

## Organización

Los endpoints están organizados por versiones.

Actualmente el proyecto utiliza la versión:

```text
/api/v1/
```

Esta organización permite mantener una estructura preparada para futuras versiones de la API.

## Responsabilidades

La carpeta `api` se encarga principalmente de:

* Definir rutas HTTP.
* Recibir solicitudes.
* Validar datos mediante schemas.
* Ejecutar operaciones CRUD.
* Consultar y modificar información.
* Generar respuestas HTTP.
* Manejar errores de las solicitudes.

## Dependencias

Los endpoints utilizan componentes de otras partes del proyecto:

```text
api
 │
 ├── schemas
 │
 ├── models
 │
 ├── db
 │
 └── core
```

La carpeta `api` funciona como una capa de comunicación entre el cliente y la lógica de acceso a datos.
