# faceswap-playground

This repo has been opened for users playing with the project. 

Sadly the project is not yet ready to use for non technical people, it will improve over time, so check for updates regularly and discuss with other. 

## What can you do here?
 - Discuss here about your experience of the project
 - Help people having trouble running it
 - Add guidelines and help for newcomers
 - Share data/models

**If you are a more experienced user** you can help by proposing solutions for a better user-experience. Ideally, the goal is to get to a release that can be used to non technical people.

## Quick start
Get the code from the main 'faceswap' repo and set it up (setup section below)

The project has multiple entry points. You will have to:
 - Gather photos (or use the one provided in the training data provided below)
 - **Extract** faces from your raw photos
 - **Train** a model on your photos (or use the one provided in the training data provided below)
 - **Convert** your sources with the model

### Extract
From your setup folder, run `python extract.py`. This will take photos from `src` folder and extract faces into `extract` folder.

### Train
From your setup folder, run `python train.py`. This will take photos from `data/trump` and `data/cage` folder and train a model that will be saved inside the `models` folder.

### Convert
From your setup folder, run `python convert_photo.py`. This will take photos from `original` folder and apply new faces into `modified` folder.

Note: there is no conversion for video yet. You can use MJPG to convert video into photos,, process images, and convert images back to video

## Training Data  
**Whole project with training images and trained model (~300MB):**  
https://anonfile.com/p7w3m0d5be/face-swap.zip or [click here to download](https://anonfile.com/p7w3m0d5be/face-swap.zip)

## How To setup and run the project

### Setup
Clone the repo and setup you environment. There is a Dockerfile that should kickstart you. Otherwise you can setup things manually, see in the Dockerfiles for dependencies

**Main Requirements:**
    Python 3
    Opencv 3
    Tensorflow 1.3+(?)
    Keras 2

You also need a modern GPU with CUDA support for best performance

**Some tips:**

Reuse existing models will train much faster than start from nothing.  
If there are not enough training data, start with someone looks similar, then switch the data.
