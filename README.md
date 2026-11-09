# Proyecto de Inteligencia de Negocios
## Optimización del desempeño comercial en la industria de videojuegos: análisis histórico de ventas para la toma de decisiones estratégicas

**Alumno:** Hernández Martínez Ricardo
**Equipo:** Risk Analysts
**Semestre:** 2026-II
**Repositorio:** https://github.com/Richi0001/proyecto_Bi_Videojuegos

## Descripción del proyecto

Este proyecto analiza los factores que apoyan la **toma de decisiones estratégicas** en la industria de videojuegos (género, plataforma, región y año de lanzamiento), a partir del **desempeño comercial histórico** (ventas en copias y posición en el mercado), para orientar la planeación de inversiones en nuevos proyectos.

**Pregunta de negocio:**
¿Qué combinaciones de género, plataforma y región han concentrado mayores ventas históricas entre 1980 y 2016, y qué patrones de distribución pueden servir de referencia para la toma de decisiones de inversión en nuevos proyectos de videojuegos?

---

## Fuentes de datos

### Fuente 1 (seleccionada)
- **Nombre:** Video Game Sales
- **Plataforma:** Kaggle
- **Enlace:** https://www.kaggle.com/datasets/gregorut/videogamesales
- **Autor:** Gregorut (basado en VGChartz)
- **Licencia:** Pública
- **Formato:** CSV
- **Tamaño:** Aprox 2.6 MB
- **Filas:** 16,598
- **Columnas:** 11
- **Cobertura declarada:** 1980-2020
- **Cobertura efectiva verificada:** 1980-2016

### Fuente 2 (alternativa, no utilizada)
- **Nombre:** Video Game Sales with Ratings
- **Plataforma:** Kaggle
- **Enlace:** https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings
- **Autor:** Rush4Ratio
- **Licencia:** Pública
- **Cobertura:** 1980-2017
- **Motivo de descarte:** altos faltantes en calificaciones (Critic_Score: 8,582; User_Score: 6,704) y variables no necesarias para la pregunta.

## Organización del repositorio

proyecto_Bi_Videojuegos/
│
├── README.md
├── docs/
│ ├── avance01.pdf
│ ├── avance02_informe.pdf
│ ├── avance03_informe.pdf
│ └── diccionario_o_metadatos/
│ └── diccionario.txt
├── data/
│ ├── raw/
│ │ ├── vgsales.csv
│ │ └── videoGameSalesWithRatings.csv
│ └── processed/
│ └── (salidas del ETL, generadas por el notebook del Avance 3)
├── notebooks/
│ ├── inspeccion_videojuegos.ipynb
│ ├── idn_p01_Hernandez_Martinez_Ricardo.ipynb
│ ├── idn_p02_Hernandez_Martinez_Ricardo.ipynb
│ ├── idn_avance02_Hernandez_Martinez_Ricardo.ipynb
│ └── idn_avance03_Hernandez_Martinez_Ricardo.ipynb
├── bitacora/
│ ├── bitacora_equipo.txt
│ ├── bitacora_equipo_avance02.txt
│ ├── bitacora_equipo_avance03.txt
│ └── bitacora.csv
└── presentacion/
├── avance01.pdf
├── avance02_presentacion.pdf
└── avance03_presentacion.pdf

## Dependencias

- Python 3.10+
- pandas 2.2.3
- matplotlib (para gráficos del análisis estadístico)
- Jupyter Notebook / Google Colab

## Orden de ejecución

1. `notebooks/inspeccion_videojuegos.ipynb` — Inspección inicial del dataset.
2. `notebooks/idn_avance02_Hernandez_Martinez_Ricardo.ipynb` — Lectura, perfilamiento y preparación de datos (Avance 2).
3. `notebooks/idn_avance03_Hernandez_Martinez_Ricardo.ipynb` — ETL reproducible, validación, conciliación y análisis estadístico (Avance 3).

Los notebooks de prácticas (`idn_p01`, `idn_p02`) son independientes y se usan para las prácticas de Melbourne Housing.

## Cómo obtener los datos

Los datos crudos están en `data/raw/`. Si no se comparten por tamaño, descargar desde:
- https://www.kaggle.com/datasets/gregorut/videogamesales
- https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings

**Nota sobre `data/processed/`:** esa carpeta contiene las salidas del ETL del Avance 3 (`listos.csv`, `pendientes.csv`, `controles.csv`, `bitacora.csv`). Se regeneran automáticamente al ejecutar el notebook del Avance 3. No se versionan si pesan demasiado; se pueden regenerar desde el código.

## Cobertura real

El dataset declara cobertura hasta 2020, pero el análisis verificó que la concentración real de registros termina en 2016. Los años 2017 (3 registros) y 2020 (1 registro) son datos atípicos y no se consideran representativos, los años 2018 y 2019 no presentan registros, las tendencias se delimitan al periodo 1980-2016.

## Resumen del Avance 3

En el Avance 3 implementamos un **ETL reproducible** sobre `vgsales.csv`:

| Etapa | Función | Resultado |
|---|---|---|
| Extracción | `extraer()` | 16,598 filas × 11 columnas |
| Normalización | `normalizar()` | `Year` a Int64; texto con `strip` |
| Validación | `revisar()` | 7 reglas de calidad (5 bloqueantes + 2 reportables) |
| Separación | — | 16,598 válidos, 0 pendientes |
| Preparación | `preparar()` | 12 columnas (+ `decada`), ordenado por Rank |
| Guardado | `to_csv()` | `listos.csv`, `pendientes.csv`, `controles.csv`, `bitacora.csv` |

**Conciliación:** 16,598 = 0 + 16,598 + 0.

**Análisis estadístico:** 5 medidas descriptivas (media/mediana por género, desviación por plataforma, frecuencias, percentiles, correlación NA-EU).

**Reproducibilidad verificada:** misma entrada + mismas reglas = misma salida.
