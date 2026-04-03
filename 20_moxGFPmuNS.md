---
title: moxGFP::μNS
numbering:
  enumerator: 17.%s
---

Here, data related to moxGFP::μNS(1-721) and moxGFP::μNS(472-721) biomolecular condensation was represented as interactive maps.
Barkley studied the distribution of condensates formed by these constructs with representative images and quantitative analyses, see Figure 4 [@doi:10.1091/mbc.E24-01-0013].
The conclusion was that moxGFP::μNS(1-721) condensed better than moxGFP::μNS(472-721).

### Which moxGFP::μNS construct formed more condensates?

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
moxGFP:μNS(1-721) (**left**) tends to condense more than moxGFP:μNS(472-721) (right).
:::

:::{dropdown} Methods
CV-1 cells were seeded on 35mm glass-bottom dishes (20mm coverslips, no 1.5 glass).
pCI-neo moxGFP::μNS(1-721) and moxGFP::μNS(472-721) plasmids were transfected for 24 hours before PFA fixation.
2500 fields (50x50 grid) were imaged (100X objective).
Data was converted to 8-bit TIF, stitched, then converted to DZI format, hosted on Github Pages, and is viewed with OpenSeadragon.
:::

### Recording the formation of moxGFP::μNS condensates

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