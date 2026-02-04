---
title: Approach
numbering:
  enumerator: 7.%s
label : ml_page
---

---

# Computational image selection with machine learning

The process of representative microscopy image selection remains a subjective, non-repeatable step in the scientific process.
To address this, automated methods of objective representative image selection from microscopy datasets were introduced (https://doi.org/10.1016/s0006-3495(99)77379-0).
The challenge is to automate representative image selection with computers.
One study proposed principal component analysis and K-means clustering to select representative images from medical ultrasound video series [@doi:10.3389/fonc.2021.673775].
Another method was proposed using real-world datasets [@doi:10.1109/BIP60195.2023.10379342], though it did not involve neural networks.
We propose a method using autoencoder models to define representative images in latent space and compared methods on the [MNIST database](<wiki:MNIST_database>).

Autoencoders are commonly used for anomaly detection, which is based on the assumption that the autoencoder learns an optimal latent space to describe the normal data, so that when images are reconstructed, anomalous data will have a higher reconstruction error than normal data [@doi:10.1109/WTS.2018.8363930].
Though this assumption is flawed [@doi:10.48550/arXiv.2501.13864] and autoencoders can be unreliable anomaly detectors [@doi:10.1109/ICUFN57995.2023.10199315], it would suggest that autoencoders could be useful to select normal images from datasets.

Barkley imaged one million unique examples of the [cell nucleus](<wiki:Cell_nucleus>), a scale suitable to train artificial intelligence models.
It is the sum of 100 automated confocal imaging experiments that sampled ~37.25cm² at high-magnification, yielding 1,061,277 cropped single-cell images segmented from 1600 stitched panoramas.
An autoencoder was trained on NucleusNet, and representative images were defined near centroids of latent space.
However, the embedding is uninterpretable and design limitations were encountered, so it was impossible to justify this approach.