# Dashboard de Análisis de Precios de Propiedades

Este repositorio contiene los archivos y recursos necesarios para construir un dashboard interactivo que analiza el precio final promedio de las propiedades basado en varios KPIs. El dashboard visualiza datos geográficos y estadísticos para ayudar a identificar patrones y tendencias en el mercado inmobiliario.

## Descripción del Dashboard

El dashboard está diseñado para ofrecer una visión detallada del mercado inmobiliario a través de tres vistas principales:

1. **Mapa por Código Postal:**
   - **Objetivo:** Visualizar el precio final promedio en cada código postal.
   - **Detalles:** Se utiliza un filtro de "Top N" basado en el número de reseñas para destacar áreas con alta actividad.

2. **Gráfico por Tipo de Propiedad:**
   - **Objetivo:** Mostrar el precio final promedio clasificado por tipo de propiedad.
   - **Detalles:** Se aplican filtros para mostrar solo los tipos de propiedades más relevantes o con los precios más altos.

3. **Mapa por Código Postal, Barrio y Host ID:**
   - **Objetivo:** Detallar la distribución geográfica con enfoque en diferentes barrios y Host IDs.
   - **Detalles:** Visualización en capas para facilitar la comparación entre diferentes zonas y gestores de propiedades.

## Herramientas Utilizadas

- [Tableau](https://www.tableau.com/)
  
## Estructura del Repositorio

- `/data`: Contiene los datasets utilizados en el dashboard.
- `/visualizations`: Almacena los archivos de visualización del dashboard.
