---
title: Background
numbering:
  enumerator: 8.%s
label : background_page
---

In this second chapter we explored methods of objective representative image selection.
The goal was to use an artificial intelligence model to determine average images from a dataset.
It was first demonstrated in a study that used principal component analysis and K-means clustering to select representative images from medical ultrasound video series [@doi:10.3389/fonc.2021.673775].
Another method for objective representative image selection was tested on real-world datasets [@doi:10.1109/BIP60195.2023.10379342], though it did not involve neural networks.
The proposed method made average images using measures of central tendency in pixel space, then practical images were defined in vector space using singular value decomposition.
Barkley adapted this approach to the latent space of a convolutional autoencoder model and compared methods on the [MNIST database](<wiki:MNIST_database>).

Artificial intelligence models require large datasets, so Barkley created a large but simple image collection of the [cell nucleus](<wiki:Cell_nucleus>) called NucleusNet.
It is the sum of 100 automated confocal imaging experiments that sampled ~37.25cm² at high-magnification, yielding 1,061,277 cropped single-cell images segmented from 1600 stitched panoramas.
A random selection of 1% of NucleusNet can be browsed using [OpenSeadragon](https://openseadragon.github.io/).

Autoencoders are commonly used for anomaly detection, which is based on the assumption that the autoencoder learns an optimal latent space to describe the normal data, so that when images are reconstructed, anomalous data will have a higher reconstruction error than normal data [@doi:10.1109/WTS.2018.8363930].
Though this assumption is flawed [@doi:10.48550/arXiv.2501.13864] and autoencoders can be unreliable anomaly detectors [@doi:10.1109/ICUFN57995.2023.10199315], it would suggest that autoencoders could be useful to select normal images from a dataset.
An autoencoder model was trained on NucleusNet, and representative images were defined near the centroid of the embedding.

