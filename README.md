# FaceRecognition
Face Recognition using Eigen Faces, LBP and LDA
This Project is a part of Visual Recognition Course.
## Objective
The main purpose of this project is to see how PCA, LDA and LBP performs in Face Recognition.
## Face Recognition
Face Recognition is different from face detection. In face recognition, we deal with the identity of the faces unlike face detection where our main aim remains at making a bounding box around the face. In this project we will use eigen faces techique for face recognition.
## Why not Neural Networks
Using fancy things do not solve problem everytime. For getting started with a project requirement analysis is a must do thing. Our requirement for this project is dataset. The dataset that we have collected from Univeristy Students isn't large enough to train neural networks. Also, if we go about training neural networks, we might face dimensional issues. With higher dimensions neural networks might cost much higher time to train. So lets start with dimensionality reduction. Dimensionality reduction techniques can be supervised as well as unsupervised. We will compare both techniques.
## PCA - Principal Component Analysis
An approach to collect dimensions with highest variance. In this project I have implemented PCA from scratch. Out of 4096 dimensions, 400 dimensions captured almost 95% of the variance. Now, projecting image onto these new 400 dimensions will give us eigen faces. Eigen faces are nothing but images with smaller dimensions which are principal axes. Finally, for obtaining classification report, Support Vector Machine is used as a classifier.

## LDA - Linear Discriminant Analysis
It is a supervised approach for dimensionality reduction. This approach choose those principal axes which helps in classification, i.e. it tries to choose those dimensions which discriminates between datapoints belonging to different classes. It basically maximizes scatter between different classes. Images obtained after projecting them on reduced dimensions are known as fisherfaces. 

## LBP - Local Binary Patterns
It is not necessary that the input we are getting for face recognition is face centered. So, to improve performance of our model, we first will crop image by using haar features present in frontalface.xml file of cascade classifier. This algorithm extracts facial characteristics from image. It sets binary value to all the neighbours of a pixel using a particular threshold value and concatenate them to get final result.

## Results
Performance of LBP was found to be better than PCA which performed again better than LDA. Cropping of facial region also contributed in making LBP perform best. The results are there in respective notebooks.
