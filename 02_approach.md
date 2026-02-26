---
title: Approach
numbering:
  enumerator: 1.%s
label : approach_page
---

# Embedded microscopy maps

This chapter critiques the quality and reproducibility of representative microscopy images as scientific evidence.
The problem is that static figures motivate authors to cherry-pick desirable examples.
Scientists also lack tools to evaluate the replicability of claims from representative images.
A solution is cloud-based [virtual microscopy](<wiki:Virtual_microscopy>); using the internet to share image data.
Often used for pedagogy and digital pathology, virtual microscopy could benefit research.
Academics have proposed a variation of virtual microscopy for the unbiased presentation of electron microscopy data [@doi:10.1083/jcb.201201140].
Today, there are free and open-source solutions [@doi:10.1242/jcs.262198] and recent advances in file formats [@doi:10.1007/s00418-023-02209-1] that have yet to be used in scientific publishing.
Our approach involved automated image acquisition, multi-scale [pyramid](<wiki:Pyramid_(image_processing)>) file formats, and embedded interactive viewers ([](#abstract)).

```{figure} ./figures/Virtual_microscopy.png
:label: abstract
Cloud-based virtual microscopy. 1. Automated image acquisition with any suitable microscope. 2. Reformat data to a pyramidal format like DZI or OME-Zarr and host online. 3) As readers interact with embedded microscopy maps, image tiles or data chunks are retrieved from cloud storage.
```

The Elemental Microscopy journal supports two viewers; [Vizarr](https://github.com/hms-dbmi/vizarr) [@doi:10.1038/s41592-022-01482-7] and [OpenSeadragon](https://openseadragon.github.io/), enabling two alternative methods of cloud-based virtual microscopy.

## Vizarr

OME-Zarr is a standardized and flexible image format developed for use cases like virtual microscopy [@doi:10.1007/s00418-023-02209-1].
Most native microscopy file formats can be converted to OME-Zarr with preserved metadata using [Bio-Formats](https://www.openmicroscopy.org/bio-formats/).
It is a chunked file type that can support multiple resolution levels.
Considered an advanced implementation of microscopy maps [@doi:10.1242/jcs.262198], pyramidal OME-Zarr data (v0.4) was hosted in S3 storage and is viewed with Vizarr [@doi:10.1038/s41592-022-01482-7].

## OpenSeadragon

A free and open-source solution, described elsewhere [@doi:10.1242/jcs.262198], was also demonstrated.
Pyramidal Deep Zoom image (DZI) data was hosted on Github Pages and tiles are streamed to the [OpenSeadragon](https://openseadragon.github.io/) viewer.
Readers cannot control dimensions like channels or time, so it is best suited for single-channel or composite images like NucleusNet.