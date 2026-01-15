---
title: Introduction
numbering:
  enumerator: 1.%s
label : introduction_page
---

Representative microscopy images are visual communication tools used by microscopists to present the results of research to other scientists.
The earliest representative microscopy images were hand drawings in [Micrographia](<wiki:Micrographia>) in 1665 by Robert Hooke.
Nowadays, roughly three-quarters of publications in biomedical journals report at least one microscopy image [@doi:10.7554/eLife.55133].
In scientific journals, microscopists show stereotypical images of observations in static figures.
An un-spoken rule is that scientists trust the representative image is honest and accurate.
However, microscopy image selection and quantitative analyses thereof are vulnerable to bias and deception [@doi:10.1242/jcs.261567].
Aside from research integrity, scientists sincerely misinterpret observations.
The problem is that it is difficult for readers to critically evaluate experiments that show representative images in static figures.
Furthermore, archival and review of primary microscopy data is disorganized and time-consuming if at all available.
These limitations can be overcome with interactive visualization stategies like virtual nanoscopy [@doi:10.1083/jcb.201201140].
Virtual nanoscopy is the idea that microscopy data can be presented as an interactive zoomable map; a microscopy map.
In practice, microscopy maps are easy to implement, but dynamic browsing needs external links or software [@doi:10.1242/jcs.262198].
As a proof of principle, microscopy maps were embedded in this paper to pilot virtual nanoscopy in the scientific literature.

[Reproducibility](<wiki:Reproducibility>) is an essential principle of the [scientific method](<wiki:Scientific_method>) for acquiring knowledge.
Microscopists contribute to the [reproducibility crisis](<wiki:Replication_crisis>) in science, which is being adressed through protocol standardization [@doi:10.1111/jmi.13041].
From the perspective of biomedical researchers, the perceived cause is the pressure to publish [@doi:10.1371/journal.pbio.3002870].
Repeatability in the same study by the same researchers is distinguished from replicability by independent researchers using the same methodology.
Large-scale replicability studies performed by scientists at Amgen and Bayer assessed that 11% [@doi:10.1038/483531a] and 25% [@doi:10.1038/nrd3439-c1] of key findings from preclinical cancer research papers were robust and replicable.
Another reproducibility project evaluated replication success with other criteria, though the 'lowest bar' determined a replication rate of 79% for representative images [@doi:10.7554/eLife.71601].
Notably, 26% of claimed effects were originally evidenced by a representative image without quantitative analysis.
Consider that representative images cannot describe population variation and the uncertainty of an observation.
Microscopy maps show population effects, making them useful as a method for replicating published representative images.
Results should be observed again with a high degree of reliability, therefore original claims should be apparent in microscopy maps.
To test this, Barkley challenged the claim that mammalian orthoreovirus remodels the endoplasmic reticulum (ER) of cells [@doi:10.1128/mBio.01253-18].
This study was appropriate for replication because most experiments reported representative light or electron microscopy images without numerical results.
An immunofluorescence experiment was replicated and the coverslips were imaged with an automated confocal microscope.
The replication study was supported with [OrganelleBox](https://organellebox.sf.czbiohub.org) to cross-validate and expand the virtual nanoscopy study to sixteen organelles during reovirus infection.
Embedded microscopy maps were based on the OME-Zarr next generation file format (cite) 
pyramidal OME-Zarr data is retrieved from cloud storage as readers interact with the viewer.

An opposite approach to preventing bias in representative images is to automate image selection.
A study critical of representative microscopy images focused on methods of objective image selection to limit bias (https://doi.org/10.1016/s0006-3495(99)77379-0).
The authors implemented a web server that chose typical images from uploaded data, but it is now unsupported and there is no modern equivalent.
We started by revisiting the idea of objective image selection, as Barkley and Parker thought it was an interesting use case for artificial intelligence.
Barkley automated the process of sample collection and image selection from a collection of one million single-cell images of the [cell nucleus](<wiki:Cell_nucleus>), called _NucleusNet_.
Stitched panoramas and cropped images were presented in interactive figures, including microscopy maps.
Representative images were then selected from NucleusNet by an [autoencoder](<wiki:Autoencoder>) model.
Autoencoders are unsupervised deep learning models that compress and reconstruct images through a vector bottleneck referred to as _latent space_.
The structure of latent space is a [black box](<wiki:Black_box>), though it can be shaped to be more useful with the art of representation learning [@doi:10.1109/TPAMI.2013.50].
Representative images were defined as encoded images near the centroid of latent space, though counter-examples showed that this method did not generalize.
With an uninterpretable embedding space, Barkley found that it would be irresponsible to use autoencoders for the task of image selection.
To define what is representative, both the subjective determinations made by humans and the objective determinations made by autoencoders are opaque.
In contrast, microscopy maps offer greater transparency and accessibility as a visual communication tool compared to representative images.

---

## Definitions

_Virtual nanoscopy_ was a term used to describe the process of automated image acquisition, followed by unbiased presentation in an interactive tile-based viewer. [@doi:10.1083/jcb.201201140]

_Microscopy map_ is the interactive figure used to view virtual nanoscopy data. [@doi:10.1083/jcb.201201140]
The original term '_electron_ microscopy map' was redefined to fit a broader use case because our study used confocal microscopy data.

A _representative image_ is defined as a visual communication tool used by microscopists to communicate research findings to other scientists.
This definition is agnostic to the research context and it emphasizes the use of pictures as scientific evidence.
Parker suggested that _stereotypical image_ would be an apt name for the current use of representative images.

A _grayscale image_ is defined as a two-dimensional matrix where each pixel is a single intensity value ranging from $0-1$ that represents the amount of light or intensity information at a specific point [@doi:10.1109/BIP60195.2023.10379342].

A _latent space_ is a collection of vectors that form a reduced-dimensionality embedding of the data, fit by a machine learning model [@doi:10.1111/cgf.13672].
