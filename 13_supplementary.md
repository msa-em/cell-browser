---
title: Supplementary Information
numbering:
  enumerator: 10.%s
---

# Definitions

_Virtual microscopy_ is the process of sharing image data over computer networks.
A related term _virtual nanoscopy_ described the process of automated imaging and unbiased presentation of electron microscopy data using interactive viewers [@doi:10.1083/jcb.201201140].

A _microscopy map_ is the interactive figure used to view virtual microscopy data [@doi:10.1083/jcb.201201140].
This name fits broader use cases including light and electron microscopy.

A _representative image_ is an illustration used by microscopists to exemplify research results to other scientists.
This definition is agnostic to the research context and it emphasizes the use of pictures as scientific evidence.

A _grayscale image_ is defined as a two-dimensional matrix where each pixel is a single intensity value ranging from 0-1 that represents the amount of light or intensity information at a specific point [@doi:10.1109/BIP60195.2023.10379342].

A _latent space_ is a collection of vectors that form a reduced-dimensionality embedding of the data, fit by a machine learning model [@doi:10.1111/cgf.13672].

---

# MNIST autoencoder

## Training history

:::{figure} #sfig10a_data
:label: sfig10a
:placeholder: ./figures/sfig10a.png
Autoencoder MSE reconstruction loss over one-hundred epochs of training on the MNIST dataset.
:::

---

# NucleusNet

:::{figure} #sfig10b_data
:label: sfig10b
:placeholder: ./figures/sfig10b.png
The number and brightness of ROIs in the stitched images was measured using the associated cellpose mask files. A pre-computed centroid 694.5 ROIs and 79.0 mean intensity was marked.
:::

```{list-table} Representative stitched images ranked by distance to centroid: 694.5 ROIs, 79.0 mean intensity
:label: table3
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

## Model

The entire single-cell image collection was sharded into [TFRecords](https://www.tensorflow.org/tutorials/load_data/tfrecord) to better load the dataset into memory and shuffle it during training.
An autoencoder model was trained for 50 epochs on NucleusNet and the encoder and decoder weights were saved.
The input was 256 by 256 pixel grayscale images that were embedded into 512-dimensional latent vectors.
The model overfit slightly because the training and validation losses diverged at later epochs.

### Training history

:::{figure} #sfig10c_data
:label: sfig10c
:placeholder: ./figures/sfig10c.png
History of MSE reconstruction loss (batch size: 32) for the training and validation datasets over 50 epochs.
:::

## Latent space interpolation

A method to evaluate the quality of latent space is interpolation, whereby mixing codes in latent space and decoding the result creates a semantically meaningful combination of the datapoints [@doi:10.48550/arXiv.1807.07543].
Interpolating with an autoencoder describes the process of using the decoder to decode a convex combination of two latent vectors [@doi:10.48550/arXiv.1807.07543].
A high-quality interpolation should have two characteristics: intermediate points along the interpolation should resemble real data and they should provide a semantically meaningful transition between the endpoints [@doi:10.48550/arXiv.1807.07543].
Interpolating between any two latent vectors of embedded NucleusNet images produced reasonable intermediate reconstructions from the decoder with a smooth transition between endpoints ([](#sfig10d)).

:::{figure} #sfig10d_data
:label: sfig10d
:placeholder: ./figures/sfig10d.png

Random pairs from NucleusNet-10K. All images are decoded vectors. t=0.00 and t=1.00 correspond to latent vectors of real images. Four intermediate interpolations at t=0.20, t=0.40, t=0.60 and t=0.80 are mixed codes. Run the notebook to resample random pairs of embedded vectors from NucleusNet-10K.
:::

---

# Stereotypical images from NucleusNet-10K

### Anaphase
```{image} ./figures/anaphase.png
:label: anaphase
```

### Telophase
```{image} ./figures/telophase.png
:label: telophase
```