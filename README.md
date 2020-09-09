# Multi-Lable classification with Classifier Chain of Artificial Neural Network

## Abstract
Multi-label classification is a generalization of
a multi-class classification problem where one entity can
belong to more than one class from the class set. Recent
works have proposed multiple methods of solving this
problem that involves both statistical and deep learning
methods. While methods exist for using deep learning
models for this problem, most of them require the model
to have a high dimension output vector and the property
of inter-dependency of classes has not been explored. An
ensemble of statistical models called the chain classifiers
can be used to address these issues. This study explores
methods of using neural network classifiers in the classifier
chain model and tries to address some problems with such
architecture while compare their performance on different
types of data using different metrics with each other
and with other well performing multi-label classification
methods.

## Basic ANN based CC Architecture
This model requires feeding the output node of the NN for lable one to the input vector of the NN for the next lable, 
thus considering the dependency. <br>
<p align="center">
<img src = "https://github.com/SAint7579/TY-Seminar-ChainClassifiers/blob/master/Images/basic_chain.PNG"></img>
</p>


<p align="center">
<img src = "https://github.com/SAint7579/TY-Seminar-ChainClassifiers/blob/master/Images/yeast_result.PNG"></img>
</p>
<h3 align="center"> Results of Basic ANN Chain (CC-ANN) on Yeast Dataset </h3>

<br>

## Bi-Directional chain classifiers
A simple chain architecture doesn't consider the direction of considering dependency. The lable Kn will have the output from lables 
K1 to Kn-1 in consideration whereas the first lable K1 will have none. Therefore, bidirectional chains create chains in both the directions
and ensemble thier results to get a more accurate prediction.<br>
<p align="center">
<img src = "https://github.com/SAint7579/TY-Seminar-ChainClassifiers/blob/master/Images/bdchain.PNG"></img>
</p>

## Transfering weights in a Chain Classifier
Training a neural nets based CC can be taxing. However, using the fact that the middle layer weights in subsequent classifiers of a
chain has almost similar weights, we can transfer the weights from the first classifer to the following ones in order to reduce the number 
of total nodes requiring backpropagation. 
<p align="center">
<img src = "https://github.com/SAint7579/TY-Seminar-ChainClassifiers/blob/master/Images/transferchains.PNG"></img>
</p>
<br><br>
