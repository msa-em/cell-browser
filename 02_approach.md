---
title: Approach
numbering:
  enumerator: 1.%s
---

Already adopted by some clinicians and educators, virtual microscopy could also benefit researchers as an interface for communicating and interpreting image data.
Indeed, interactive microscopy maps were proposed as an unbiased way to present electron microscopy data [@doi:10.1083/jcb.201201140].
Free and open-source solutions [@doi:10.1242/jcs.262198] and recent advances in file formats [@doi:10.1007/s00418-023-02209-1] now make this feasible, yet virtual microscopy remains rare in scientific publishing.
Most journals publish articles as static pages that cannot run code, so interactive figures must be provided as links to external pages.
Even [Elsevier's Virtual Microscope](https://www-prod.elsevier.com/researcher/author/tools-and-resources/data-visualization/virtual-microscope) is opened from links in figure captions.
To our knowledge, Elemental Microscopy is among the first journals that allows interactive viewers to be embedded directly within the article, so each figure is a live view of the full-resolution dataset rather than a static rendering.
Here we describe a workflow for this kind of virtual microscopy: datasets are acquired automatically, converted to multi-scale [pyramid](<wiki:Pyramid_(image_processing)>) formats, hosted in the cloud, and streamed to viewers embedded in a paper ([](#abstract)).

```{figure} ./figures/Virtual_microscopy.png
:label: abstract
Virtual microscopy. 1. Automated dataset collection with any suitable microscope. ZDC: Z-drift compensation. 2. Stitch tiles then convert the image to DZI or OME-Zarr, host online. 3. Image tiles or data chunks are retrieved from cloud storage as readers interact with microscopy maps.
```

Elemental Microscopy natively supports two interactive viewers; [Vizarr](https://github.com/hms-dbmi/vizarr) [@doi:10.1038/s41592-022-01482-7] and [OpenSeadragon](https://openseadragon.github.io/), which enable virtual microscopy of OME-Zarr and Deep Zoom images, respectively.
To use either viewer, authors copy the provided markdown and replace the source URL with a link to their own data.
Authors can also build custom viewers and embed them within their online articles.
Brodrick developed [microATLAS](https://github.com/LadInTheLab/microATLAS-widget) to present the large multiplexed immunofluorescence datasets in this article, and its [widget builder](https://ladinthelab.github.io/microATLAS-widget/builder.html) generates embedding code that specifies both the image and its display settings.
We also collaborated with the developers of [Find Nuclei](https://www.find-nuclei.com/), a browser-based dashboard for OME-Zarr datasets, so that its toolbar embed button generates MyST code for embedding the viewer in Elemental Microscopy articles [@FindNuclei2026].

The four figures below are interactive microscopy maps for readers to try, each showing the same demo dataset: a mosaic of around one million nucleus images [@doi:10.5281/zenodo.18776682].
This data is not analyzed in this article; it is included only to show how each viewer handles very large images.
Three figures stream OME-Zarr data from cloud object storage to Vizarr, microATLAS and Find Nuclei, while the fourth streams a smaller Deep Zoom (DZI) subset from GitHub Pages to OpenSeadragon.
Each viewer is embedded with a single MyST directive, shown below its figure.
For Vizarr and OpenSeadragon, authors replace the source URL with a link to their own data, while microATLAS and Find Nuclei generate the embedding code, so adding an interactive figure amounts to pasting a block of markup.

## OME-Zarr

OME-Zarr is a standardized and flexible image format developed for use cases like virtual microscopy [@doi:10.1007/s00418-023-02209-1].
Most native microscopy file formats can be converted to OME-Zarr with preserved metadata using [Bio-Formats](https://www.openmicroscopy.org/bio-formats/).
It is a chunked file type that can support multiple resolution levels.
As an advanced implementation of microscopy maps [@doi:10.1242/jcs.262198], pyramidal OME-Zarr data can be viewed online [@doi:10.1038/s41592-022-01482-7].

### Vizarr

```{iframe} https://hms-dbmi.github.io/vizarr/?source=https://nyu1.osn.mghpcc.org/barkley-replication/nuclei_mosaic.zarr&viewState={%22target%22:[124547.79378129813,32310.74580437236],%22zoom%22:-3.8361114954494266}
:width: 100%
```

```{code} markdown
:label: vizarr_code
:caption: Minimal markdown to embed Vizarr in Elemental Microscopy. Replace the source with your data.
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/nuclei_mosaic.zarr",
  "height": "600px"
}
:::
```

### microATLAS

:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/nuclei_mosaic.zarr",
  "width": "600px",
  "height": "600px",
  "views": [
    {
      "name": "inferno",
      "zoom": -2.866,
      "target": [
        137103,
        166506,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true
        ],
        "channelColors": [
          [
            255,
            255,
            255
          ]
        ],
        "contrastLimits": [
          [
            0,
            255
          ]
        ],
        "blendMode": "merged",
        "colormap": "inferno"
      },
      "default": true
    }
  ]
}
:::

```{code} markdown
:label: microatlas_code
:caption: Example markdown to embed microATLAS in Elemental Microscopy. Create your own with the [builder](https://ladinthelab.github.io/microATLAS-widget/builder.html).
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/nuclei_mosaic.zarr",
  "width": "600px",
  "height": "600px"
}
:::
```

### Find Nuclei

:::{any:bundle} https://find-nuclei.github.io/embed/v1/widget.mjs
{
  "url": "https://nyu1.osn.mghpcc.org/barkley-replication/nuclei_mosaic.zarr",
  "channels": "0:on:FFFFFF:0:240",
  "x": 2115, "y": 1688, "zoom": -1.9,
  "height": "600",
  "invert": true
}
:::

```{code} markdown
:label: findnuclei_code
:caption: Example markdown to embed [Find Nuclei](https://www.find-nuclei.com/) in Elemental Microscopy [@FindNuclei2026].
:::{any:bundle} https://find-nuclei.github.io/embed/v1/widget.mjs
{
  "url": "https://nyu1.osn.mghpcc.org/barkley-replication/nuclei_mosaic.zarr",
  "channels": "0:on:FFFFFF:0:240",
  "x": 2115, "y": 1688, "zoom": -1.9,
  "height": "600",
  "invert": true
}
:::
```

## Deep Zoom

[Deep Zoom](<wiki:Deep_Zoom>) is a free and open-source solution, described elsewhere [@doi:10.1242/jcs.262198], now embeddable in Elemental Microscopy.
Pyramidal Deep Zoom image (DZI) data hosted on Github Pages is streamed to the [OpenSeadragon](https://openseadragon.github.io/) viewer.
By default, readers cannot control dimensions like channels or time, so it is best suited for single-channel or composite images.

### OpenSeadragon

:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/nucleusnet-10k/nucleusnet_10k.dzi"
}
:::

```{code} markdown
:label: openseadragon_code
:caption: Minimal markdown to embed OpenSeadragon in Elemental Microscopy. Replace the source with your DZI.
:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/nucleusnet-10k/nucleusnet_10k.dzi"
}
:::
```
