# Schemas

La carpeta `schemas` contiene los esquemas utilizados para validar y estructurar los datos que recibe y devuelve la API.

Los schemas están construidos utilizando **Pydantic**.

## Archivo

```text
user_shema.py
```

## Responsabilidades

Los schemas permiten:

* Validar datos de entrada.
* Definir los campos requeridos.
* Establecer restricciones de longitud.
* Validar correos electrónicos.
* Definir la estructura de las respuestas.
* Evitar exponer información que no debe devolverse al cliente.

## Schemas de usuarios

El archivo contiene estructuras para diferentes operaciones relacionadas con usuarios.

### Creación

Define los datos necesarios para registrar un usuario.

### Actualización

Permite definir los datos que pueden modificarse.

### Respuesta

Define la información que será enviada al cliente como respuesta de la API.

La contraseña no debe formar parte de la información pública devuelta al cliente.

## Flujo

Los schemas participan en el proceso:

```text
Solicitud HTTP
      │
      ▼
   Schema
      │
      ▼
  Validación
      │
      ▼
    API
      │
      ▼
   Modelo
      │
      ▼
 Base de datos
```

Esto permite mantener separada la validación de datos de los modelos utilizados para la persistencia.
