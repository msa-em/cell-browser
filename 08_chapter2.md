---
title: Chapter 2
numbering:
  enumerator: 8.%s
label : chapter2_page
---

Autoencoders are commonly used for anomaly detection, which is based on the assumption that the autoencoder learns an optimal latent space to describe the normal data, so that when images are reconstructed, anomalous data will have a higher reconstruction error than normal data [@doi:10.1109/WTS.2018.8363930].
Though this assumption is flawed [@doi:10.48550/arXiv.2501.13864] and autoencoders can be unreliable anomaly detectors [@doi:10.1109/ICUFN57995.2023.10199315], it would suggest that autoencoders could be useful to select normal images from a dataset.
In this section, we explored methods of objective representative image selection to contribute to this open challenge (https://doi.org/10.1016/s0006-3495(99)77379-0).
The goal was to use an artificial intelligence model to determine average images from a dataset.
It was demonstrated in a study that used principal component analysis and K-means clustering to select representative images from medical ultrasound video series [@doi:10.3389/fonc.2021.673775].
Another method for objective representative image selection was tested on real-world datasets [@doi:10.1109/BIP60195.2023.10379342], though it did not involve neural networks.
The proposed method made average images using measures of central tendency in pixel space, then practical images were defined in vector space.
Barkley adapted this approach to the latent space of an autoencoder model and compared methods on the [MNIST database](<wiki:MNIST_database>).

Artificial intelligence models need large datasets, so Barkley created an image collection of the [cell nucleus](<wiki:Cell_nucleus>) called NucleusNet.
It is the sum of 100 automated confocal imaging experiments that sampled ~37.25cm² at high-magnification, yielding 1,061,277 cropped single-cell images segmented from 1600 stitched panoramas.
A random selection of ~1% of NucleusNet can be browsed using [OpenSeadragon](https://openseadragon.github.io/).
An autoencoder model was trained on NucleusNet, and representative images were defined near the centroid of the embedding.
It is impossible interpret the embedding and justify this approach because neural networks are black boxes.
However, it is a method that is unlikely to return anomalous examples as representative images from datasets of this scale.