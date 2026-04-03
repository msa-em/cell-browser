---
title: moxGFP::μNS
numbering:
  enumerator: 17.%s
---

Here, data related to moxGFP::μNS(1-721) and moxGFP::μNS(472-721) biomolecular condensation was represented as interactive maps.
We studied the distributions of moxGFP::μNS condensates and found that moxGFP::μNS(1-721) nucleated better than moxGFP::μNS(472-721) [@doi:10.1091/mbc.E24-01-0013].

### Which moxGFP::μNS construct formed more condensates?

:::{dropdown} Click to reveal the answer:
moxGFP:μNS(1-721) (**left**) tends to condense more than moxGFP:μNS(472-721) (right).
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

:::{dropdown} Methods
CV-1 cells were seeded on 35mm glass-bottom dishes (20mm coverslips, no 1.5 glass).
pCI-neo moxGFP::μNS(1-721) and moxGFP::μNS(472-721) plasmids were transfected for 24 hours before PFA fixation.
2500 fields (50x50 grid) were imaged (100X objective).
Data was converted to 8-bit TIF, stitched, then converted to DZI format, hosted on Github Pages, and is viewed with OpenSeadragon.
:::

### Recording the formation of moxGFP::μNS condensates.

Published data was converted to OME-Zarr for visualization as interactive microscopy maps [@doi:10.1091/mbc.E24-01-0013].
CV-1 cells expressing moxGFP::μNS were imaged live at 4-5 hours post-transfection to monitor the nucleation of nascent factories at ~5 minute intervals.

::::{grid} 2 2 2 2
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/nucleation/2022-09-29_FL.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "moxGFP::μNS(1-721)",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Loop",
      "zoom": -3.995,
      "target": [
        2560,
        2560,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true,
          false,
          false
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            255,
            0,
            255
          ],
          [
            255,
            255,
            255
          ]
        ],
        "contrastLimits": [
          [
            0,
            4095
          ],
          [
            0,
            4095
          ],
          [
            0,
            4095
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "playback": {
        "playing": true,
        "fps": 24,
        "startFrame": 1
      },
      "default": true
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 10,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/nucleation/2022-09-28_MR.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "moxGFP::μNS(472-721)",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Loop",
      "zoom": -3.995,
      "target": [
        2560,
        2560,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true,
          false,
          false
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            255,
            0,
            255
          ],
          [
            255,
            255,
            255
          ]
        ],
        "contrastLimits": [
          [
            0,
            4095
          ],
          [
            0,
            4095
          ],
          [
            0,
            4095
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "playback": {
        "playing": true,
        "fps": 24,
        "startFrame": 1
      },
      "default": true
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 10,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
::::

:::{dropdown} Methods
See _Droplet nucleation time-lapse experiments_ in the materials and methods [@doi:10.1091/mbc.E24-01-0013].
The plasma membrane was stained with Vybrant DiD cell-labeling solution, which is hidden by default.
:::