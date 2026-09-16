# Database

La carpeta `db` contiene los componentes necesarios para la conexión y comunicación con la base de datos.

## Archivo

```text
database.py
```

## Responsabilidades

El módulo se encarga de:

* Configurar la conexión a la base de datos.
* Crear el engine de SQLModel.
* Administrar las sesiones.
* Crear las tablas.
* Obtener la configuración desde variables de entorno.

## PostgreSQL

El proyecto utiliza PostgreSQL como sistema de gestión de base de datos.

La conexión se configura mediante la variable:

```env
DATABASE_URL
```

Esta variable debe almacenarse en el archivo `.env`.

## Sesiones

El módulo proporciona una sesión de base de datos que puede ser utilizada por los endpoints para realizar operaciones de consulta, inserción, actualización y eliminación.

## Creación de tablas

Las tablas se generan utilizando los modelos registrados en SQLModel.

Esto permite mantener la estructura de la base de datos relacionada directamente con los modelos definidos en la carpeta `models`.
