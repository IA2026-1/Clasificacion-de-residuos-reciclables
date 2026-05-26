<img width="2048" height="768" alt="banner" src="https://github.com/user-attachments/assets/7aab1576-3d68-40d4-b265-300982cba92d" />

---

#  Modelo de Visión Artificial para la Clasificación de Residuos


---

# Autores

- Juan Manuel Rivera Torres  
- Edwin David Gutierrez Olarte  
- Juan Pablo Ballesteros Macias  

---

# Universidad

**Universidad Industrial de Santander (UIS)**  
**Curso:** Inteligencia Artificial I

---

# 📌 Descripción del Proyecto

Este proyecto desarrolla un sistema de visión artificial basado en técnicas de Machine Learning y Deep Learning capaz de identificar y clasificar automáticamente diferentes tipos de residuos reciclables.

El propósito principal es optimizar los procesos de reciclaje mediante automatización inteligente, reduciendo errores humanos y facilitando la separación eficiente de materiales.

---

#  Objetivo General

Implementar un modelo de visión artificial capaz de reconocer y clasificar residuos sólidos reciclables para mejorar los procesos de gestión ambiental y reciclaje automatizado.

---

# 🗂️ Dataset Utilizado

El dataset utilizado contiene aproximadamente **7,010 imágenes** distribuidas en cinco categorías principales de residuos reciclables.

## 📦 Categorías

| Categoría | Descripción |
|---|---|
| Cardboard | Cartón, cajas y empaques |
| Glass | Botellas y recipientes de vidrio |
| Metal | Latas y residuos metálicos |
| Paper | Hojas, revistas y papel |
| Plastic | Envases PET y plásticos comunes |

## 🔗 Dataset
https://www.kaggle.com/datasets/sumn2u/garbage-classification-v2

---

# ⚙️ Metodología y Pipeline de Desarrollo

El proyecto se desarrolló en varias fases fundamentales para garantizar un análisis robusto y resultados confiables.

---

#  1. Preparación y Exploración de Datos (EDA)

Durante esta etapa se realizaron procesos de:

- Redimensionamiento de imágenes a **128x128 píxeles**
- Normalización basada en ImageNet
- Codificación de etiquetas mediante LabelEncoder
- Exploración visual mediante mosaicos de imágenes

Estas técnicas permitieron mejorar la calidad del dataset y analizar la variabilidad entre clases.

---

# 2. Extracción de Características y Reducción de Dimensionalidad

##  Extracción de Características

Se utilizó **ResNet50** como extractor de características profundas para obtener representaciones robustas de las imágenes.

##  Selección de Características

Se implementó:

- SelectKBest

Con el objetivo de identificar las características más relevantes y reducir el costo computacional.

##  Reducción de Dimensionalidad

Se aplicaron técnicas como:

- PCA
- t-SNE

Estas técnicas permitieron visualizar la distribución espacial de las clases y analizar su separabilidad.

###  Observaciones

- Las clases **Metal** y **Glass** mostraron agrupaciones claramente definidas.
- Se observó cierto solapamiento entre **Paper** y **Cardboard** debido a similitudes visuales.

---

# 🔍 3. Aprendizaje No Supervisado (Clustering)

Con el objetivo de validar la estructura natural del dataset se implementaron distintos algoritmos de clustering.

## K-Means

- Aplicación del Método del Codo (Elbow Method)
- Determinación del número óptimo de clusters

## DBSCAN

- Identificación de datos atípicos (*noise*)
- Detección de agrupaciones densas

##  Clustering Jerárquico

- Construcción de dendrogramas
- Análisis de relaciones jerárquicas entre materiales

---

#  Modelos Implementados

Durante el desarrollo del proyecto se evaluaron diferentes algoritmos de clasificación y análisis:

- ResNet50
- SVM
- Random Forest
- Decision Tree
- Gaussian Naive Bayes
- MLP (Multi-Layer Perceptron)
- PCA
- t-SNE
- SelectKBest
- K-Means
- DBSCAN
- GridSearchCV

---

#  Resultados

El sistema logró un desempeño sólido en la clasificación de residuos reciclables.

##  Rendimiento

- F1-Score superior a **0.90** en la mayoría de las categorías.
- Alta capacidad de generalización en entornos controlados.
- Reducción significativa de errores de clasificación.

---

# Trabajo Futuro

Como mejora futura del proyecto se propone:

- Implementar modelos de detección de objetos en tiempo real.
- Integrar arquitecturas como **YOLO**.
- Clasificar múltiples residuos simultáneamente mediante video en vivo.

---

# 📂 Estructura del Proyecto

```bash
📁 Proyecto-IA-Residuos
│
├── 📁 dataset
├── 📁 notebooks
├── 📁 modelos
├── 📁 resultados
├── 📁 imagenes
├── 📄 README.md
├── 📄 requirements.txt
└── 📄 LICENSE
