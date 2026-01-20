---
title: Background
numbering:
  enumerator: 2.%s
label : background_page
---

This article concerns the quality of representative images as scientific evidence and recommends virtual microscopy as an alternative.
[Virtual microscopy](<wiki:Virtual_microscopy>) is the process of sharing image data over computer networks.
Often used for pedagogy, virtual microscopy could benefit science and the acquisition of knowledge from a microscope.
Academics proposed a variation of virtual microscopy for the unbiased presentation of transmission electron microscopy data [@doi:10.1083/jcb.201201140] as an improvement to representative images.
There are several software options to this end [@doi:10.1242/jcs.262198] and recent advances in file formats [@doi:10.1007/s00418-023-02209-1] that have yet to be implemented in scientific journals.
The general approach to virtual microscopy involves automated image acquisition from a microscope, followed by stitching a multi-scale [pyramid](<wiki:Pyramid_(image_processing)>) that is streamed to interactive viewers over computer networks ([](#abstract)).

```{figure} ./figures/Virtual_microscopy.png
:label: abstract
Figure Legend.
```

The Elemental Microscopy journal supports two open-source viewers; Vizarr [@doi:10.1038/s41592-022-01482-7] and [OpenSeadragon] (https://openseadragon.github.io/), which were both embedded into the article as demonstrations of virtual microscopy to readers.
These two methods were made possible with software from several open-source communities, as well as cloud resources.

## Vizarr

Considered an advanced method [@doi:10.1242/jcs.262198], microscopy maps can be made from pyramidal OME-Zarr data hosted in S3 cloud storage.
OME-Zarr data is a cloud-optimized chunked file format that can support multiple resolution levels [@doi:10.1007/s00418-023-02209-1].
Most native microscopy file formats can be reformatted to OME-Zarr with preserved metadata using [Bio-Formats](https://www.openmicroscopy.org/bio-formats/).
In the replication study, OME-Zarr data (v0.4) was hosted in Amazon Web Services S3 storage, which is streamed to Vizarr [@doi:10.1038/s41592-022-01482-7] as readers interact with the figure.

## OpenSeadragon

An alternative method was shown in the second chapter of this article based on free and open-source options [@doi:10.1242/jcs.262198].
This approach uses the Deep Zoom Image format, hosted in a Github repository, read by the [OpenSeadragon viewer](https://openseadragon.github.io/).
The reader has limited control of dimensions like channels or time, so it is best suited for single-channel or composite images like NucleusNet.