# Core

La carpeta `core` contiene funcionalidades y configuraciones generales que son utilizadas por diferentes partes de la aplicación.

## Archivos

```text
core/
│
├── README.md
├── cors.py
└── security.py
```

## `cors.py`

Contiene la configuración relacionada con **CORS (Cross-Origin Resource Sharing)**.

Su función es configurar los orígenes, métodos y encabezados permitidos para las solicitudes realizadas hacia la API.

## `security.py`

Contiene funciones relacionadas con la seguridad de las contraseñas.

El proyecto utiliza:

* Passlib.
* Argon2.

Las contraseñas no deben almacenarse directamente en texto plano.

La función de generación de hash permite convertir una contraseña en un valor seguro que puede almacenarse en la base de datos.

También se cuenta con una función para verificar una contraseña contra su hash almacenado.

## Responsabilidad

La carpeta `core` concentra funcionalidades generales para evitar colocar configuraciones y lógica reutilizable directamente dentro de los endpoints.
