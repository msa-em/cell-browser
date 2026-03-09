---
title: Approach
numbering:
  enumerator: 1.%s
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
Cloud-based virtual microscopy. 1. Automated image acquisition with any suitable microscope. 2. Stitch and reformat to pyramidal DZI or OME-Zarr and host online. 3) As readers interact with embedded microscopy maps, image tiles or data chunks are retrieved from cloud storage.
```

Elemental Microscopy supports two interactive viewers; [Vizarr](https://github.com/hms-dbmi/vizarr) [@doi:10.1038/s41592-022-01482-7] and [OpenSeadragon](https://openseadragon.github.io/), enabling two alternative methods of virtual microscopy with OME-Zarr or Deep Zoom.
Authors can also build custom viewers.
Brodrick developed [microATLAS](https://github.com/LadInTheLab/microATLAS-widget), the OME-Zarr viewer used in this article.
[Vizarr](#vizarr), [OpenSeadragon](#openseadragon) and [microATLAS](#microatlas) are readily embeddable with the `:::{any:bundle}` directive.

## OME-Zarr

OME-Zarr is a standardized and flexible image format developed for use cases like virtual microscopy [@doi:10.1007/s00418-023-02209-1].
Most native microscopy file formats can be converted to OME-Zarr with preserved metadata using [Bio-Formats](https://www.openmicroscopy.org/bio-formats/).
It is a chunked file type that can support multiple resolution levels.
Considered an advanced implementation of microscopy maps [@doi:10.1242/jcs.262198], pyramidal OME-Zarr data can be viewed online [@doi:10.1038/s41592-022-01482-7].

### Vizarr

```{code}
:label: vizarr
:caption: Minimal markdown to embed Vizarr in Elemental Microscopy. Replace the source with your data.
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://your-bucket.s3.amazonaws.com/sample.zarr/",
  "height": "600px"
}
:::

```

### microATLAS

```{code}
:label: microatlas
:caption: Example markdown to embed microATLAS in Elemental Microscopy. Create your own with the [builder](https://ladinthelab.github.io/microATLAS-widget/builder.html).
:::{any:bundle} https://ladinthelab.github.io/microATLAS-widget/widget.js
{
  "source": "https://your-bucket.s3.amazonaws.com/sample.zarr/",
  "views": [
    {
      "name": "Overview",
      "zoom": -4,
      "target": [4886, 4886, 0]
    }
  ],
  "annotations": [
    { "name": "Region A", "target": [2400, 2400], "color": [100, 200, 255] }
  ],
  "scaleBar": { "maxWidth": 120, "position": "bottom-right" }
}
:::
```

## Deep Zoom

A free and open-source solution, described elsewhere [@doi:10.1242/jcs.262198], is now embeddable in Elemental Microscopy.
Pyramidal Deep Zoom image (DZI) data hosted on Github Pages is streamed to the [OpenSeadragon](https://openseadragon.github.io/) viewer.
By default, readers cannot control dimensions like channels or time, so it is best suited for single-channel or composite images like NucleusNet.

### OpenSeadragon

```{code}
:label: openseadragon
:caption: Minimal markdown to embed OpenSeadragon in Elemental Microscopy. Replace the source with your DZI.
:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://your-github.github.io/your-repository/sample.dzi"
}
:::
```