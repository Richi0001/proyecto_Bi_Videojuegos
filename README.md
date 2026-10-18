# Proyecto de Inteligencia de Negocios, avance 02
## Optimización del desempeño comercial en la industria de videojuegos: análisis histórico de ventas para la toma de decisiones estratégicas

**Alumno:** Hernández Martínez Ricardo
**Equipo:** Risk Analysts
**Semestre:** 2026-2
**Repositorio:** https://github.com/Richi0001/proyecto_Bi_Videojuegos

---

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
- **Tamaño:** aprox 2.6 MB
- **Filas:** 16,598
- **Columnas:** 11
- **Cobertura declarada:** 1980-2020
- **Cobertura efectiva verificada:** 1980-2016

### Fuente 2 (alternativa)
- **Nombre:** Video Game Sales with Ratings
- **Plataforma:** Kaggle
- **Enlace:** https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings
- **Autor:** Rush4Ratio
- **Licencia:** Pública
- **Cobertura:** 1980-2017

---

## Organización del repositorio

proyecto_Bi_Videojuegos/
│
├── README.md
├── docs/
│ ├── avance01.pdf
│ ├── avance02_informe.pdf
│ └── diccionario_o_metadatos/
│ └── diccionario.txt
├── data/
│ └── raw/
│ ├── vgsales.csv
│ └── videoGameSalesWithRatings.csv
├── notebooks/
│ ├── inspeccion_videojuegos.ipynb
│ ├── idn_p01_Hernandez_Martinez_Ricardo.ipynb
│ ├── idn_p02_Hernandez_Martinez_Ricardo.ipynb
│ └── idn_avance02_Hernandez_Martinez_Ricardo.ipynb
├── bitacora/
│ └── bitacora_equipo.txt
└── presentacion/
├── avance01.pdf
└── avance02_presentacion.pdf

---

## Dependencias

- Python 3.10+
- pandas 2.2.3
- Jupyter Notebook / Google Colab

---

## Orden de ejecución

1. `notebooks/inspeccion_videojuegos.ipynb` - Inspección inicial
2. `notebooks/idn_avance02_Hernandez_Martinez_Ricardo.ipynb` - Avance 2
---

## Cómo obtener los datos

Los datos crudos están en `data/raw/`. Si no se comparten por tamaño, descargar desde:
- https://www.kaggle.com/datasets/gregorut/videogamesales
- https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings

---

## Nota sobre cobertura

El dataset declara cobertura hasta 2020, pero el análisis verificó que la concentración real de registros termina en 2016. Los años 2017 (3 registros) y 2020 (1 registro) se identifican como datos atípicos y no se consideran representativos. Los años 2018 y 2019 no presentan registros. Las tendencias se delimitan al periodo 1980-2016.

---

## Estado del proyecto

- Avance 1: Problema, datos y plan analítico
- Avance 2: Lectura, perfilamiento y preparación de datos con Python
