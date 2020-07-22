# Risky-Business
Classification

## Resampling

### Balanced Accuracy Score review

The Random Over Sampler (ROS) has the greatest Balanced Accuracy Score, but SMOTE and SMOTEENN are both within a few hundreths of a point. The Cluster Centroids is just above .5 so this would be the first model ruled out.

#### Balanced Accuracy Score: 
* Random Over Sampler = 0.65
* SMOTE = 0.64
* Cluster Centroids = 0.51
* SMOTEENN = 0.63

### Recall Score review

Both the ROS and SMOTE have the highest Recall Score. As with Bakanced Accuracy Score, Cluster Centroids is far below. SMOTEENN also has a low recall score. This leaves the two Oversampling models as the optional choices.

#### Recall Score:
* Random Over Sampler = 0.68
* SMOTE = 0.65
* Cluster Centroids = 0.41
* SMOTEENN = 0.55

### Geometric Mean Score review

Comparing the Geometric Mean Score, all models except the Cluster Centroids model are within a few hundreds of a point, but once again the ROS model has the highest score.

#### Geometric Mean Score:
* Random Over Sampler = 0.65
* SMOTE = 0.64
* Cluster Centroids = 0.50
* SMOTEENN = 0.63

When comparing the array of ROS and SMOTE, the differnce is 54/33 to 55/32, respectively. Since I believe it's better to book 1 less loan then to book a loan that's going to default, I'd prefer the SMOTE over ROS, but it's only a differnce of one high-risk loan.

## Ensemble Learning

### Balanced Accuracy Score review

Easy Ensemble Classifier model has the highest Balanced Accuracy Score. Altough the Balanced Random Forest Classifier is better than all the Resampling models.

#### Balanced Accuracy Score: 
* Balanced Random Forest Classifier = 0.79
* Easy Ensemble Classifier  = 0.93

### Recall Score review

The Recall Score is close for both Ensemble Learning models, but the Easy Ensemble Classifier model wins again.

#### Recall Score:
* Balanced Random Forest Classifier = 0.89
* Easy Ensemble Classifier  = 0.94

### Geometric Mean Score review

Once again the Easy Ensemble Classifier model has the highest score when comparing the Geometric Mean Score.

#### Geometric Mean Score:
* Balanced Random Forest Classifier = 0.78
* Easy Ensemble Classifier  = 0.93

### Top 3 Features review

The interested thing about the top 5 features and top 3 specifically is that thay are all related to a customer making payments on their mortgage. This might be concerning because it as if one value is being used multiple times. An individuals mortgage payment is always made up of Principal and Interest. The top three features are Payment, Principal and Interest.

#### Top 5 Features

* Payments received to date for portion of total amount funded by investors
* Principal received to date
* Interest received to date
* Payments received to date for total amount funded
* Last total payment amount received

## Conclusion

The Ensemble Learning models far outpreform the Resampling models. And, the Easy Ensemble Classifier far outperforms the Balanced Random Forest Classifier. Therefore I would recommend using the Easy Ensemble Classifier model.
