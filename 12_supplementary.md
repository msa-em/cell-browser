---
title: Supplementary Data
numbering:
  enumerator: 12.%s
label : supplementary_page
---

---

# MNIST autoencoder

## Loss plot

:::{figure} #sfig12a_data
:label: sfig12a
:placeholder: ./figures/sfig12a.png
Autoencoder reconstruction loss over one-hundred epochs of training on the MNIST dataset.
:::

---

# NucleusNet

:::{figure} #sfig12b_data
:label: sfig12b
:placeholder: ./figures/sfig12b.png
The number and brightness of ROIs in the stitched images was measured using the associated cellpose mask files. A pre-computed centroid 694.5 ROIs and 79.0 mean intensity was marked.
:::

```{list-table} Representative stitched images ranked by distance to centroid: 694.5 ROIs, 79.0 mean intensity
:label: sTable1
:header-rows: 1

* - Filename
  - Number of ROIs
  - Mean intensity
  - Distance*
* - Run72TR_bottom_left
  - 685
  - 78.6
  - 0.046
* - Run63TR_top_right
  - 709
  - 78.6
  - 0.066
* - Run72BR_top_right
  - 687
  - 80.3
  - 0.074
* - Run68TR_top_right
  - 711
  - 79.6
  - 0.076
* - Run25BR_top_right
  - 698
  - 77.5
  - 0.079
* - Run25BR_bottom_left
  - 681
  - 78.0
  - 0.080
* - Run72BR_top_left
  - 712
  - 79.5
  - 0.080
* - Run102TR_top_left
  - 716
  - 78.3
  - 0.099
* - Run50TL_top_right
  - 714
  - 77.8
  - 0.104
* - Run72BL_top_right
  - 720
  - 79.1
  - 0.109
```
Z-score-normalized euclidean distance was used for equal weighting because the features had different scales.

---

# NucleusNet autoencoder

## Model training

The entire single-cell image collection was sharded into [TFRecords](https://www.tensorflow.org/tutorials/load_data/tfrecord) to better load the dataset into memory and shuffle it during training.
An autoencoder model was trained for 50 epochs on NucleusNet and the encoder and decoder weights were saved.
The input was 256 by 256 pixel grayscale images that were embedded into 512-dimensional latent vectors.
Barkley interpreted that the model overfit to the data because the training loss reduced more than validation loss at later epochs.

### Loss plot

:::{figure} #sfig12c_data
:label: sfig12c
:placeholder: ./figures/sfig12c.png
History of MSE reconstruction loss (batch size: 32) for the training and validation datasets over 50 epochs.
:::

## Latent space interpolation

A method to evaluate the quality of latent space is interpolation, whereby mixing codes in latent space and decoding the result creates a semantically meaningful combination of the datapoints [@doi:10.48550/arXiv.1807.07543].
Interpolating with an autoencoder describes the process of using the decoder to decode a convex combination of two latent vectors [@doi:10.48550/arXiv.1807.07543].
A high-quality interpolation should have two characteristics: intermediate points along the interpolation should resemble real data and they should provide a semantically meaningful transition between the endpoints [@doi:10.48550/arXiv.1807.07543].
Interpolating between any two latent vectors of embedded NucleusNet images produced reasonable intermediate reconstructions from the decoder with a smooth transition between endpoints ([](#fig2h)).
This result is consistent with the literature describing smooth interpolations with base model autoencoders [@doi:10.48550/arXiv.1807.07543].
The authors noted that intermediate points did not always resemble real data, which was true with some of the NucleusNet-10K interpolations.

:::{figure} #sfig12d_data
:label: sfig12d
:placeholder: ./figures/sfig12d.png

Decoded latent vectors along intermediate points of interpolations between random pairs of images from NucleusNet-10K.
Executing the code will randomly draw fifty pairs for interpolation.
Images that you see are decoded latent vectors, with t=0.00 and t=1.00 representing latent vectors corresponding to real images.
Four intermediate interpolations at t=0.20, t=0.40, t=0.60 and t=0.80 are mixed codes.
:::

---

# Replication study

Barkley noted the type of data in each figure and supplementary figure, excluding videos, in order of presentation.
For data type, there were four possible options; light microscopy image, electron microscopy image, correlative light-electron microscopy image, quantitation.
Quantitation was considered any analysis with numbers, while the other three data types were representative images.
Some figure panels had multiple images.
If the images were of different samples, then they were counted as unique images (>1 images).
Others were multi-channel or time-lapse images, which was considered one image with multiple frames.

```{list-table} Assessment of the types of data in the original study [@doi:10.1128/mBio.01253-18].
:label: table4
:header-rows: 1
* - Figure
  - Data type
  - Images
  - Frames
  - Frame type
* - 1A
  - Light microscopy image
  - 1
  - 1
  -
* - 1B
  - Light microscopy image
  - 1
  - 1
  -
* - 1C
  - Electron microscopy image
  - 1
  - 1
  -
* - 1D
  - Correlative light-electron microscopy image
  - 1
  - 1
  -
* - 1E
  - Correlative light-electron microscopy image
  - 1
  - 1
  -
* - 1F
  - Electron microscopy image
  - 1
  - 1
  -
* - S1A
  - Light microscopy image
  - 2
  - 1
  -
* - S1B
  - Electron microscopy image
  - 4
  - 1
  -
* - 2A
  - Electron microscopy image
  - 1
  - 1
  -
* - 2B
  - Electron microscopy image
  - 1
  - 1
  -
* - 2C
  - Electron microscopy image
  - 1
  - 1
  -
* - 2D
  - Electron microscopy image
  - 1
  - 1
  -
* - 2E
  - Electron microscopy image
  - 1
  - 1
  -
* - 2F
  - Electron microscopy image
  - 1
  - 1
  -
* - 2G
  - Electron microscopy image
  - 1
  - 1
  -
* - 2H
  - Electron microscopy image
  - 4
  - 1
  -
* - 3
  - Electron microscopy image
  - 1
  - 1
  -
* - 4A
  - Light microscopy image
  - 1
  - 4
  - Time
* - 4B
  - Light microscopy image
  - 1
  - 2
  - Channel
* - 4C
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S2A
  - Light microscopy image
  - 1
  - 3
  - Time
* - S2B
  - Light microscopy image
  - 1
  - 3
  - Time
* - 5A
  - Light microscopy image
  - 4
  - 1
  -
* - 5B
  - Light microscopy image
  - 1
  - 3
  - Channel
* - 5C
  - Light microscopy image
  - 1
  - 3
  - Channel
* - 5D
  - Electron microscopy image
  - 1
  - 1
  -
* - 5E
  - Electron microscopy image
  - 1
  - 1
  -
* - S3A
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3B
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3C
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3D
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3E
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3F
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3G
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3H
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3I
  - Light microscopy image
  - 1
  - 3
  - Channel
* - 6A
  - Quantitation
  - 0
  - 0
  -
* - 6C
  - Quantitation
  - 0
  - 0
  -
```

---

# Stereotypical images from NucleusNet-10K

```{image} ./figures/anaphase.png
:label: anaphase
Anaphase
```
```{image} ./figures/telophase.png
:label: telophase
Telophase
```

