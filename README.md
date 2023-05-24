# deteccion_leucemia
Algoritmo red neuronal convolucional para detección sospecha leucemia en células de sangre
Este repositorio contiene el código del proyecto para detectar en imágenes de células sanguíneas la sospecha de presencia de cáncer (leucemia ALL).

## Tabla de contenidos
- Dataset
- Modelo
- Resultados

## Dataset

El conjunto de datos consiste en imágenes de células de sangre 7172 con sospecha de leucemia y 3389 normales ( sin cáncer) obtenido del repositorio de Kaggle https://www.kaggle.com/datasets/andrewmvd/leukemia-classification


## Modelo
Se realizó dos arquitecturas de redes neuronales convolucionales:
-La diferencia principal entre cada una de ellas radica en el tipo de regularización.
-Se entrenó cada uno de los modelos con dos datasets de 3000 imágenes diferentes, obteniendo así 4 estructuras diferentes,
- Se realizó la evaluación con la aplicación de un dataset diferente al aplicado en el proceso de train y la puesta en producción del modelo con mejor performance con un conjunto de imágenes nuevo.

## Resultados modelo puesto en producción
|Métrica    | Modelo 1     | 
|--------------|-----------|
| Acc Train |   88,8%    |       
| Acc Validation    | 84,3% |      
| Acc Test   | 87,8% |      
| Recall   | 98% |      

Se evaluó el performance del modelo mediante métricas de accuracy en el entrenamiento. Adicional se evaluó la métrica de Recall en el testeo de las imágenes al ser un tema médico, se priorizó la detección de casos positivos que realmente son positivos.
