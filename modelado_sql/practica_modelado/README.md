# Videoclub Database Schema

## Descripción

Este repositorio contiene el esquema de la base de datos para la gestión de un videoclub como práctica final. Incluye todas las tablas necesarias para el registro de socios, direcciones, películas, directores, géneros, copias de películas y préstamos.

## Características

- **Socio**: Registro de miembros del videoclub con detalles personales.
- **Direccion**: Información de contacto para campañas de publicidad.
- **email**: Información de contacto para campañas de publicidad.
- **telefóno**: Información de contacto.
- **Película**: Catálogo de películas con títulos, géneros y directores.
- **Género y Director**: Clasificación de películas por género y director.
- **Copia**: Registro de copias individuales de cada película.
- **Préstamo**: Seguimiento de préstamos y devoluciones de películas.

## Herramientas Utilizadas

- PostgreSQL para la base de datos.
- draw.io para el diseño del diagrama de entidad-relación.

## Estructura del Repositorio

- `schema.sql`: Script para la creación del esquema de la base de datos.
- `diagrams/`: Diagramas de entidad-relación.
- `data/`: Documentación adicional y especificaciones.

## Cómo Empezar

Para comenzar a utilizar este esquema de base de datos, sigue los siguientes pasos:

1. Clona el repositorio en tu sistema local.
2. Crea una base de datos en PostgreSQL y ejecuta el script `schema.sql` para configurar las tablas y relaciones.
   
## Uso

Una vez instalado, puedes ejecutar las consultas SQL dentro de tu base de datos para gestionar el videoclub.

