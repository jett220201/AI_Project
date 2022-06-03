# Clasificación de residuos aprovechables y no aprovechables por KNN con adquisición de características por medio de momentos de Hu.

## Integrantes:
  - *Juan Esteban Torres Tamayo*
  - *Janner Arley Rosero Mora*

## Tabla de contenido:
  - Dataset
  - Desarrollo
  - Resultados
  - Conclusiones
  - Video
 
## Dataset
Para la implementación de este clasificador se elaboro un dataset de fotos de residuos solidos urbanos dentro de las instalaciones del campus de la Pontificia Universidad Javeriana sede Cali. Este dataset cuenta con 230 fotografías dentro de un ambiente con luminosidad controlada, de estas 230 fotos se cuenta con 95 de residuos aprovechables y 135 de residuos no aprovechables, donde se puede encontrar fotos de botellas de vidrio y plástico, envoltorios, servilletas, vasos de papel, cajas tetrapack, entre otros residuos. Estas fotografías pueden ser vistas aquí https://drive.google.com/drive/folders/1Juy3mwwbKxS25jGUhr4gWGNkdIkjnA0d?usp=sharing.


Para la construcción del dataset las imágenes fueron procesadas usando OpenCv en Python, de ellas se extrajeron 7 características correspondientes a los 7 momentos de Hu de cada fotografía.

En cuanto a las etiquetas, estas fotografías fueron etiquetadas manualmente siguiendo la Norma 2184 de 2019 del gobierno de Colombia para la clasificación de residuos. Pero este clasificador solo considera el caso binario, es decir, aprovechable o no aprovechable.

  - 1 -> Residuo Aprovechable
  - 0 -> Residuo No Aprovechable
 
 ## Desarrollo
 
Para el desarrollo de este clasificador se realizo una división del dataset, siendo 10% para evaluar el desempeño final y 90% para realizar entrenamiento y validación cruzada. Siguiendo el proceso se normalizan los datos usando un StandardScaler y se procede a reducir las dimensiones de los datos por medio de PCA, dando por solo 2 dimensiones correspondientes al 0.983631295 de los datos. 

Se hace uso del modelo K-Neighbors Classifier (KNN) para la clasificación de este proyecto. Para la optimización de los hiper parámetros del clasificador de uso el método GridSearch con validación cruzada (GridSearchCV), en el se iteraron los parámetros n_neighbors, metric y weights.
 
 ## Resultados
 
 Después de realizar el entrenamiento y optimización usando GridSearchCV se extrajo el mejor clasificador hallado usando F1 Score por métrica, obteniendo:
 
 ```
Best estimator: KNeighborsClassifier(metric='manhattan', n_neighbors=3)
with metrics: {'metric': 'manhattan', 'n_neighbors': 3, 'weights': 'uniform'} and score: 0.5377339045443461
```

Finalmente se calcula la métrica del Coeficiente de Correlación de Matthews (MCC):

```
MCC =  0.2196969696969697
```
 
 ## Conclusiones
 
 ## Video
 

