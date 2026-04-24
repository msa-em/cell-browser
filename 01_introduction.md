---
title: Introduction
numbering:
  enumerator: 0.%s
---

Representative microscopy images are visual communication tools used by microscopists to present research results to other scientists.
The earliest representative microscopy images were hand-drawn in Robert Hooke's [Micrographia](<wiki:Micrographia>) in 1665.
Today, roughly three-quarters of publications in biomedical journals report at least one microscopy image [@doi:10.7554/eLife.55133].
There is an unspoken expectation that scientists rely on these images to be honest and accurate.
However, microscopy image selection and quantitative analyses thereof are vulnerable to bias and deception [@doi:10.1242/jcs.261567].
Besides cherry-picking, scientists can sincerely misinterpret observations.
The problem is that readers find it difficult to critically evaluate representative images.
Furthermore, archival and review of primary microscopy data is disorganized and time-consuming, if at all available.
These problems can be addressed with novel visualization strategies like [virtual microscopy](<wiki:Virtual_microscopy>) that transmit entire interactive datasets over the internet.
An example is the unbiased presentation of electron microscopy data to readers as interactive digital maps; microscopy maps [@doi:10.1083/jcb.201201140].
In practice, microscopy maps are easy to share but are accessed via external links [@doi:10.1242/jcs.262198].

[Reproducibility](<wiki:Reproducibility>) is an essential principle of the [scientific method](<wiki:Scientific_method>) for acquiring knowledge, yet there is a contentious [reproducibility crisis](<wiki:Replication_crisis>) in science.
From the perspective of biomedical researchers, the perceived cause is the pressure to publish [@doi:10.1371/journal.pbio.3002870].
Repeatability within the same study by the same researchers is distinguished from replicability by independent researchers using the same methodology.
Large-scale replicability studies found that only 11% [@doi:10.1038/483531a] and 25% [@doi:10.1038/nrd3439-c1] of key findings from preclinical cancer research papers were replicable.
Another study found that, even at its 'lowest bar' criterion, the replication success rate was 79% for representative images [@doi:10.7554/eLife.71601].
Furthermore, representative images without quantitative analysis accounted for 26% of the claimed effects.
Consider that highly magnified representative images cannot describe population variation and the uncertainty of an observation.
A feature of virtual microscopy is the unbiased sampling and transmission of multi-scale image data, making it useful as a method to replicate representative images.
Results should be observed again with a high degree of reliability; therefore original claims should be evident in replicate microscopy maps.

Here, microscopy maps were used to reassess the claim that mammalian orthoreovirus remodels the endoplasmic reticulum (ER) of cells during infection [@doi:10.1128/mBio.01253-18].
This study was qualitative because most of the results were representative microscopy images without quantification.
Using the protocols described in the original paper, hundreds of overlapping tiles were sampled at high-magnification from replicate immunofluorescence experiments on a fully motorized confocal microscope.
Microscopy maps were embedded in the article using the next generation file format OME-Zarr [@doi:10.1007/s00418-023-02209-1] and custom viewers based on Viv [@doi:10.1038/s41592-022-01482-7].

:::{warning} AI disclosure
The text in this manuscript was written and edited by humans without AI assistance.
AI-generated code was used in the notebooks, autoencoder, and data processing tasks.
:::

:::{dropdown} Definitions
_Virtual microscopy_ is the process of sharing image data over computer networks.
A related term _virtual nanoscopy_ described the process of automated imaging and unbiased presentation of electron microscopy data using interactive viewers [@doi:10.1083/jcb.201201140].

A _microscopy map_ is the interactive figure used to view virtual microscopy data [@doi:10.1083/jcb.201201140].
This name fits broader use cases including light and electron microscopy.

A _representative image_ is an illustration used by microscopists to exemplify research results to other scientists.
This definition is agnostic to the research context and it emphasizes the use of pictures as scientific evidence.

A _grayscale image_ is defined as a two-dimensional matrix where each pixel is a single intensity value ranging from 0-1 that represents the amount of light or intensity information at a specific point [@doi:10.1109/BIP60195.2023.10379342].

A _latent space_ is a collection of vectors that form a reduced-dimensionality embedding of the data, fit by a machine learning model [@doi:10.1111/cgf.13672].
:::