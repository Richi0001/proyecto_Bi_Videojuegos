DICCIONARIO DE DATOS

Proyecto: Análisis de factores de éxito comercial en la industria de videojuegos
Equipo: Risk Analysts
Fecha: 15 de septiembre de 2026

==================================================
FUENTE 1 (DATASET SELECCIONADO)
==================================================

INFORMACIÓN GENERAL
-------------------
Nombre: Video Game Sales
Plataforma: Kaggle
Enlace: https://www.kaggle.com/datasets/gregorut/videogamesales
Autor original: Gregorut (basado en datos de VGChartz)
Fecha de consulta: 15 de septiembre de 2026
Licencia: Pública
Formato: CSV
Tamaño: aprox 2.6 MB
Filas: 16,598
Columnas: 11
Cobertura: 1980-2020, global
Unidad de observación: Un videojuego

DICCIONARIO DE COLUMNAS
-----------------------
Rank: Entero. Posición en el ranking global de ventas. Ejemplo: 1. Rango: 1 - 16,598.
Name: Texto. Nombre del videojuego. Ejemplo: Wii Sports.
Platform: Texto. Plataforma de lanzamiento. Ejemplo: Wii, PS4, Xbox. Varias.
Year: Entero. Año de lanzamiento. Ejemplo: 2006. Rango: 1980 - 2020.
Genre: Texto. Género del videojuego. Ejemplo: Sports, Action. Varias.
Publisher: Texto. Empresa que publicó el juego. Ejemplo: Nintendo. Varias.
NA_Sales: Decimal. Ventas en Norteamérica (millones). Ejemplo: 41.49. Rango: 0 - 82.74.
EU_Sales: Decimal. Ventas en Europa (millones). Ejemplo: 29.02. Rango: 0 - 50.00.
JP_Sales: Decimal. Ventas en Japón (millones). Ejemplo: 3.77. Rango: 0 - 10.22.
Other_Sales: Decimal. Ventas en otras regiones (millones). Ejemplo: 8.46. Rango: 0 - 20.00.
Global_Sales: Decimal. Ventas globales (millones). Ejemplo: 82.74. Rango: 0 - 82.74.

METADATOS DISPONIBLES
---------------------
La página de Kaggle no incluye un diccionario formal, pero los nombres de las columnas son descriptivos.
No se especifica la fecha exacta de recolección de datos.
La fuente original es VGChartz, un sitio de seguimiento de ventas de videojuegos.

LIMITACIONES CONOCIDAS
----------------------
Valores faltantes en Year y Publisher.
Datos hasta 2020 (no reflejan tendencias recientes).
No incluye calificaciones de crítica ni usuarios.
No incluye datos de presupuesto o marketing.

==================================================
FUENTE 2 (ALTERNATIVA)
==================================================

INFORMACIÓN GENERAL
-------------------
Nombre: Video Game Sales with Ratings
Plataforma: Kaggle
Enlace: https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings
Autor original: Rush4Ratio (basado en VGChartz y Metacritic)
Fecha de consulta: 15 de septiembre de 2026
Licencia: pública
Formato: CSV
Tamaño: aprox 3 MB
Filas: 16,719
Columnas: 16
Cobertura: 1980-2017, global
Unidad de observación: Un videojuego

DICCIONARIO DE COLUMNAS
-----------------------
Name: Texto. Nombre del videojuego. Ejemplo: Wii Sports.
Platform: Texto. Plataforma. Ejemplo: Wii.
Year_of_Release: Entero. Año de lanzamiento. Ejemplo: 2006. Faltantes.
Genre: Texto. Género. Ejemplo: Sports.
Publisher: Texto. Empresa que publicó. Ejemplo: Nintendo. Faltantes.
NA_Sales: Decimal. Ventas en Norteamérica (millones). Ejemplo: 41.49.
EU_Sales: Decimal. Ventas en Europa (millones). Ejemplo: 29.02.
JP_Sales: Decimal. Ventas en Japón (millones). Ejemplo: 3.77.
Other_Sales: Decimal. Ventas en otras regiones (millones). Ejemplo: 8.46.
Global_Sales: Decimal. Ventas globales (millones). Ejemplo: 82.74.
Critic_Score: Decimal. Calificación de crítica (0-100). Ejemplo: 76. Muchos faltantes.
Critic_Count: Entero. Número de críticas. Ejemplo: 51. Muchos faltantes.
User_Score: Texto/Número. Calificación de usuarios (0-10). Ejemplo: 8.0. Valores "tbd".
User_Count: Entero. Número de usuarios que calificaron. Ejemplo: 322. Muchos faltantes.
Developer: Texto. Desarrollador. Ejemplo: Nintendo. Faltantes.
Rating: Texto. Clasificación ESRB. Ejemplo: E. Faltantes.

METADATOS DISPONIBLES
---------------------
Incluye calificaciones de crítica (Metacritic) y usuarios.
No incluye diccionario formal, pero las columnas son descriptivas.

LIMITACIONES CONOCIDAS
----------------------
Muchos valores faltantes en columnas de ratings.
Valores "tbd" en User_Score que deben tratarse como faltantes (N/A).
Cobertura hasta 2017 (menor que la Fuente 1).

==================================================
DECISIÓN SOBRE LAS FUENTES
==================================================
Fuente 1 (Video Game Sales): Aceptar-->Contiene todas las variables necesarias, tiene licencia pública y mejor cobertura temporal.
Fuente 2 (Video Game Sales with Ratings): Aceptar con cautela --> Útil como alternativa, pero con más faltantes y menor cobertura.

Se selecciona la Fuente 1 como base principal del proyecto.

==================================================
ATRIBUCIÓN
==================================================
Los datos utilizados provienen de:
- Video Game Sales, publicado por Gregorut en Kaggle, basado en datos de VGChartz.
- Video Game Sales with Ratings, publicado por Rush4Ratio en Kaggle, basado en VGChartz y Metacritic.

Ambos datasets tienen licencia Publica.
