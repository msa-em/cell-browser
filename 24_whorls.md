---
title: OSER Assay
numbering:
  enumerator: 21.%s
---

Fluorescent proteins tend to oligomerize when confined to the ER, which can restructure the organelle into organized smooth ER (OSER) whorls [@doi:10.1083/jcb.200306020].
This artifact is used to assess the propensity of fluorescent proteins to oligomerize [@doi:10.1111/j.1600-0854.2012.01336.x].
Here, six fluorescent proteins were tested in an OSER assay using interactive microscopy maps.
Four of these fluorescent proteins can be cross-referenced with estimates of the percentage of cells expressing mEGFP (98.8±1.2), mCherry (95.0±0.8), FusionRed (91.5±3.0) and mNeonGreen (90.4±2.1) lacking visible OSER whorls [@doi:10.1038/nmeth.3891].

::::{grid} 2 2 2 2
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/oser_assay/fusionred.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "FusionRed-CytERM",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "scaleBar": {
    "maxWidth": 50,
    "position": "bottom-right",
    "fontSize": 10,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/oser_assay/mcherry.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-CytERM",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "scaleBar": {
    "maxWidth": 50,
    "position": "bottom-right",
    "fontSize": 10,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/oser_assay/dendra2.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "Dendra2-CytERM",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "scaleBar": {
    "maxWidth": 50,
    "position": "bottom-right",
    "fontSize": 10,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/oser_assay/megfp.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mEGFP-CytERM",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "scaleBar": {
    "maxWidth": 50,
    "position": "bottom-right",
    "fontSize": 10,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/oser_assay/mneongreen.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mNeonGreen-CytERM",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "scaleBar": {
    "maxWidth": 50,
    "position": "bottom-right",
    "fontSize": 10,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/oser_assay/moxgfp.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "moxGFP-CytERM",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "scaleBar": {
    "maxWidth": 50,
    "position": "bottom-right",
    "fontSize": 10,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
::::

:::{dropdown} Methods
3e5 HeLa cells were seeded on 35mm glass-bottom dishes.
An OSER assay was performed with six fluorescent proteins cloned into the CytERM plasmid.
2.5µg was transfected with lipofectamine 3000 for 24 hours before PFA fixation and automated imaging of 15x15 (225 field) grids with a 100X objective lens.
Illumination settings, including excitation/emission, were adjusted individually.
mEGFP, moxGFP, Dendra2 and mNeongreen used the same wavelengths.
:::