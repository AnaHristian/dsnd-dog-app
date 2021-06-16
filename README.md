## Project Motivation
This project walks you through one of the most popular Udacity projects across machine learning and artificial intelligence nanodegree programs. The goal is to classify images of dogs according to their breed.

## Required Libraries
* Machine, deep learning libraries: PyTorch, scikit-learn, OpenCV;
* Data analysis libraries: NumPy, pandas;
* Data visualization: Matplotlib, Pillow;

## Files Description
* `dog-app.ipynb`: a Jupyter Notebook where you can find the development of the algorithm that will estimate the dog’s breed, given an image of a dog. And, if you provide an image of a human, it will provide an estimate of the dog breed that is most resembling;
* `dog-app.html`: for easier preview, I included also the html format of our dog-app;
* Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip)
* Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip)
* You can also use you own images to test the app and there are some images provided for you in the img folder

## Results
* Creating a CNN to classify dog breeds from scratch doesn’t give great accuracy. After training my from scratch model for 50 epochs I did get an accuracy of 26%. Not that great and did take some time to train.
* On the other hand, using transfer learning to create a CNN that can identify dog breeds from images proved to be more consistent with our task. I used a pre-trained densenet121 model, freezed its parameters and reshaped the final layer to have the same number of outputs as the number of classes from our dataset. Trained the model only for three epochs and got an 81% accuracy. This is a great improvement which let us use this model for our app.
The model does a pretty good job at classifying dog breeds and gives a human a funny dog breed estimator but there are ways to improve our algorithm.
* We can finetune the transfer model to obtain higher accuracy on the dog breed classifier.
  - We can add more real-world images in our dataset for the model to train and improve performance.
  - We can add more data augmentation transforms so that the model sees variation of the input images.

## Acknowledgements
In developing this dog-app project also helped the Deep Learning Nanodegree Program from Udacity.
