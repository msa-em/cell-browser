---
title: Autoencoders
numbering:
  enumerator: 8.%s
---

# Introduction

Microscopy maps are interactive figures, yet static images predominate scientific publishing.
Despite the benefits of virtual microscopy, representative images will continue to be used until mainstream journals adopt modern visualization tools.
Because scientific communication often uses static figures, we also considered methods of computational image selection.
This follows a study critical of representative microscopy images that focused on methods of objective image selection to reduce bias (https://doi.org/10.1016/s0006-3495(99)77379-0).
To explore the possibility of using computers to select microscopy images, we made a dataset of one million images of the [cell nucleus](<wiki:Cell_nucleus>) called _NucleusNet_, then representative images were selected from NucleusNet by an [autoencoder](<wiki:Autoencoder>) model.
Autoencoders are unsupervised deep learning models that compress and reconstruct images through a vector bottleneck referred to as _latent space_.
The structure of latent space is a [black box](<wiki:Black_box>), though it can be shaped to be more useful with the art of representation learning [@doi:10.1109/TPAMI.2013.50].
Representative images were defined near the centroid of latent space, though counterexamples showed that this approach does not generalize to all datasets.
To define what is representative, both the subjective determinations made by humans and the objective determinations made by autoencoders are opaque.

Paraphrased from the Deep Learning book ({cite}`Goodfellow-et-al-2016`), an autoencoder is a neural network that is trained to copy its input to its output.
Autoencoders originated in the eighties and its primary application was dimensionality reduction for information storage and retrieval.
Autoencoders consist of two parts: an encoder and a decoder with hidden layers that describe the code used to represent the data.
The autoencoder is restricted in some way that it is forced to prioritize which aspects of the input to copy, so it often learns useful properties of the data.

Autoencoders can be used for anomaly detection, which is based on the assumption that the autoencoder learns an optimal latent space to describe the normal data, so that when images are reconstructed, anomalous data will have a higher reconstruction error than normal data [@doi:10.1109/WTS.2018.8363930].
Though this assumption is flawed [@doi:10.48550/arXiv.2501.13864] and autoencoders are unreliable anomaly detectors [@doi:10.1109/ICUFN57995.2023.10199315], it would suggest that autoencoders could be useful to select representative images from datasets.

An image collection of over one million [cell nuclei](<wiki:Cell_nucleus>) was made to help train machine learning models on microscopy data.
It is the sum of 100 automated confocal imaging experiments that sampled ~37.25cm² at high-magnification, yielding 1,061,277 cropped single-cell images segmented from 1600 stitched panoramas.
An autoencoder was trained on NucleusNet and representative images were defined near the centroids of latent space, though this approach was unjustifiable because the latent space was uninterpretable.

:::{dropdown} Model architecture
Our autoencoder used common configurations for anomaly detection [@doi:10.48550/arXiv.2501.13864].
Rectified linear unit (ReLU) activation functions were used throughout the network for nonlinearity, except with a sigmoid activation function at the final layer.
Linear activation functions were used in the fully-connected dense layer connections to and from the latent space bottleneck.
Stacked $3*3$ kernels were used throughout the network, so each layer had two convolutions without spatial pooling in between, giving an effective receptive field of $5*5$ with fewer parameters and greater nonlinearity.
Spatial pooling is carried out by average pooling layers, which is performed over a $2*2$ window with a stride of 2.
A stack of four convolutional layers was followed by a fully-connected dense layer into latent space $z$. 
The decoder mirrors the encoder.
Latent vectors are reshaped then upsampled with Conv2DTranspose (stride 2) and Conv2D through a stack of convolutional layers to reconstruct a grayscale image.
The network was trained with Adam optimizer to minimize the mean squared error (MSE) between original and reconstructed images.
These configurations were used for all autoencoders in this study.
Models varied in the number of layers, number of filters, latent dimensions, learning rate and batch size which were parameters that were manually tuned to the dataset.
The dimensions of the inputs varied; 28 by 28 pixels for MNIST and 256 by 256 pixels for NucleusNet.
There are variations of autoencoders that have been compared to show the efficiencies and trade-offs of different models at image reconstruction, latent representation and accuracy at anomaly detection [@doi:10.1016/j.mlwa.2024.100572].
:::

# MNIST dataset

## Method replication

A method of objective representative image selection [@doi:10.1109/BIP60195.2023.10379342] was shown on real-world data including the [MNIST database](<wiki:MNIST_database>), which is an annotated collection of 70,000 images of handwritten numbers.
Their two-step approach to objective representative image selection calculated theoretical average images then measured the distance between real and theoretical images in vector space.
Measures of central tendency were the arithmetic mean, median and geometric median, calculated as 784-dimensional vectors reshaped to 28x28 pixel images.
Their example tested a sub-set of MNIST images (n=720) labelled 'four'.
Our attempt used all MNIST 'four' images (N=6824), but the theoretical images were consistent with previous work ([](#fig8a)) [@doi:10.1109/BIP60195.2023.10379342].

:::{figure} #fig8a_data
:label: fig8a
:placeholder: ./figures/fig8a.png
Replicating theoretical images of the MNIST digit 'four'.
N=6824 grayscale 'four' images were flattened to 784-dimensional vectors to calculate then reshape reconstructions of the arithmetic mean, median and geometric median.
:::

:::{figure} #fig8b_data
:label: fig8b
:placeholder: ./figures/fig8b.png
Practical images of the MNIST digit '4' [based on the singular value decomposition](https://github.com/jusotoTEC/reprImgSVD).
:::

## Autoencoder-based method

### 1. Calculating and decoding average latent vectors

An autoencoder model was trained on the MNIST dataset ([](#sfig10a)) and the weights were saved to this repository.
n=6824 encoded latent vectors corresponding to the image 'four' were averaged and reconstructed using the decoder weights ([](#fig8c)).
Theoretical images output from the autoencoder appeared similar to the previous reconstructions ([](#fig8a)).

:::{figure} #fig8c_data
:name: fig8c
:placeholder: ./figures/fig8c.png
Decoded latent vectors: arithmetic mean, median and geometric median.
:::

### 2. Determining practical images in Euclidean space

The behaviour of the theoretical image generally does not correspond to a distinct image, therefore it is not considered the final representative image.
However, it can be used to select representative examples from the dataset [@doi:10.1109/BIP60195.2023.10379342].
Encoded vectors corresponding to real images were ranked by Euclidean distance to the centroids in latent space to define the closest real images ([](#fig8d)).
Unexpectedly, the outcome was remarkably similar, if not identical to the previous method ([](#fig8b)).

:::{figure} #fig8d_data
:name: fig8d
:placeholder: ./figures/fig8d.png
Nearest encoded vectors to the arithmetic mean, median and geometric median.
:::

## Limitations

These methods relied on testing a sub-set of manually annotated data.
Reconstructing theoretical averages using the entire dataset produced counterexamples ([](#fig8e) and [](#fig8f)), which shows that this two-step approach cannot generalize to all datasets.
Conceptually, it made sense to find an average example of the digit four, but not to find the average of all digits.
Perhaps these methods would benefit from an upstream classifier model or manual annotation.

:::{figure} #fig8e_data
:name: fig8e
:placeholder: ./figures/fig8e.png
Reconstructing theoretical MNIST digits by averaging pixels without labels.
:::

:::{figure} #fig8f_data
:name: fig8f
:placeholder: ./figures/fig8f.png
Autoencoder reconstructions of theoretical MNIST digits without labels. The 64-dimensional latent space was averaged and decoded using the saved weights.
:::
