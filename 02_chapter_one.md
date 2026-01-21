---
title: Chapter One
numbering:
  enumerator: 2.%s
label : one_page
---

This article criticizes the quality and reproducibility of representative images.
The problem is that static figures encourage scientists to cherry-pick desirable examples.
Scientists also lack tools to evaluate the replicability of published representative images.
A solution is [virtual microscopy](<wiki:Virtual_microscopy>), sharing scientific images over computer networks.
Often used for pedagogy, virtual microscopy could benefit science.
Academics have proposed a variation of virtual microscopy for the unbiased presentation of transmission electron microscopy data [@doi:10.1083/jcb.201201140].
There are free and open-source methods [@doi:10.1242/jcs.262198] and recent advances in file formats [@doi:10.1007/s00418-023-02209-1] that have yet to be implemented in scientific journals.
Our approach to virtual microscopy is automated image acquisition, stitching a multi-scale [pyramid](<wiki:Pyramid_(image_processing)>), and an interactive viewer streaming data from the cloud ([](#abstract)).

```{figure} ./figures/Virtual_microscopy.png
:label: abstract
Figure Legend.
```

This journal currently supports two interactive viewers; Vizarr [@doi:10.1038/s41592-022-01482-7] and [OpenSeadragon](https://openseadragon.github.io/), which were embedded as demonstrations of cloud-based virtual microscopy.
Both methods of microscopy maps were implemented using software from open-source communities.

## Vizarr

OME-Zarr is a standardized and flexible format developed for cloud-based applications like virtual microscopy.
Most native microscopy file formats can be converted to OME-Zarr with preserved metadata using [Bio-Formats](https://www.openmicroscopy.org/bio-formats/).
It is a cloud-optimized chunked file format that can support multiple resolution levels [@doi:10.1007/s00418-023-02209-1].
Considered an advanced method [@doi:10.1242/jcs.262198], pyramidal OME-Zarr data hosted in S3 cloud storage can be viewed with Vizarr [@doi:10.1038/s41592-022-01482-7].
For our replication study, OME-Zarr data (v0.4) was hosted in Amazon Web Services S3 storage.

## OpenSeadragon

Another method, described elsewhere [@doi:10.1242/jcs.262198], is free and open-source.
Using pyramidal Deep Zoom Image data, hosted on Github pages, tiles are streamed to the [OpenSeadragon viewer](https://openseadragon.github.io/).
The reader has limited control of dimensions like channels and time, so it is best suited for single-channel or composite images like NucleusNet.