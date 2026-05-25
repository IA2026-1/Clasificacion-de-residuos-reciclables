<img width="2048" height="768" alt="ChatGPT Image 25 may 2026, 03_29_28 p m" src="https://github.com/user-attachments/assets/07d32f1b-5098-4597-acc8-4e98968f6f48" />


MODELO DE VISIÓN ARTIFICIAL PARA LA CLASIFICACIÓN DE RESIDUOS
Autores: 
Juan Manuel Rivera Torres
Edwin David Gutierrez Olarte
Juan Pablo Ballesteros Macias 

Institución: Universidad Industrial de Santander Curso: Inteligencia Artificial I

Objetivo: Implementar un sistema de visión artificial capaz de identificar y clasificar automáticamente diversos tipos de residuos sólidos para optimizar los procesos de reciclaje y gestión ambiental.


Descripción del Dataset
El dataset utilizado consta de 7,010 imágenes de alta resolución organizadas en 5 categorías fundamentales para el reciclaje

-Cardboard (Cartón): Empaques y cajas.
-Glass (Vidrio): Botellas y recipientes transparentes/oscuros.
-Metal (Metal): Latas y residuos ferrosos.
-Paper (Papel): Hojas impresas y revistas.
-Plastic (Plástico): Envases PET y polímeros comunes.
-Link de descarga: https://www.kaggle.com/datasets/sumn2u/garbage-classification-v2 

Metodología y Pipeline de Desarrollo
El proyecto se dividió en fases críticas para cumplir con los estándares de investigación en IA:
A. Preparación y Exploración (EDA)
Se realizaron transformaciones avanzadas incluyendo Resize (128x128), normalización basada en ImageNet y codificación de etiquetas mediante LabelEncoder
-La exploración visual mediante mosaicos confirmó la variabilidad intra-clase del dataset.

B. Selección de Características y Reducción de Dimensionalidad
Selección Formal: Se aplicaron métodos de Feature Selection (SelectKBest) para identificar las variables más influyentes del vector de ResNet50, optimizando el tiempo de cómputo

Análisis Espacial: Se implementó PCA (reduciendo a 50 y 2 componentes) y t-SNE para visualizar la separabilidad de las clases. Los gráficos de t-SNE revelaron agrupaciones naturales claras para 'Metal' y 'Glass', y solapamientos menores entre 'Paper' y 'Cardboard'.

C. Exploración No Supervisada (Clustering)
Para validar la estructura natural de los datos, se implementaron:
-K-Means: Determinado mediante el Método del Codo (Elbow Method) para encontrar el K óptimo
-DBSCAN: Utilizado para identificar muestras anómalas (noise) en el dataset
-Clustering Jerárquico: Representación mediante dendrogramas para entender la jerarquía acústica de los materiales

4. Análisis de Viabilidad y Conclusiones
-Viabilidad Técnica: El sistema es altamente robusto, manteniendo un F1-Score superior a 0.90 en la mayoría de las clases, lo que permite su despliegue en entornos controlados de clasificación

-Viabilidad Comercial: La automatización de este proceso reduce costos operativos en plantas de reciclaje y minimiza la tasa de error humana en la segregación de materiales

-Trabajo Futuro: Implementación de modelos de detección de objetos en tiempo real (YOLO) para procesar múltiples residuos en una sola captura.


Modelos (Palabras Clave)
ResNet50, SVM, Random Forest, Decision Tree, Gaussian NB, MLP, PCA, t-SNE, SelectKBest, K-Means, DBSCAN, GridSearchCV


Enlaces del Proyecto
Código (Notebook): [ENLACE A COLAB/GITHUB]
Video de Sustentación: [ENLACE A YOUTUBE]
Repositorio Oficial: [ENLACE A ESTE GITHUB]
Para validar la estructura natural de los datos, se implementaron:
K-Means: Determinado mediante el Método del Codo (Elbow Method) para encontrar el K óptimo
.
DBSCAN: Utilizado para identificar muestras anómalas (noise) en el dataset
.
Clustering Jerárquico: Representación mediante dendrogramas para entender la jerarquía acústica de los materiales
