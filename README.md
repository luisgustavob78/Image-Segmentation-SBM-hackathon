# Image-Segmentation-SBM-hackathon

## Introduction

Corrosion is one of the biggest issues in offshore operations at oil & gas indsutry. That phenom can be responsble for a lot of mechanical failures in critical equipments like pipes, pressure vessels, and heat exchangers. To deal with this problem, there are some techniques of inspection to detect the development of corrosion process on those equipments, but all of them are dependent of too much human intervention, what makes these techniques very biased and confused. 

Thinking about these questions, the SBM offshore company launched a hackathon where the challenge was to create an image segmentation model to detect through an image if there is some kind of corrosion in a specific equipment installed in her ships used as Floating Production Storage and Offloading (FPSO). The business goal here is to increase the level of atomation in the corrosion detection process to get more accuracy than human-based conclusions and to reduce the inspection costs.

## Data

The company made avaliable 2000 images and respectives annotations for the participants. This kind of asset is very strategic for an oil & gas company, and because of thes any participant is authorized to share this data.

## Preprocessing

To get the data ready for the model, we used Keras ImageDataGenerator to create the datasets and to execute a process of data augmentation that was used to increase our data and to simulate different quality of images to make the model more generalist

![](https://github.com/luisgustavob78/Image-Segmentation-SBM-hackathon/blob/main/image_data_generator.png)

## Modelling

One of the main criteria in the hackathon was the computational cost. The ships used by SBM are located thousands of miles from the coast, what makes the quality of network signal very poor, so they need a solution that can be run on the edge. 

Considering this detail, me and my team chose the Unet model beacuase is a lighter model compared with mask r cnn, for example.

As result, we reached 82% of accuracy and 51% of losses.

![](https://github.com/luisgustavob78/Image-Segmentation-SBM-hackathon/blob/main/GIF%2025-10-2020%2021-52-58.gif)

## Instalation 

All the code was run on google colab, where all TensorFlow extensions are already installed. The only installation we needed to do was the following:

´´´

pip install -q git+https://github.com/tensorflow/examples.git

´´´
