---
title: Approach
numbering:
  enumerator: 2.%s
label : approach_page
---

---

# Embedded microscopy maps

This section criticizes the quality and reproducibility of representative microscopy images.
The problem is that immutable figures encourage scientists to cherry-pick desirable examples.
Scientists also lack the tools to evaluate the replicability of published representative images.
A solution is [virtual microscopy](<wiki:Virtual_microscopy>); sharing image data over computer networks.
Often used for pedagogy, virtual microscopy could benefit research.
Academics have proposed a variation of virtual microscopy for the unbiased presentation of transmission electron microscopy data [@doi:10.1083/jcb.201201140].
Today, there are free and open-source methods [@doi:10.1242/jcs.262198] and recent advances in file formats [@doi:10.1007/s00418-023-02209-1] that have yet to be implemented in scientific journals.
Our approach to virtual microscopy involved automated image acquisition, stitched multi-scale [pyramid](<wiki:Pyramid_(image_processing)>) formats, and embedded interactive viewers ([](#abstract)).
This journal supports two viewers; Vizarr [@doi:10.1038/s41592-022-01482-7] and [OpenSeadragon](https://openseadragon.github.io/) that were used to demonstrate cloud-based virtual microscopy.

```{figure} ./figures/Virtual_microscopy.png
:label: abstract
General approach to cloud-based virtual microscopy. 1) Automated image acquisition with a microscope. 2) Convert microscopy data to a pyramidal format, host in the cloud. 3) Retrieve chunks of data from the cloud as readers interact with viewers embedded in the article.
```

## Vizarr

OME-Zarr is a standardized and flexible format developed for cloud-based applications like virtual microscopy [@doi:10.1007/s00418-023-02209-1].
Most native microscopy file formats can be converted to OME-Zarr with preserved metadata using [Bio-Formats](https://www.openmicroscopy.org/bio-formats/).
It is a cloud-optimized chunked file format that can support multiple resolution levels.
Considered an advanced method [@doi:10.1242/jcs.262198], pyramidal OME-Zarr data (v0.4) was hosted in S3 cloud storage and is viewed with Vizarr [@doi:10.1038/s41592-022-01482-7].

## OpenSeadragon

Another method, described elsewhere [@doi:10.1242/jcs.262198], was implemented as a free and open-source option to share microscopy maps.
Using pyramidal Deep Zoom Image data, hosted on Github pages, tiles are streamed to the [OpenSeadragon viewer](https://openseadragon.github.io/).
The reader cannot control dimensions like channels or time, so it is best suited for single-channel or composite microscopy images.