# Classification of usable and non-usable waste by KNN with acquisition of characteristics through Hu moments.

## By:
  - *Juan Esteban Torres Tamayo*
  - *Janner Arley Rosero Mora*

## Content:
  - Dataset
  - Development
  - Results
  - Conclusions
  - Video
 
## Dataset
For the implementation of this classifier, a dataset of photos of urban solid waste within the campus of the Pontificia Universidad Javeriana Cali was developed. This dataset has 230 photographs in an environment with controlled lighting, of these 230 photos there are 95 of usable waste and 135 of non-usable waste, where you can find photos of glass and plastic bottles, wrappers, napkins, paper cups, tetrapack boxes, among other waste. These photographs can be seen here https://drive.google.com/drive/folders/1Juy3mwwbKxS25jGUhr4gWGNkdIkjnA0d?usp=sharing.


For the construction of the dataset, the images were processed using OpenCv in Python, from which 7 features corresponding to the 7 Hu moments of each photograph were extracted.

As for the labels, these photographs were manually labeled following the Colombian government's Standard 2184 of 2019 for waste classification. But this classifier only considers the binary case, i.e. usable or not usable.

  - 1 -> Usable
  - 0 -> Not Usable
 
 ## Development
 
For the development of this classifier a division of the dataset was performed, being 10% to evaluate the final performance and 90% to perform training and cross validation. Following the process, the data is normalized using a StandardScaler and the data dimensions are reduced by means of PCA, giving only 2 dimensions corresponding to 0.983631295 of the data. 

The K-Neighbors Classifier (KNN) model is used for the classification of this project. For the optimization of the hyper parameters of the classifier, the GridSearch method with cross validation (GridSearchCV) was used, in which the parameters n_neighbors, metric and weights were iterated.
 
 ## Results
 
 After performing the training and optimization using GridSearchCV, the best classifier found using F1 Score per metric was extracted, obtaining:
 
 ```
Best estimator: KNeighborsClassifier(metric='manhattan', n_neighbors=3)
with metrics: {'metric': 'manhattan', 'n_neighbors': 3, 'weights': 'uniform'} and score: 0.5377339045443461
```

Finally, the Matthews Correlation Coefficient (MCC) metric is calculated:

```
MCC =  0.2196969696969697
```
 
 ## Conclusions
 
After the execution of the present project, several considerations came to light, since we have our own dataset to which the abstraction of features by the authors using Hu's moments is done in the same way, it has been noted that these features do not form a sufficiently robust Dataset to generate a classifier since the best results obtained are not even close to 50%, this is perhaps due to several factors such as the imbalance of classes, the reduced number of samples from which the features were abstracted or perhaps the very nature of the objects to be classified. On the other hand, it is highlighted that although a systematic process was followed for the processing of the generated Dataset, the dubious quality of this is the factor that defined the overall performance of the classifier and therefore it is concluded that in future works the process of feature abstraction should be changed or improved in case of generating a Dataset of its own starting from the samples currently used.
 
 ## Video
 
 https://youtu.be/cNHl97oLwv0

