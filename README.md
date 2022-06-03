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
 
 
 
 ## Resultados
 
 
 ## Conclusiones
 
 ## Video
 

