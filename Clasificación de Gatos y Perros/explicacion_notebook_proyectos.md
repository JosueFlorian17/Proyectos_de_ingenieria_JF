# Proyecto: Clasificación de Imágenes: Perros vs Gatos usando CNN

Se implementará un modelo de clasificación de imágenes para diferenciar entre perros y gatos utilizando Redes Neuronales Convolucionales (CNN). El modelo se entrena usando el dataset "Dogs vs Cats Small" que encontramos en la plataforma de Kaggle. El objetivo es construir una CNN que sea capaz de clasificar imágenes de manera eficiente, evaluando tanto su precisión como la pérdida durante el entrenamiento y la validación.

## Metodología

Comenzamos con la descarga y actualización de librerías de Keras actualizadas al año 2024, pues el notebook de ejemplo cuenta con código del año 2017, con las librerías desactualizadas. Las imágenes son redimensionadas, normalizadas, y aprovechamos las carpetas incluídas de conjuntos de entrenamiento, validación y prueba. Posteriormente, se define una arquitectura de CNN que incluye varias capas convolucionales con activaciones ReLU, capas de pooling para la reducción de dimensionalidad y capas densas finales para la clasificación binaria. Se utiliza la función de pérdida `BinaryCrossentropy` junto con el optimizador `Adam` para la actualización de los pesos del modelo.

## Entrenamiento y Evaluación

El modelo se entrena sobre múltiples épocas (20 y 60), monitorizando el rendimiento. Durante el proceso, se aplican técnicas como *data augmentation* para mejorar la capacidad del modelo de generalizar a nuevas imágenes no vistas. Tras el entrenamiento, el rendimiento final se evalúa en el conjunto de prueba, proporcionando métricas detalladas de precisión y pérdida.

## Visualización de Resultados y Optimización de GPU

Además de las métricas cuantitativas, también incluye la visualización de curvas de aprendizaje para evaluar el comportamiento del modelo. Uno de los errores que encontré durante el desarrollo, fue el uso y agotamiento de la memoria de GPU ofrecida por google colab, por falta de optimización en alguno de los procesos de la red neuronal, luego de defirnir más limitaciones y funciones, se obtuvo un resultado esperado
