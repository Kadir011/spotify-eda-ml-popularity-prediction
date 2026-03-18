<div align="center">

<img src="https://storage.googleapis.com/pr-newsroom-wp/1/2023/05/Spotify_Primary_Logo_RGB_Green.png" width="80" alt="Spotify Logo"/>

# Spotify EDA & ML Popularity Prediction

### Análisis exploratorio de datos y predicción de popularidad musical

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-11557C?style=for-the-badge&logo=plotly&logoColor=white)](https://matplotlib.org/)
[![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/drive/1ZpWB1F8B9L_U3Yl0SJGMHOK7G-I1zyHI?usp=sharing)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/solomonameh/spotify-music-dataset)

</div>

---

## Descripción del Proyecto

Pipeline completo de **ciencia de datos aplicada a la industria musical**. Se analizaron y procesaron **4,831 canciones** de Spotify para descubrir qué factores determinan la popularidad de una canción y predecirla mediante modelos de Machine Learning — incluyendo casos de estudio post-fallecimiento de artistas icónicos.

---

## Datasets

<div align="center">

| Dataset | Descripción | Tamaño |
|:---|:---|:---:|
| `high_popularity_spotify_data.csv` | Canciones con **alta popularidad** en Spotify | 287 tracks |
| `low_popularity_spotify_data.csv` | Canciones con **baja popularidad** en Spotify | 614 tracks |

**Variables de audio analizadas:** `energy` · `tempo` · `danceability` · `loudness` · `valence` · `acousticness` · `speechiness` · `liveness`

**Fuente:** [Spotify Music Dataset — Kaggle](https://www.kaggle.com/datasets/solomonameh/spotify-music-dataset)

</div>

---

## Stack Tecnológico

<div align="center">

| Herramienta | Versión | Uso Principal |
|:---:|:---:|:---|
| <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/> | 3.10+ | Lenguaje base del proyecto |
| <img src="https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white"/> | 2.0+ | Carga, limpieza y manipulación de datos |
| <img src="https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white"/> | 1.24+ | Operaciones numéricas y simulaciones |
| <img src="https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=plotly&logoColor=white"/> | 3.7+ | Visualizaciones y gráficos base |
| <img src="https://img.shields.io/badge/Seaborn-4C72B0?style=flat&logo=python&logoColor=white"/> | 0.12+ | Visualizaciones estadísticas avanzadas |
| <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white"/> | 1.3+ | Modelos de Machine Learning |
| <img src="https://img.shields.io/badge/Google_Colab-F9AB00?style=flat&logo=googlecolab&logoColor=white"/> | — | Entorno de ejecución en la nube |

</div>

---

## Contenido del Notebook

<div align="center">

| # | Sección | Descripción |
|:---:|:---|:---|
| 1 | 🔧 **Importar dependencias** | Configuración del entorno y librerías |
| 2 | 📥 **Cargar datasets** | Carga de archivos CSV desde Google Colab |
| 3 | 🧹 **Limpieza avanzada** | Eliminación de duplicados, nulos y outliers |
| 4 | 🔍 **5 Consultas analíticas** | Insights sobre géneros, artistas y audio features |
| 5 | 📊 **8 Visualizaciones** | Gráficos estilo Spotify: heatmaps, boxplots, barplots |
| 6 | 🤖 **Modelos ML** | Random Forest + Regresión Logística con class_weight |
| 7 | 🎤 **Caso Especial: Juice WRLD** | Impacto post-fallecimiento en popularidad |
| 8 | 🎧 **Caso Especial: Avicii** | Legado en EDM y simulación 2018–2024 |
| 9 | 📝 **Conclusiones Finales** | Hallazgos clave y próximos pasos |

</div>

---

## Modelos de Machine Learning

<div align="center">

| Modelo | AUC | Observaciones |
|:---|:---:|:---|
| Random Forest (inicial) | 0.637 | Predijo 100% como "Baja popularidad" — sesgo crítico |
| Regresión Logística `balanced` | **0.707** | Detectó 57/287 canciones de alta popularidad (19.9% recall) |
| SMOTE (próximo paso) | ~0.80+ | Se estima un recall del 45–60% para clase Alta |

</div>

---

## Hallazgos Clave

- 🎯 **La popularidad no depende de una sola variable de audio** — la fortaleza está en la *consistencia* de producción, no en valores extremos
- 💃 **Alta bailabilidad ≠ alta popularidad** — Soca (0.795 danceability) y Reggae (0.765) lideran en baile pero quedan en el tercio inferior de popularidad
- 🌍 **Afrobeats en expansión** — 5 artistas en el top 10 de volumen: Asake, Seyi Vibez, Bnxn, Wizkid y Burna Boy
- 📺 **Streaming y audiencia en vivo son métricas independientes** — ningún género lidera en ambas simultáneamente
- 🌿 **R&B lidera popularidad** con 76.2 puntos promedio pero solo 0.16 de liveness

---

## Casos Especiales — Impacto Post-Fallecimiento

<div align="center">

| Artista | Género | Pico de popularidad | Incremento | Estabilización |
|:---:|:---:|:---:|:---:|:---|
| **Juice WRLD** | Hip-Hop/Rap | Dic. 2019 | +24.5% | Por encima de línea base |
| **Avicii** | Electronic (EDM) | Abr. 2018 | **+45%** | 83–88 pts hasta 2024 |

> 🏆 Avicii registró el **impacto más pronunciado** de ambos casos. Su álbum póstumo *TIM* (2019) generó una recuperación visible, consolidando un legado permanente en la historia del EDM.

</div>

---

## Próximos Pasos

- [ ] Aplicar **SMOTE** para balancear clases y mejorar el recall
- [ ] Incorporar **XGBoost** para comparar con los modelos actuales
- [ ] Agregar **datos temporales reales** de streams en lugar de simulaciones
- [ ] Expandir el análisis a géneros emergentes como **Amapiano** y **Afrobeats** (2024–2025)

---

## Ejecutar en Google Colab

<div align="center">

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ZpWB1F8B9L_U3Yl0SJGMHOK7G-I1zyHI?usp=sharing)

</div>

1. Haz clic en el badge de arriba
2. Sube los archivos `high_popularity_spotify_data.csv` y `low_popularity_spotify_data.csv`
3. Ejecuta las celdas en orden (`Ctrl+F9`)

---

## Contacto

<div align="center">

| Plataforma | Enlace |
|:---:|:---|
| <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white"/> | [linkedin.com/in/kadir-barquet-bravo](https://www.linkedin.com/in/kadir-barquet-bravo/) |
| <img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white"/> | [github.com/Kadir011](https://github.com/Kadir011) |
| <img src="https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white"/> | [barquetbravokadir@gmail.com](mailto:barquetbravokadir@gmail.com) |

---

<sub>Desarrollado con ❤️ y 🎵 · Dataset: Spotify via Kaggle · Entorno: Google Colab</sub>

</div>
