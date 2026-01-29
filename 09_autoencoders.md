---
title: Autoencoders
numbering:
  enumerator: 8.%s
label : autoencoders_page
---

From the Deep Learning book {cite}`Goodfellow-et-al-2016`; an autoencoder is a neural network that is trained to copy its input to its output.
Autoencoders originated in the eighties and its primary application was dimensionality reduction for information storage and retrieval.
Autoencoders consist of two parts: an encoder and a decoder with hidden layers that describe the code used to represent the data.
The autoencoder is restricted in some way that it is forced to prioritize which aspects of the input to copy, so it often learns useful properties of the data.

## Model architecture

The architecture of our networks followed a common configuration in autoencoder-based anomaly detection methods [@doi:10.48550/arXiv.2501.13864].
Rectified linear unit (ReLU) activation functions were used throughout the network for nonlinearity {cite}`NIPS2012_c399862d`, except with a sigmoid activation function at the final layer.
Linear activation functions were used in the fully-connected dense layer connections to and from the latent space bottleneck.
Stacked $3*3$ kernels were used throughout the network, so each layer had two convolutions without spatial pooling in between, giving an effective receptive field of $5*5$ with fewer parameters and greater nonlinearity [@doi:10.48550/arXiv.1409.1556].
Spatial pooling is carried out by average pooling layers, which is performed over a $2*2$ window with a stride of 2.
A stack of four convolutional layers was followed by a fully-connected dense layer into latent space $z$. 
The decoder mirrors the encoder.
Latent vectors are reshaped then upsampled with Conv2DTranspose (stride 2) and Conv2D through a stack of convolutional layers to reconstruct a grayscale image.
The network was trained with Adam optimizer [@doi:10.48550/arXiv.1412.6980] to minimize the mean squared error (MSE) between original and reconstructed images.
These configurations were used for all autoencoders in this study.
Models varied in the number of layers, number of filters, latent dimensions, learning rate and batch size which were parameters that were manually tuned to the dataset.
The dimensions of the inputs varied; 28 by 28 pixels for MNIST and 256 by 256 pixels for NucleusNet.
There are variations of autoencoders that have been compared to show the efficiencies and trade-offs of different models at image reconstruction, latent representation and accuracy at anomaly detection [@doi:10.1016/j.mlwa.2024.100572].

---

# MNIST dataset

## Literature replication

A method of objective representative image selection [@doi:10.1109/BIP60195.2023.10379342] was tested on real-world data like the [MNIST database](<wiki:MNIST_database>), which is a collection of 70,000 images of handwritten numbers that were manually annotated into ten classes corresponding to the digits 0-9.
Briefly, their two-step approach to objective representative image selection calculated theoretical average images then measured the distance between real and theoretical images in vector space.
Measures of central tendency were the arithmetic mean, median and geometric median, calculated as 784-dimensional vectors then reshaped to reconstruct 28x28 pixel theoretical images.
Their example used a sub-set of MNIST images (n=720) labelled 'four'.
Our example used all MNIST "four" images (N=6824), but the outcome was consistent with the primary literature ([](#fig9a)) [@doi:10.1109/BIP60195.2023.10379342].

:::{figure} #fig9a_data
:label: fig9a
:placeholder: ./figures/fig9a.png
Computation of theoretical representative images of the MNIST digit '4'.
N=6824 grayscale images with the label '4' were flattened to 784-dimensional vectors to compute then reshape reconstructed images of the arithmetic mean (left), median (middle) and geometric median (right).
:::

The chosen exemplars were not the same as the original study ([](#fig9b)).

:::{figure} #fig9b_data
:label: fig9b
:placeholder: ./figures/fig9b.png
Computation of practical representative images of the MNIST digit '4' using the arithmetic mean (left), median (middle) and geometric median (right).
:::

## Using autoencoders to select average MNIST digits

This approach to representative image selection was adopted to use the latent space of an autoencoder model.
First, theoretical average latent vectors were calculated using measures of central tendency.
Then, practical examples in the embedding were ranked by Euclidean distance to the calculated centroids.

### 1. Compute and decode centroid latent vectors

A convolutional autoencoder model was trained on the MNIST dataset and the encoder and decoder weights were saved ([](#sfig12a)). 
n=6824 latent vectors labelled 'four' were averaged and reconstructed using the decoder weights to synthesize theoretical images of the digit 'four' ([](#fig9c)).
The decoded centroid latent vectors appeared similar to the mean and median reconstructions calculated using independent pixel values ([](#fig9a)).

:::{figure} #fig9c_data
:name: fig9c
:placeholder: ./figures/fig9c.png
Decoded latent vectors: arithmetic mean (left), median (middle) and geometric median (right).
:::

### 2. Define practical images in Euclidean space

The behaviour of the theoretical image generally does not correspond to a distinct image, therefore it is not considered the final representative image.
However, it can be used to select representative examples from the dataset [@doi:10.1109/BIP60195.2023.10379342].
The closest latent vector to each centroid was found based on the lowest Euclidean distance in the vector embedding ([](#fig9d)).
The chosen images were remarkably similar, suggesting these methods are comparable.

:::{figure} #fig9d_data
:name: fig9d
:placeholder: ./figures/fig9d.png
Closest examples to the arithmetic mean (left), median (middle) and geometric median (right).
:::

## Limitations

These examples of objective image selection relied on class information from an annotated dataset.
Both methods fell apart reconstructing theoretical averages of global centroids without labels ([](#fig9e) and [](#fig9f)).
This shows that the approach does not generalize.
Conceptually, it made sense to find an average image of the digit four, but not to find the average of all digits.
Perhaps this approach would be more reliable with labels, but this would require an upstream classifier model or manual annotation.

:::{figure} #fig9e_data
:name: fig9e
:placeholder: ./figures/fig9e.png
Figure legend.
:::

:::{figure} #fig9f_data
:name: fig9f
:placeholder: ./figures/fig9f.png
Figure legend.
:::
