---
title: Approach
numbering:
  enumerator: 2.%s
label : approach_page
---

---

# Embedded microscopy maps

This chapter criticizes the quality and reproducibility of representative microscopy images.
The problem is that immutable figures encourage scientists to cherry-pick desirable examples.
Scientists also lack tools to openly evaluate the replicability of microscopy experiments.
A solution is cloud-based [virtual microscopy](<wiki:Virtual_microscopy>); sharing image data over computer networks.
Often used for pedagogy, virtual microscopy could benefit scientific research.
Academics have proposed a variation of virtual microscopy for the unbiased presentation of transmission electron microscopy data [@doi:10.1083/jcb.201201140].
Today, there are free and open-source options [@doi:10.1242/jcs.262198] and recent advances in file formats [@doi:10.1007/s00418-023-02209-1] that have yet to be implemented in scientific journals.
Our approach to virtual microscopy involved automated image acquisition, multi-scale [pyramid](<wiki:Pyramid_(image_processing)>) file formats, and embedded interactive viewers ([](#abstract)).

```{figure} ./figures/Virtual_microscopy.png
:label: abstract
Cloud-based virtual microscopy. 1) Automated image acquisition with any suitable microscope. 2) Reformat data and host in the cloud. 3) Retrieve data chunks from cloud storage as readers interact with microscopy maps.
```

This journal supports two viewers; Vizarr [@doi:10.1038/s41592-022-01482-7] and [OpenSeadragon](https://openseadragon.github.io/) to demonstrate two methods of cloud-based virtual microscopy.

## Vizarr

OME-Zarr is a standardized and flexible file format developed for cloud-based microscopy applications [@doi:10.1007/s00418-023-02209-1].
Most native microscopy file formats can be converted to OME-Zarr with preserved metadata using [Bio-Formats](https://www.openmicroscopy.org/bio-formats/).
It is a chunked file format that can support multiple resolution levels.
Considered an advanced method of sharing microscopy maps [@doi:10.1242/jcs.262198], pyramidal OME-Zarr data (v0.4) was hosted in S3 storage and is viewed with Vizarr [@doi:10.1038/s41592-022-01482-7].

## OpenSeadragon

Another method, described elsewhere [@doi:10.1242/jcs.262198], is a free and open-source alternative for sharing microscopy maps.
Pyramidal Deep Zoom Image data was hosted on Github pages and tiles are streamed to the [OpenSeadragon](https://openseadragon.github.io/) viewer.
The reader cannot control dimensions like channels or time, so it is best suited for single-channel or composite microscopy images.