# Malaria Classifier from Cell Image

## Project Overview

Repository for the Malaria Classifier Project

- Developed an classifier to identify if a given cell is uninfected or parasitised by malaria based on an image of the cell.
- Utilised the Malaria dataset from the Tensorflow Datasets package.
- Constructed tensors representing the cell images
- Trained a Deep Learning model using containing dense and convolutional neural network layers
- Accuracy on test set: 0.9608

## Codes and Resources Used

**Python Version:** 3.9

**Packages:** tensorflow, numpy, sklearn, matplotlip, seaborn

**Web Framework Requirements:** ```pip install -r requirements.txt```

**Scissors-paper-stone Classifier:** https://github.com/KeithGalli/neural-nets 

**Malaria Classifier:** https://www.kaggle.com/amyjang/tensorflow-image-classification-with-malaria-tfds

**Saving Numpy Files:** https://machinelearningmastery.com/how-to-save-a-numpy-array-to-file-for-machine-learning/ 

## Data Preperation

Although the dataset contained 27,558 cell images, I used only 25% of the images for training, 5% for validating and 5% for testing. This is due to hardware and time limitation. 

                    Number of training images: 6890

                    Number of validating images: 1377

                    Number of testing images: 1378

Inspecting the images, I noticed that the images are not of the same size. I padded and reshaped the data to standardise the image size for our model. I also rebuilt the tensor to fit the model.

## Model Building

Firstly, I created a basic model to act as our baseline. The basic model performed poorly, with only 0.556 accuracy on the training set. 

Next, I built a complex model consisting of both dense and convolutional neural network layers. I included callbacks into the model too: 

- Model Checkpoint: to save our best performing model for reusability
- Early Stopping: to stop the training once no more improvements are recorded, preventing overfitting and saving time.

## Model Performance

The model conducted 14 epochs during training. Upon completion, here are the results:

### Accuracy

                Training: 0.9573

                Validating: 0.9550

                Testing: 0.9608

### Loss

                Training: 0.1350

                Validating: 0.1296

                Testing: 0.1296

