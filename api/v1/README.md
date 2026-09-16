# API v1

Esta carpeta contiene la primera versión de los endpoints de la API REST.

Actualmente contiene las rutas relacionadas con la gestión de usuarios.

## Archivo

### `user_api.py`

Contiene el router encargado de las operaciones relacionadas con los usuarios.

## Endpoint base

Las rutas utilizan el prefijo:

```text
/api/v1/users
```

## Operaciones disponibles

### Crear usuario

```http
POST /api/v1/users/
```

Permite registrar un nuevo usuario.

Los datos recibidos son validados mediante los schemas definidos en la carpeta `schemas`.

### Obtener usuarios

```http
GET /api/v1/users/
```

Permite consultar los usuarios registrados.

### Obtener usuario

```http
GET /api/v1/users/{user_id}
```

Permite consultar un usuario específico utilizando su identificador.

### Actualizar usuario

```http
PUT /api/v1/users/{user_id}
```

Permite modificar la información de un usuario existente.

### Eliminar usuario

```http
DELETE /api/v1/users/{user_id}
```

Permite eliminar un usuario mediante su identificador.

## Relación con otros módulos

`user_api.py` utiliza diferentes componentes del proyecto:

```text
user_api.py
    │
    ├── schemas
    │
    ├── models
    │
    ├── db
    │
    └── core/security.py
```

Esto permite mantener separadas las responsabilidades de rutas, validación, datos y seguridad.
