# fish-counting-system

This repository includes the code files developed for creating a fish counting system. 
The dataset used is not included here. 

The code files for the project consist of three files: crop images, fish object detection and fish classification. 

Crop images
- The crop images file takes in all the images from the dataset, containing multiple fish from a sea cage. 
- This file creates bounding boxes around ground-truth (manually) detected fish for all of those images. 
- Each bounding box is then cropped into a new image containing that single fish. 

Fish object detection
- The fish object detection file takes in all the images containing multiple fish from a sea cage, from the test set. 
- This file creates bounding boxes around automatically detected objects for all of those images, which has at least a 60% chance of being a fish. 
- Each bounding box is then cropped into a new image containing that single fish. 
- Each automatically detected fish is also compared to each ground-truth detected fish using Intersection over Union. 

Fish classification
- The fish classification file takes in cropped images of single fish created by the crop images file. 
- This file performs data preparation of the cropped images, CNN feature extraction, PCA dimensional reduction, grid search with perceptron, Adaline, SVC, KNN, and MLP, ensemble, and counting. 
- Different approaches is tested
- The counting part is using the best performed approach for classification as well as the cropped images of automatically detected fish from the fish object detection file. 
