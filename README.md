# Mi proyecto de FastAPI

Proyecto desarrollado con **FastAPI** para la creación de una API REST orientada a la gestión de usuarios.

El proyecto utiliza una estructura organizada por responsabilidades, separando las rutas de la API, configuración general, seguridad, conexión con la base de datos, modelos y esquemas de validación.

## Tecnologías utilizadas

* Python
* FastAPI
* SQLModel
* Pydantic
* PostgreSQL
* Passlib
* Argon2
* Docker
* Docker Compose

## Estructura del proyecto

```text
trabajo4/
│
├── README.md
├── .gitignore
├── .env.example
├── docker-compose.yml
├── main.py
│
├── api/
│   ├── README.md
│   └── v1/
│       ├── README.md
│       └── user_api.py
│
├── core/
│   ├── README.md
│   ├── cors.py
│   └── security.py
│
├── db/
│   ├── README.md
│   └── database.py
│
├── models/
│   ├── README.md
│   └── user_model.py
│
└── schemas/
    ├── README.md
    └── user_shema.py
```

## Descripción de las carpetas

### `api/`

Contiene las rutas y endpoints de la API REST.

Aquí se reciben las solicitudes HTTP y se realizan las operaciones correspondientes sobre los usuarios.

### `core/`

Contiene funcionalidades generales de la aplicación, principalmente configuración de CORS y seguridad.

### `db/`

Contiene la configuración necesaria para conectarse y trabajar con la base de datos PostgreSQL.

### `models/`

Contiene los modelos utilizados para representar las entidades de la base de datos mediante SQLModel.

### `schemas/`

Contiene los esquemas utilizados para validar los datos de entrada y estructurar las respuestas de la API.

## Funcionalidades

Actualmente el proyecto permite realizar operaciones CRUD sobre usuarios:

* Crear usuarios.
* Consultar usuarios.
* Consultar un usuario por ID.
* Actualizar usuarios.
* Eliminar usuarios.
* Validar información recibida.
* Validar correos electrónicos.
* Proteger las contraseñas mediante hash.
* Utilizar Argon2 para el almacenamiento seguro de contraseñas.
* Conectarse a PostgreSQL.

## API

Los endpoints de usuarios se encuentran bajo:

```text
/api/v1/users
```

### Crear usuario

```http
POST /api/v1/users/
```

### Obtener usuarios

```http
GET /api/v1/users/
```

### Obtener usuario por ID

```http
GET /api/v1/users/{user_id}
```

### Actualizar usuario

```http
PUT /api/v1/users/{user_id}
```

### Eliminar usuario

```http
DELETE /api/v1/users/{user_id}
```

## Documentación automática

FastAPI genera documentación interactiva automáticamente.

Una vez iniciada la aplicación:

```text
http://127.0.0.1:8000/docs
```

También se puede consultar:

```text
http://127.0.0.1:8000/redoc
```

## Configuración

Las variables de configuración sensibles deben almacenarse en un archivo `.env`.

Ejemplo:

```env
DATABASE_URL=postgresql+psycopg2://USUARIO:CONTRASEÑA@localhost:5433/NOMBRE_BASE_DATOS
```

El archivo `.env` no debe subirse al repositorio.

Se puede utilizar `.env.example` como referencia para configurar el proyecto.

## Ejecución del proyecto

Crear un entorno virtual:

```bash
python -m venv .venv
```

Activarlo en Windows:

```bash
.venv\Scripts\activate
```

Instalar las dependencias:

```bash
pip install -r requirements.txt
```

Ejecutar la aplicación:

```bash
uvicorn main:app --reload
```

La API estará disponible en:

```text
http://127.0.0.1:8000
```

## PostgreSQL con Docker

El proyecto incluye un archivo `docker-compose.yml` para facilitar la ejecución de PostgreSQL.

Para iniciar el contenedor:

```bash
docker compose up -d
```

Para detenerlo:

```bash
docker compose down
```

## Arquitectura

La comunicación general del proyecto sigue una estructura similar a:

```text
Cliente
   │
   ▼
FastAPI
   │
   ▼
API / Routers
   │
   ├── Schemas
   │
   ├── Models
   │
   └── Core
   │
   ▼
Base de datos
   │
   ▼
PostgreSQL
```

La separación de responsabilidades facilita el mantenimiento y permite organizar el proyecto por componentes.

## Objetivo del proyecto

El objetivo es desarrollar una API REST utilizando FastAPI, aplicando conceptos de:

* Desarrollo de APIs.
* Arquitectura de software.
* Validación de datos.
* Bases de datos.
* Seguridad.
* Manejo de sesiones.
* Contenedores.
* Documentación de proyectos.

## Autor

**Luis Morales**
