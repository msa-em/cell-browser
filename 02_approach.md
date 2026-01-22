---
title: Approach
numbering:
  enumerator: 2.%s
label : approach_page
---

---

# Chapter One

This section criticizes the quality and reproducibility of representative microscopy images.
The problem is that immutable figures encourage scientists to cherry-pick desirable examples.
Scientists also lack the tools to evaluate the replicability of published representative images.
A solution is [virtual microscopy](<wiki:Virtual_microscopy>); sharing image data over computer networks.
Often used for pedagogy, virtual microscopy could benefit research.
Academics have proposed a variation of virtual microscopy for the unbiased presentation of transmission electron microscopy data [@doi:10.1083/jcb.201201140].
Today, there are free and open-source methods [@doi:10.1242/jcs.262198] and recent advances in file formats [@doi:10.1007/s00418-023-02209-1] that have yet to be implemented in scientific journals.
Our approach to virtual microscopy involved automated image acquisition, a stitched multi-scale [pyramid](<wiki:Pyramid_(image_processing)>), and an embedded interactive viewer ([](#abstract)).
This journal supported two viewers; Vizarr [@doi:10.1038/s41592-022-01482-7] and [OpenSeadragon](https://openseadragon.github.io/), which were embedded to demonstrate methods of virtual microscopy.

```{figure} ./figures/Virtual_microscopy.png
:label: abstract
Figure Legend.
```

## Vizarr

OME-Zarr is a standardized and flexible format developed for cloud-based applications like virtual microscopy [@doi:10.1007/s00418-023-02209-1].
Most native microscopy file formats can be converted to OME-Zarr with preserved metadata using [Bio-Formats](https://www.openmicroscopy.org/bio-formats/).
It is a cloud-optimized chunked file format that can support multiple resolution levels.
Considered an advanced method [@doi:10.1242/jcs.262198], pyramidal OME-Zarr data (v0.4) hosted in S3 cloud storage is viewed with Vizarr [@doi:10.1038/s41592-022-01482-7].

## OpenSeadragon

Another method described elsewhere [@doi:10.1242/jcs.262198] is free and open-source.
Using pyramidal Deep Zoom Image data, hosted on Github pages, tiles are streamed to the [OpenSeadragon viewer](https://openseadragon.github.io/).
The reader has limited control of dimensions like channels and time, so it is best suited for single-channel or composite images.