---
title: mNeonGreen::μNS
numbering:
  enumerator: 18.%s
---

::::{figure}
:label: sfig16
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/video.zarr",
  "width": "500px",
  "height": "500px",
  "title": {
    "text": "mNeonGreen::μNS + mCherry-KDEL",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Play by default",
      "zoom": -3.784,
      "target": [
        3431,
        3431,
        0
      ],
      "playback": {
        "playing": true,
        "fps": 24,
        "startFrame": 0
      },
      "default": true
    },
    {
      "name": "mCherry-KDEL artifacts",
      "zoom": 0.106,
      "target": [
        3718,
        5505,
        0
      ],
      "playback": {
        "playing": true,
        "fps": 24,
        "startFrame": 0
      }
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
Cotransfection of mNeonGreen::μNS and mCherry-KDEL in live cells.
::::

:::{dropdown} Methods
HeLa cells were seeded on 35mm glass-bottom dishes (20mm coverslips, no 1.5 glass).
pCI-neo mNeonGreen::μNS(1-721) and mCherry-KDEL plasmids were cotransfected (1:1 ratio, 1.25μg each) for 24 hours with Lipofectamine 3000.
The stage was heated (37C) but did not have carbon dioxide so the media was supplemented with 25mM HEPES buffer before imaging.
49 fields (7x7 grid) were imaged in a serpentine pattern at 4 minute intervals for thirty frames (~2 hours total).
:::