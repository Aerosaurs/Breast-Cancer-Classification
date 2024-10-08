# Breast cancer diagnosis using statistical techniques in Python (Random forest, Support vector, XGBoost)
Author : Hritik P.

# Problem Statment
Breast cancer remains a significant global health concern, and timely and accurate diagnosis plays a pivotal role in determining treatment plans and patient outcomes. Traditional diagnostic methods often involve manual examination and interpretation, which can lead to variability and subjective judgments. This project aims to harness the power of advanced statistical techniques, including Random Forest, Support Vector Machines (SVM), and XGBoost, to create a robust and objective breast cancer diagnostic model using Python.

# Data Set used 
https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

# ML models and Results
- includes application of Grid Search, SMOTE sampling, and visualization using principal component analysis
- data used is from UCI Machine Learning Repository 

For most models, k-fold cross validation was performed with grid search to find optimal model parameters. 

 <p float="left">
 <img src=https://cdn-images-1.medium.com/max/1600/1*rgba1BIOUys7wQcXcL4U5A.png width=400 float="left"/>
 <img src=https://cdn-images-1.medium.com/max/1600/1*9CwvAqj99xcPDgQkCdm47w.png width=400 float="left"/>
 </p>
        


## XGBoost
XGBoost, or extreme gradient boosting, is a top machine learning model and the dominating algorithm among competitions.
- supports many tunings parameters such as learning rate and early stopping 
- as a tree boosting algorithm, minimal data-preprocessing is needed (i.e. data normalization/scaling)

#### Test accuracy achieved with XGBoost
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/xgboost_accuracy.png width=400/>

 #### Example tree 
  <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/xgboost_tree.png width=400/>

#### Feature importance

 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/xgboost_feature_importance.png width=400/>

#### Training/validation error

 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/xgboost_error.png width=400/>
 
#### Training/validation loss
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/xgboost_loss.png width=400/>


## Random Forest Classifier
- RFC utilizes multiple decision trees and averages between them to make predictions
- again, as a tree based model, RFC requires minimal data preprocessing

#### Test accuracy achieved with RFC
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/randomforest_accuracy.png width=400/>
 
 #### Example tree
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/randomforest_tree.png width=400/>


## Support Vector Machine 
- note PCA was used to bring dimensionality down to 2 in order to plot the hyperplane
- support vector machines classifies models by finding a hyperplane to separate classes while maximizing the margin distance from the classes
- as a distance based method, SVM requires data normalization to ensure no features take precendence over others
#### Accuracy achieved with SVM
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/svm_accuracy.png width=400/> 
 
#### Linear decision boundary
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/linear.png width=400/>
 
#### Radial basis function decision boundary
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/rbf.png width=400/>
 
 
## K-Neighbours 
- again, PCA was used to bring dimensionality down to 2 for plotting purposes
#### Accuracy achieved with KNC
<img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/kneighors_accuracy.png width=400/>

#### Nearest neighbours classification plot
<img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/kneighbors_plot.png width=400/>

 
## Deep Learning
- simple deep learning model used with residual connections similar to Resnet v1 to ensure "deep" networks train, at a minimum, as well as "shallow" networks
- the goal of deep learning is to calculate weights and biases within the network using gradients and error functions
#### Model
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/model.png width=400/> 

#### Oversampled results
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/oversampled_accuracy.png width=400/> 
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/oversampled_loss.png width=400/> 
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/oversampled_results.png width=400/> 


#### Non-oversampled results
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/nonoversampled_accuracy.png width=400/> 
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/nonoversampled_loss.png width=400/> 
 <img src=https://github.com/kwantommy/breast-cancer-diagnosis/blob/master/images/nonoversampled_results.png width=400/> 
