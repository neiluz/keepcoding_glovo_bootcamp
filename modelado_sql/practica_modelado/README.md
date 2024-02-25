# Base de Datos de Videoclub 


## Descripción

Este proyecto de base de datos fue desarrollado como parte de la práctica final del modulo: Modelado y sql. El esquema de la base de datos incluye funcionalidades para registrar socios, películas, directores, géneros, copias de películas, préstamos y devoluciones, así como direcciones, emails y teléfonos de los socios para campañas de publicidad.

- **Objetivos:**
   * Registro de Socios: Implementar un sistema para el registro y seguimiento de los socios del videoclub, incluyendo datos personales y de contacto, para facilitar la emisión de carnets y la comunicación directa.
   * Gestión de Películas: Crear un catálogo digital de películas que permita un fácil acceso a información sobre títulos, directores, géneros y disponibilidad de copias.
   * Préstamos y Devoluciones: Desarrollar un módulo para el registro y seguimiento de préstamos y devoluciones de películas.
     
- **Actividades a desarrollarr**:
   * Modelado de la Base de Datos: Diseñar un esquema de base de datos que refleje de manera eficiente la estructura de datos necesaria para los objetivos planteados.
   * Implementación de Tablas: Crear las tablas necesarias para socios, películas, directores, géneros, copias de películas, préstamos, devoluciones, direcciones, emails y teléfonos.
   * Desarrollo de Consultas SQL: Formular consultas SQL para la inserción, actualización, borrado y consulta de datos.

  ---

## Características
El diagrama del Modelo Entidad-Relación (ER) proporciona una representación visual de la estructura de la base de datos del videoclub. Ilustra cómo las diferentes entidades como Socio, Pelicula, Copia, Prestamo, y otras están interconectadas y cómo se relacionan entre sí a través de diversas claves primarias (PK) y claves foráneas (FK).

![Modelo Entidad-Relación para Videoclub](https://github.com/neiluz/keepcoding_glovo_bootcamp/blob/main/modelado_sql/practica_modelado/Diagrama_videoclub.jpg)

- Socios: Gestión de socios del videoclub con sus datos personales y de contacto.
- Direcciones, Emails y Teléfonos: Información de contacto de los socios para campañas de publicidad y comunicación.
- Películas: Catálogo completo de películas disponibles en el videoclub, incluyendo títulos y sinopsis.
- Géneros y Directores: Clasificación detallada de películas por género y director para facilitar la búsqueda y recomendación de películas.
- Copias de Películas: Registro de todas las copias de cada película, permitiendo un control de inventario eficaz.
- Préstamos: Seguimiento de los préstamos de películas a socios, incluyendo fechas de préstamo y devolución.

## Herramientas Utilizadas

- PostgreSQL para la base de datos.
- draw.io para el diseño del diagrama de entidad-relación.

## Estructura del Repositorio

- `schema.sql`: Script para la creación del esquema de la base de datos.
- `diagrams/`: Diagramas de entidad-relación, ilustrando la estructura y relaciones de la base de datos.
- `data/`: Documentación adicional y datos de ejemplo para facilitar el entendimiento y uso del esquema de la base de datos.

## Cómo Empezar

Para comenzar a utilizar este esquema de base de datos, sigue los siguientes pasos:

1. Clona el repositorio en tu sistema local.
2. Crea una base de datos en PostgreSQL y ejecuta el script `video_club_project.sql` para configurar las tablas y relaciones.
3. Ejecuta el script schema.sql para establecer el esquema de la base de datos en tu sistema.
4. (Opcional) Importa datos de ejemplo desde la carpeta data/ para realizar pruebas.
   
## Uso y Consultas Comunes

Una vez configurado el esquema de la base de datos, puedes realizar consultas SQL para gestionar los distintos aspectos del videoclub. Este esquema está diseñado para soportar operaciones comunes como el registro de nuevos socios, adición de películas al catálogo, préstamo y devolución de copias, y la realización de campañas de publicidad mediante el uso de la información de contacto de los socios.

**Ejempos de consultas:** 

```sql
Registro de Socios
INSERT INTO socio (dni, nombre, apellido, fecha_nacimiento) VALUES ('12345678A', 'Juan', 'Pérez', '1980-01-01');

Adición de Nuevas Películas
INSERT INTO pelicula (titulo, genero_id, director_id, sinopsis) VALUES ('El Rey León', 1, 1, 'Un joven león príncipe...');

Préstamo de Películas
INSERT INTO prestamo (copia_id, numero_socio, fecha_prestamo) VALUES (1, 100, CURRENT_DATE);

Devolución de Películas
UPDATE prestamo SET fecha_devolucion = CURRENT_DATE WHERE prestamo_id = 1;

Consulta de Películas Disponibles
SELECT p.titulo, COUNT(c.copia_id) AS copias_disponibles
FROM Copia c
LEFT JOIN prestamo pr ON c.copia_id = pr.copia_id AND pr.fecha_devolucion IS NULL
JOIN pelicula p ON c.pelicula_id = p.pelicula_id
WHERE pr.prestamo_id IS NULL
GROUP BY p.titulo
HAVING COUNT(c.copia_id) > 0;
```

## Conclusión
El esquema de la base de datos del videoclub es una herramienta integral diseñada para facilitar la administración eficiente de un videoclub, desde el manejo de inventario hasta la interacción con los socios.

Este README proporciona una guía clara sobre cómo configurar y usar el esquema de la base de datos para un videoclub, ofreciendo ejemplos de consultas SQL para operaciones comunes. Puedes adaptarlo según sea necesario para incluir información adicional específica de tu proyecto.


