# Lung Cancer detection using Deep Learning
 This is an attempt for Kaggle-Data-Science Bowl 2017, for solving this data from LUNA16 Grand Challenge was also used
1. 'data' folder must contain data from Kaggle Challenge, if using sample dataset, then there must be 19 patients
2. 'subset0' folder contains data from first subset of LUNA16 dataset
3. 'CSVFILES/annotations.csv' contains information about the location of nodules in LUNA16 dataset
4. nodules_2 folder contains the training-data of nodule-detector

### Used 2 methods

## 1. Directly feeding to the network
Uses stage1_labels.csv and dataset of the patients must be in data folder
Filename: Simple-cnn-direct-images.ipynb

## 2.1 Train a nodule classifier 
This part works in LUNA16 dataset. Uses segmentation_LUNA.ipynb, this notebook saves slices from LUNA16 dataset (subset0 here) and stores in 'nodule_2' folder. The data is to be manually split into training and validation. 
Then the notebook trains a network and saves the model by the name 'model.h5'

## 2.2 Get nodule-probabilities for each region in a Kaggle image
The notebook used is 'get_nodule_vector.ipynb'

## 2.3 Train a network to classify based on above obtained vector, that a person has cancer-or-not
The notebook used is SimpleNetwork.ipynb