# Models

La carpeta `models` contiene los modelos que representan las entidades almacenadas en la base de datos.

## Archivo

```text
user_model.py
```

## `User`

El archivo `user_model.py` define el modelo utilizado para representar a los usuarios.

El modelo está construido utilizando **SQLModel**.

## Información representada

El modelo contiene información relacionada con:

* Identificador del usuario.
* Nombre de usuario.
* Correo electrónico.
* Contraseña almacenada mediante hash.
* Estado del usuario.
* Fecha de creación.

## Responsabilidad

Los modelos representan la estructura de los datos que serán almacenados en la base de datos.

Se utilizan junto con SQLModel para realizar las operaciones de persistencia.

## Relación con otros módulos

```text
Models
   │
   ├── Database
   │
   └── API
```

Los endpoints utilizan los modelos para consultar y modificar los registros almacenados en PostgreSQL.
