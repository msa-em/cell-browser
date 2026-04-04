---
title: Nucleation
numbering:
  enumerator: 19.%s
---

### Recording the formation of moxGFP::μNS condensates

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
See _Droplet nucleation time-lapse experiments_ [@doi:10.1091/mbc.E24-01-0013].
:::