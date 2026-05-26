# ♻️ Modelo de Visión Artificial para la Clasificación de Residuos

<img width="2048" height="768" alt="banner" src="https://github.com/user-attachments/assets/7aab1576-3d68-40d4-b265-300982cba92d" />


---

#  Autores

- Juan Manuel Rivera Torres  
- Edwin David Gutierrez Olarte  
- Juan Pablo Ballesteros Macias  

---

#  Institución

**Universidad Industrial de Santander (UIS)**  
**Curso:** Inteligencia Artificial I

---

#  Objetivo del Proyecto

Desarrollar un sistema de visión artificial capaz de automatizar la clasificación de residuos sólidos domésticos mediante técnicas de inteligencia artificial, con el fin de mejorar la eficiencia en la separación y recuperación de materiales reciclables.

---

# 📌 Resumen Ejecutivo

Este proyecto implementa un pipeline robusto de Machine Learning y Deep Learning para clasificar automáticamente residuos reciclables en cinco categorías fundamentales.

##  Modelo Campeón
- **SVM (Kernel RBF)**  
- **Accuracy:** 90.58%

##  Dataset
- 7,010 imágenes procesadas mediante técnicas de visión artificial.

##  Estrategia Implementada
Se utilizó un enfoque híbrido que combina:

- Transfer Learning con **ResNet50**
- Descriptores manuales
- Selección de características
- Optimización de hiperparámetros

---

#  Descripción del Dataset

El dataset utilizado contiene aproximadamente **7,010 imágenes** distribuidas en cinco clases esenciales para procesos de reciclaje y economía circular.

| Categoría | Descripción |
|---|---|
| 📦 Cardboard | Cartón, cajas y empaques |
| 🍾 Glass | Botellas y recipientes de vidrio |
| 🥫 Metal | Latas y residuos metálicos |
| 📄 Paper | Hojas, revistas y papel |
| 🧴 Plastic | Envases PET y plásticos comunes |

## 🔗 Dataset
https://www.kaggle.com/datasets/sumn2u/garbage-classification-v2

---

#  Pipeline de Desarrollo y Metodología

El desarrollo del proyecto siguió un enfoque estructurado dividido en varias etapas técnicas.

---

#  A. Preparación y Exploración de Datos (EDA)

##  Exploración Visual
Se realizó una inspección visual completa de las cinco categorías mediante mosaicos de imágenes, permitiendo identificar:

- Variabilidad de iluminación
- Diferencias de textura
- Cambios de orientación
- Diversidad intra-clase

##  Preprocesamiento

Se aplicaron técnicas de preparación de datos como:

- Redimensionamiento a **128x128 píxeles**
- Normalización estadística basada en **ImageNet**
- Codificación de etiquetas mediante **LabelEncoder**

Estas transformaciones permitieron estandarizar la entrada para los modelos de aprendizaje automático.

---

#  B. Ingeniería y Selección de Características

##  Extracción de Características

Se compararon dos enfoques principales:

###  Transfer Learning
Utilizando:

- **ResNet50**
- 2,048 características profundas

###  Descriptores Manuales
Implementando:

- HOG
- LBP
- Histogramas de Color

Generando aproximadamente:

- 8,260 características

##  Resultado Comparativo

El enfoque basado en **Transfer Learning** obtuvo un rendimiento superior, alcanzando aproximadamente:

- **+20% de mejora en Accuracy**

frente a los descriptores manuales.

---

##  Selección Formal de Características

Se implementó:

- **SelectKBest (ANOVA F-score)**

para seleccionar las **200 características más relevantes**, logrando:

- Reducción del costo computacional
- Mayor velocidad de entrenamiento
- Conservación del poder predictivo

---

#  C. Reducción de Dimensionalidad

##  PCA (Principal Component Analysis)

Se redujo el espacio de características a:

- **344 componentes**

manteniendo:

- **93% de la varianza acumulada**

---

##  t-SNE

Se utilizó para generar visualizaciones espaciales en 2D y analizar la separabilidad entre clases.

###  Hallazgos

- Las clases **Metal** y **Glass** mostraron agrupaciones claramente definidas.
- Se observó cierto solapamiento entre **Paper** y **Cardboard** debido a similitudes visuales.

---

#  D. Exploración No Supervisada (Clustering)

Con el objetivo de validar la estructura natural del dataset se implementaron diferentes algoritmos de clustering.

---

##  K-Means

Se aplicaron:

- Método del Codo (Elbow Method)
- Coeficiente Silhouette

Esto permitió identificar un número óptimo de clusters alineado con las etiquetas reales.

---

##  DBSCAN

Utilizado para:

- Detección de ruido
- Identificación de muestras atípicas
- Agrupaciones densas

---

##  Clustering Jerárquico

Se construyeron:

- Dendrogramas
- Enlace Ward

permitiendo analizar relaciones jerárquicas entre materiales reciclables.

---

#  Resultados Supervisados y Optimización

Se evaluaron múltiples modelos de clasificación utilizando:

- Validación Cruzada Estratificada (5-Fold)
- GridSearchCV para optimización de hiperparámetros

---

##  Resultados de Modelos

| Modelo | Accuracy |
|---|---|
| 🏆 SVM (RBF) | **90.58%** |
| 🌲 Random Forest | 85.45% |
| 🧠 Deep MLP | 90.23% |
| 📈 Gaussian Naive Bayes | 76.03% |

---

#  Análisis de Viabilidad

##  Viabilidad Técnica

El modelo presenta un alto rendimiento en entornos de procesamiento acelerado con GPU, especialmente en la identificación de:

- Vidrio
- Metal

las cuales fueron las categorías con menor nivel de confusión.

---

##  Viabilidad Comercial

La automatización de clasificación de residuos permite:

- Reducir contaminación cruzada
- Incrementar la pureza del material reciclado
- Optimizar procesos industriales
- Disminuir errores humanos

---

#  Trabajo Futuro

Como trabajo futuro se plantea:

- Implementar modelos de detección de objetos en tiempo real
- Integrar arquitecturas como **YOLO**
- Procesar múltiples residuos simultáneamente mediante video en vivo

---

#  Tecnologías y Herramientas Utilizadas

- Python
- TensorFlow
- Scikit-Learn
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Seaborn

---

#  Modelos y Técnicas Implementadas

- ResNet50
- SVM
- Random Forest
- Decision Tree
- Gaussian NB
- MLP
- PCA
- t-SNE
- SelectKBest
- GridSearchCV
- K-Means
- DBSCAN

---


# 🔗 Enlaces del Proyecto


##  Video de Sustentación
[INSERTAR LINK A YOUTUBE]


---

#  Impacto Ambiental

Este proyecto busca contribuir al desarrollo de soluciones inteligentes para:

- Gestión sostenible de residuos
- Automatización ecológica
- Optimización del reciclaje
- Reducción del impacto ambiental
- Implementación de ciudades inteligentes

---

#  Licencia

Proyecto desarrollado con fines académicos para la asignatura **Inteligencia Artificial I** de la Universidad Industrial de Santander.
