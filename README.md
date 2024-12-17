# Structure Discovery through Image-to-Graph Machine Learning Model

![](https://cdn.jsdelivr.net/gh/HuangJiaLian/DataBase0@master/uPic/2024-12-17-19-30-Hello.png)

## Introduction

Atomic Force Microscopy (AFM) plays a crucial role in characterizing atomic-scale nanostructures. However, identifying structures from AFM images is a challenging task that relies heavily on human expertise. Simulations, particularly with Particle Probe AFM (PPAFM) [1, 2, 3], offer a cost-effective solution for generating large volumes of AFM images. By leveraging state-of-the-art machine learning models and extensive PPAFM-generated datasets, properties such as molecular structures, electrostatic potential maps, and molecular graphs can be accurately predicted using AFM images obtained from simulations or experiments.

## Motivation

Determining structures from AFM images is complex and demands significant human experience. By utilizing advanced AFM simulations and Density Functional Theory (DFT) calculations, we can generate numerous AFM images along with their corresponding structures. This dataset enables us to train machine learning models to map AFM images to their underlying structures.

In our previous work, we developed machine learning workflows based on a two-stage process. To enhance this workflow, we aim to use an end-to-end model, which simplifies the training process and improves overall efficiency. Such a model has great potential for application to experimental AFM images, enabling faster and more reliable structure discovery.

## What we've done

In this project, we applied an image-to-graph translation tool, [Relationformer](https://github.com/suprosanna/relationformer), to non-contact AFM (nc-AFM) images to predict sample structures, including atomic types and bonds. Specifically, we used a transformer-based model capable of simultaneously predicting objects (atoms) and their relationships (bonds), ensuring accurate geometric characterization.

To train this model, we utilized a high-throughput nc-AFM simulator, PPAFM, which provides high-resolution AFM images alongside molecular graph labels.

## Methods

Simulation data: We have use PPM model to get the simulated images. 
Image-to-Graph model: We have use the Relationformer as our end-to-end model. 

## Expected results

- Accurate prediction of molecular graphs, including atom types and bond information, from AFM images.
- Enhanced workflow efficiency by transitioning to an end-to-end machine learning model.
- Potential applicability to experimental AFM images for real-world structure discovery.

## References
1. Niko Oinonen, Aliaksandr V. Yakutovich, Aurelio Gallardo, Martin Ondracek, Prokop Hapala, Ondrej Krejci, Advancing Scanning Probe Microscopy Simulations: A Decade of Development in Probe-Particle Models, Comput. Phys. Commun. 305, 109341 - Available online 10 August 2024 <br/> 
2. Prokop Hapala, Georgy Kichin, Christian Wagner, F. Stefan Tautz, Ruslan Temirov, and Pavel Jelínek, Mechanism of high-resolution STM/AFM imaging with functionalized tips, Phys. Rev. B 90, 085421 – Published 19 August 2014 <br/>
3. Prokop Hapala, Ruslan Temirov, F. Stefan Tautz, and Pavel Jelínek, Origin of High-Resolution IETS-STM Images of Organic Molecules with Functionalized Tips, Phys. Rev. Lett. 113, 226101 – Published 25 November 2014 <br/>

## Aknowlegements

We thank the authors of the project of [Relationformer](https://github.com/suprosanna/relationformer).
