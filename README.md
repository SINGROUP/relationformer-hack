# Structure discovery through Image-to-Graph machine learning model

![](https://cdn.jsdelivr.net/gh/HuangJiaLian/DataBase0@master/uPic/2024-12-17-19-30-Hello.png)

## Introduction

Atomic Force Microscopy (AFM) is critical for the characterization of atomic-scale nanos-
tructures. However, finding the structure from AFM images is not an easy task, which need lots of human experience. Simulations, especially with Particle Probe AFM (PPAFM), provide a cost-effective means for rapid image generation. Using state-of-the-art machine learning models and substantial
PPAFM-generated datasets, properties like molecular structures, electrostatic force potential, and
molecular graphs can be accurately predicted using AFM images from simulations or experiments.

## Motivation

Finding the structure from AFM images is not an easy task, which need lots of human experience. Using the state of art AFM simulation and Density functional theory calculations, we can obtain many AFM images and its corresoponding structures, which enables us to train a model to obtain the map from AFM images to its corresponding structure. In the previous work, we have developed some machine learning algorithms based on two stages. To improve our workflow, it could be better to use a end-to-end model, which could be much easy to train. Therefore, it holds the great potential to apply the model to experimental AFM images. 


## What we've done

In this project, we've applied an image-to-graph translation tool ([Relationformer](https://github.com/suprosanna/relationformer)) for nc-AFM images to predict the sample structure including atomic types and bonds. In particular, we will use a transformer based model that simultaneously predicts objects (atoms) and their relations (bonds) for accurate geometry characterization. For gathering training data, we will use a high-throughput nc-AFM simulator (PPAFM) which gives us the high-resolution images and molecule-graph labels.

## Methods

Simulation data: We have use PPM model to get the simulated images. 
Image-to-Graph model: We have use the Relationformer as our end-to-end model. 

## Expected results

## References

## Aknowlegements
