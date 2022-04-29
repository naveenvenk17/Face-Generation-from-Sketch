# Face Sketch to Image Generation using GAN

This repository contains the code for implementing an image generation system using GAN (Generative Adversarial Networks) to turn face sketches into realistic photos. 

![pred1](https://user-images.githubusercontent.com/81929600/166057437-e5724864-daa0-42c0-9fcb-9dfdd8b2de2c.jpeg)



### Contents
* [Getting started](#install-requirements)
* [Data Augmentation](#data-augmentation)
* [Training](#training)
* [Performance Measurement](#performance-measurement)
* [Testing](#testing)
* [References](#references)

## Install requirements
```
pip install -r requirements.txt
```

##### Keras-contrib installation
-  Run the below command to copy the source code locally (Assuming git is installed)
https://www.github.com/keras-team/keras-contrib.git
- cd keras-contrib
- python setup.py install

Or you can refer to this link https://medium.com/@kegui/how-to-install-keras-contrib-7b75334ab742

## Data Augmentation
 - The dataset consists 100 pairs faces and sketches. 88 pairs were chosen for training set.
 - Each pair is augmented to 200 pairs of face and sketch using transformation, rotation and shearing.
 - Do Data Augmentation with this [notebook](https://github.com/naveenvenk17/Face-Generation-from-Sketch/blob/main/Data%20Augmentation.ipynb)

## GAN
 - The GAN model architecture involves two sub-models: a generator model for generating new examples and a discriminator model for classifying whether generated examples are real, from the domain, or fake, generated by the generator model.

 - GAN model consists of Generator model with 50 layers and Adversary Model with 9 layers.

## Training

 - Start training GAN model with this [notebook](https://github.com/naveenvenk17/Face-Generation-from-Sketch/blob/main/GAN.ipynb)
 - Trained our model for 82 epochs

## Model Prediction after 
 
 -  1 epoch : 

![plot_000001](https://user-images.githubusercontent.com/81929600/166057574-05df5aba-991a-4752-862d-80c59799f038.png)


 -  10 epoch : 

![plot_000010](https://user-images.githubusercontent.com/81929600/166057595-2b1ae3b3-d838-4dc5-8742-9e3bcaf4f9ec.png)


 - 25 epoch : 

![plot_000025](https://user-images.githubusercontent.com/81929600/166057612-35dcc005-788d-472f-aa35-f98b820267d3.png)

 -  50 epoch : 
 
![plot_000050](https://user-images.githubusercontent.com/81929600/166057626-ad2cd34a-1670-432c-8ebd-fe976da68a69.png)


 -  82 epoch : 

![plot_000082](https://user-images.githubusercontent.com/81929600/166057641-28b5cc54-2a70-4749-b1e1-e308bf832331.png)

<p align="center">
  <img width="300" height="300" src="https://user-images.githubusercontent.com/81929600/166057641-28b5cc54-2a70-4749-b1e1-e308bf832331.png">
</p>


## Performance Measurement
 - SSIM (Structural Similarity Index) is used for measuring the similarity between two images.
 - Calculate SSIM and Verification Accuracy (L2-norm) using this [notebook](https://github.com/naveenvenk17/Face-Generation-from-Sketch/blob/main/Compute%20SSIM%20and%20L2-norm.ipynb)

## Testing
Generate single image with this [notebook](https://github.com/naveenvenk17/Face-Generation-from-Sketch/blob/main/Testing.ipynb)

## References
<a id="1">[1]</a> 
X. Wang and X. Tang. (2009).
Face Photo-Sketch Synthesis and Recognition. 
IEEE Transactions on Pattern Analysis and Machine Intelligence (PAMI), 31(11), 1955-1967.

<a id="2">[2]</a>
W. Zhang, X. Wang and X. Tang. (2011).
Coupled Information-Theoretic Encoding for Face Photo-Sketch Recognition.
Proceedings of IEEE Conference on Computer Vision and Pattern Recognition (CVPR).

<a id="3">[3]</a>
https://github.com/Malikanhar/Face-Sketch-to-Image-Generation-using-GAN
