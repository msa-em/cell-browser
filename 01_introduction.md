---
title: Introduction
numbering:
  enumerator: 0.%s
label : introduction_page
---

Representative microscopy images are visual communication tools used by microscopists to present the results of research to other scientists.
The earliest representative microscopy images were hand drawings in [Micrographia](<wiki:Micrographia>) in 1665 by Robert Hooke.
Nowadays, roughly three-quarters of publications in biomedical journals report at least one microscopy image [@doi:10.7554/eLife.55133].
An unspoken rule is that scientists trust the chosen images are honest and accurate.
However, microscopy image selection and quantitative analyses thereof are vulnerable to bias and deception [@doi:10.1242/jcs.261567].
Aside from cherry-picking, scientists can sincerely misinterpret observations.
The problem is that it is difficult for readers to critically evaluate representative images.
Furthermore, archival and review of primary microscopy data is disorganized and time-consuming, if at all available.
These inefficiencies can be overcome with interactive visualization stategies like [virtual microscopy](<wiki:Virtual_microscopy>) that transmit images over the internet.
An example was the unbiased sampling and presentation of electron microscopy data to readers as interactive digital maps; microscopy maps [@doi:10.1083/jcb.201201140].
In practice, microscopy maps are easy to implement, but are viewed with external links or software [@doi:10.1242/jcs.262198].
Here, interactive microscopy maps were embedded in the article to introduce virtual microscopy to the literature.

[Reproducibility](<wiki:Reproducibility>) is an essential principle of the [scientific method](<wiki:Scientific_method>) for acquiring knowledge, yet there is a contentious [reproducibility crisis](<wiki:Replication_crisis>) in science.
From the perspective of biomedical researchers, the perceived cause is the pressure to publish [@doi:10.1371/journal.pbio.3002870].
Repeatability in the same study by the same researchers is distinguished from replicability by independent researchers using the same methodology.
Large-scale replicability studies performed by Amgen and Bayer assessed that 11% [@doi:10.1038/483531a] and 25% [@doi:10.1038/nrd3439-c1] of key findings from preclinical cancer research papers were replicable.
Another project evaluated replication success with other criteria, but their 'lowest bar' determined a replication rate of 79% for representative images [@doi:10.7554/eLife.71601].
Further, 26% of claimed effects were evidenced by representative images without quantitative analysis.
Consider that highly magnified representative images cannot describe population variation and the uncertainty of an observation.
A feature of virtual microscopy is the unbiased sampling of multi-scale image data, making it useful as a method to replicate representative images.
Results should be observed again with a high degree of reliability, therefore original claims should be evident in replicate microscopy maps.
To test this, Barkley challenged the claim that mammalian orthoreovirus remodels the endoplasmic reticulum (ER) of cells during infection [@doi:10.1128/mBio.01253-18].
This study was chosen because most results were representative images without quantification ([](#table4)).
A fully-motorized confocal microscope recorded large images from replicate immunofluorescence experiments at high-magnification.
Microscopy maps were embedded using the next generation file format OME-Zarr [@doi:10.1007/s00418-023-02209-1] and Vizarr viewer [@doi:10.1038/s41592-022-01482-7].
All parties have access to the same data from which Barkley interpreted that the key findings of the original study were not replicable.

Microscopy maps are interactive figures, but static figures predominate scientific publishing as an outdated relic of print journals.
Despite the benefits of virtual microscopy, representative images will persist until mainstream journals adopt modern visualization tools.
Given the widespread use of static figures in scientific discourse, the second chapter of this project was dedicated to computational image selection.
This follows a study critical of representative microscopy images that focused on methods of objective image selection to limit bias (https://doi.org/10.1016/s0006-3495(99)77379-0).
The authors implemented a web server that chose typical images from uploaded data, but it is now unsupported and there is no modern equivalent.
Representative image selection is an interesting use case for artificial intelligence.
Barkley automated the process of sample collection and image selection from a dataset of one million single-cell images of the [cell nucleus](<wiki:Cell_nucleus>), called _NucleusNet_.
Representative images were then selected from NucleusNet by an [autoencoder](<wiki:Autoencoder>) model.
Autoencoders are unsupervised deep learning models that compress and reconstruct images through a vector bottleneck referred to as _latent space_.
The structure of latent space is a [black box](<wiki:Black_box>), though it can be shaped to be more useful with the art of representation learning [@doi:10.1109/TPAMI.2013.50].
Representative images were defined near the centroid of latent space, though counter-examples show that this approach does not generalize.
To define what is representative, both the subjective determinations made by humans and the objective determinations made by autoencoders are opaque.
In contrast, microscopy maps offer greater transparency and accessibility compared to representative images as an alternative visual communication tool.

---

## Definitions

_Virtual microscopy_ is the process of sharing image data over computer networks.
A related term _virtual nanoscopy_ described the process of automated imaging with an electron microscope and unbiased data presentation using interactive viewers [@doi:10.1083/jcb.201201140].

A _microscopy map_ is the interactive figure used to view virtual microscopy data [@doi:10.1083/jcb.201201140].
This name fits broader use cases including light and electron microscopy.

A _representative image_ is defined as a visual communication tool used by microscopists to communicate research findings to other scientists.
This definition is agnostic to the research context and it emphasizes the use of pictures as scientific evidence.

A _grayscale image_ is defined as a two-dimensional matrix where each pixel is a single intensity value ranging from $0-1$ that represents the amount of light or intensity information at a specific point [@doi:10.1109/BIP60195.2023.10379342].

A _latent space_ is a collection of vectors that form a reduced-dimensionality embedding of the data, fit by a machine learning model [@doi:10.1111/cgf.13672].

---

:::{warning} AI disclosure
The text in this manuscript was written and edited by humans without AI assistance.
AI-generated code was used in the notebooks, autoencoder, and data processing tasks.
:::