---
title: moxGFP::μNS
numbering:
  enumerator: 0.%s
---

:::{attention} Molecular biology example
Which moxGFP::μNS construct formed more condensates per cell? Left or right?
:::

::::{grid} 2 2 2 2
:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/moxGFPmuNS/FL.dzi"
}
:::
:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/moxGFPmuNS/MR.dzi"
}
:::
::::

:::{dropdown} Reveal the answer
moxGFP:μNS(1-721) (**left**) condenses more than moxGFP:μNS(472-721) (right).
:::

:::{dropdown} Methodological notes
CV-1 cells were seeded on 35mm glass-bottom dishes (20mm coverslips, no 1.5 glass).
pCI-neo moxGFP::μNS(1-721) and moxGFP::μNS(472-721) plasmids were transfected for 24 hours before PFA fixation.
2500 fields (50x50 grid) were imaged (100X objective).
Data was converted to 8-bit TIF, stitched, then converted to DZI format, hosted on Github Pages, and is viewed with OpenSeadragon.
:::