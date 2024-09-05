# Proyecto: Clasificación de Imágenes: Perros vs Gatos usando CNN

Este notebook implementa un modelo de clasificación de imágenes para diferenciar entre perros y gatos utilizando Redes Neuronales Convolucionales (CNN). El modelo se entrena usando el popular conjunto de datos "Dogs vs Cats" proporcionado por Kaggle. El objetivo es construir una CNN que sea capaz de clasificar imágenes de manera eficiente, evaluando tanto su precisión como la pérdida durante el entrenamiento y la validación.

## Metodología

El flujo de trabajo comienza con la carga y preprocesamiento del conjunto de datos. Las imágenes son redimensionadas, normalizadas, y divididas en conjuntos de entrenamiento, validación y prueba. Posteriormente, se define una arquitectura de CNN que incluye varias capas convolucionales con activaciones ReLU, capas de pooling para la reducción de dimensionalidad y capas densas finales para la clasificación binaria. Se utiliza la función de pérdida `BinaryCrossentropy` junto con el optimizador `Adam` para la actualización de los pesos del modelo.

## Entrenamiento y Evaluación

El modelo se entrena sobre múltiples épocas, monitorizando el rendimiento en términos de precisión y pérdida tanto en el conjunto de entrenamiento como en el de validación. Durante el proceso, se aplican técnicas como *data augmentation* para mejorar la capacidad del modelo de generalizar a nuevas imágenes no vistas. Tras el entrenamiento, el rendimiento final se evalúa en el conjunto de prueba, proporcionando métricas detalladas de precisión y pérdida.

## Visualización de Resultados y Optimización de GPU

Además de las métricas cuantitativas, el notebook también incluye la visualización de curvas de aprendizaje para evaluar el comportamiento del modelo. Se emplea Google Colab para acelerar los tiempos de entrenamiento aprovechando la GPU disponible. También se hacen ajustes en el tamaño del lote (batch size) y el tamaño de las imágenes para optimizar el uso de memoria y recursos computacionales.
