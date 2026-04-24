---
title: Introduction
numbering:
  enumerator: 0.%s
---

Microscopy maps are interactive figures, yet static images predominate scientific publishing.
Despite the benefits of virtual microscopy, representative images will continue to be used until mainstream journals adopt modern visualization tools.
Because scientific communication often uses static figures, we also considered methods of computational image selection.
This follows a study critical of representative microscopy images that focused on methods of objective image selection to reduce bias (https://doi.org/10.1016/s0006-3495(99)77379-0).
To explore the possibility of using computers to select microscopy images, we made a dataset of one million images of the [cell nucleus](<wiki:Cell_nucleus>) called _NucleusNet_, then representative images were selected from NucleusNet by an [autoencoder](<wiki:Autoencoder>) model.
Autoencoders are unsupervised deep learning models that compress and reconstruct images through a vector bottleneck referred to as _latent space_.
The structure of latent space is a [black box](<wiki:Black_box>), though it can be shaped to be more useful with the art of representation learning [@doi:10.1109/TPAMI.2013.50].
Representative images were defined near the centroid of latent space, though counterexamples showed that this approach does not generalize to all datasets.
To define what is representative, both the subjective determinations made by humans and the objective determinations made by autoencoders are opaque.

Autoencoders can be used for anomaly detection, which is based on the assumption that the autoencoder learns an optimal latent space to describe the normal data, so that when images are reconstructed, anomalous data will have a higher reconstruction error than normal data [@doi:10.1109/WTS.2018.8363930].
Though this assumption is flawed [@doi:10.48550/arXiv.2501.13864] and autoencoders are unreliable anomaly detectors [@doi:10.1109/ICUFN57995.2023.10199315], it would suggest that autoencoders could be useful to select representative images from datasets.

An image collection of over one million [cell nuclei](<wiki:Cell_nucleus>) was made to help train machine learning models on microscopy data.
It is the sum of 100 automated confocal imaging experiments that sampled ~37.25cm² at high-magnification, yielding 1,061,277 cropped single-cell images segmented from 1600 stitched panoramas.
An autoencoder was trained on NucleusNet and representative images were defined near the centroids of latent space, though this approach was unjustifiable because the latent space was uninterpretable.
