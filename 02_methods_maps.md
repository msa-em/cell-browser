---
title: Maps
numbering:
  enumerator: 2.%s
label : maps_page
---

This article is concerned with the quality of representative images as scientific evidence and recommends virtual microscopy as an alternative visual communication tool.
Virtual microscopy is the process of sharing image data over computer networks, now used for pedagogy.
For the reader it simulates the process of looking down a microscope, allowing dynamic access to lots of high-magnification image data.
In academia, a variation of this approach was demonstrated for the unbiased communication of transmission electron microscopy data as microscopy maps [@doi:10.1083/jcb.201201140].
There are many software options to make and view microscopy maps [@doi:10.1242/jcs.262198].
The general approach involves automated image acquisition from a microscope, then tiles are stitched into a multi-scale [pyramid](<wiki:Pyramid_(image_processing)>) to be read by tile-based viewers.
A limitation to microscopy maps is the requirement to publish in static figures.
Therefore, we embedded microscopy maps into this article as a proof-of-principle demonstration of virtual microscopy in the scientific literature ([](#abstract))
This was made possible using the interactive capabilities of this journal and technologies from several open-source communities.
Two methods based on different file formats and viewers were shown in this article.

```{figure} ./figures/Virtual_microscopy.png
:label: abstract
Figure Legend.
```

## Vizarr

An advanced method to share microscopy maps is to use the OME-Zarr file format hosted in S3 cloud storage [@doi:10.1242/jcs.262198].
OME-Zarr is a cloud-optimized chunked file format that can support multiple resolution levels [@doi:10.1007/s00418-023-02209-1].
This data structure makes it suitable to stream from cloud storage to interactive viewers like Vizarr [@doi:10.1038/s41592-022-01482-7], which this journal supports.
Most native microscopy file formats can be reformatted to OME-Zarr with preserved metadata using [Bio-Formats](https://www.openmicroscopy.org/bio-formats/).
In this study, OME-Zarr data (v0.4) was hosted in Amazon Web Services S3 storage for retrieval by Vizarr.

## OpenSeadragon

A free and open-source method used the pyramidal Deep Zoom Image format and [OpenSeadragon viewer](https://openseadragon.github.io/) to host microscopy maps on Github [@doi:10.1242/jcs.262198].
This is an alternative approach that displays tiles in common image formats like JPEG.
The reader has limited control over dimensions like channel or time, so it is best suited for single-channel or composite images.
Data from NucleusNet in the second chapter of this article was presented using embedded OpenSeadragon viewers and Deep Zoom Image tiles hosted on Github.