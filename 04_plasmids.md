---
title: Plasmids
numbering:
  enumerator: 3.%s
---

## mCherry-ER fusions

mCherry-KDEL was the same construct used in the original study; mCherry-ER-3 plasmid (55041, Addgene), which retains mCherry in the lumen of the ER.
Barkley included mCherry-CytERM-N-17 (55024, Addgene) to retain mCherry on the cytoplasmic side.
mCherry-CytERM was considered a positive control for ER remodelling because organized smooth endoplasmic reticulum (OSER) whorls form through fluorescent protein dimerization [@doi:10.1083/jcb.200306020] in ~5% of transfected cells [@doi:10.1038/nmeth.3891].
Calreticulin should also be detectable in OSER whorls with immunofluorescence imaging [@doi:10.1083/jcb.200306020].
Two additional constructs were included with ER proteins fused to mCherry; mCh-Climp63 (136293, Addgene) and mCh-Sec61β (49155, Addgene).
mCherry-Climp63 was a control for ER remodeling, given its role in determining ER morphology [@doi:10.1016/j.cell.2010.11.007], while mCherry-Sec1β was considered a general ER marker [@doi:10.1126/science.aay7108].
HeLa cells were imaged after one day of transfection with plasmids encoding mCherry-ER fusions.
Trans-IT 2020, the transfection reagent used in the original study was compared to Lipofectamine 3000.
Parker advised adjusting the illumination settings individually to avoid pixel saturation.
All repetitions were shown in the Supplemental.

::::{grid} 2 2 2 2
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/plasmid_repeat/lf3000_kdel_Cycle_02.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-KDEL (Lipofectamine)",
    "position": "top-center",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "ER remodeling",
      "zoom": -0.798,
      "target": [
        11053,
        10028,
        0
      ],
      "appearance": {
        "channelsVisible": [
          false,
          true,
          true
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            0,
            0,
            255
          ],
          [
            255,
            0,
            0
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
            2208
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      }
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 12,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/plasmid_repeat/transit_KDEL_Cycle_02.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-KDEL (Trans-IT 2020)",
    "position": "top-center",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "ER remodeling",
      "zoom": -1.066,
      "target": [
        9952,
        424,
        0
      ],
      "appearance": {
        "channelsVisible": [
          false,
          true,
          true
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            0,
            0,
            255
          ],
          [
            255,
            0,
            0
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
      }
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 12,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/plasmid_repeat/lf3000_cytER_Cycle.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-CytERM (Lipofectamine)",
    "position": "top-center",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "ER remodeling",
      "zoom": -1.066,
      "target": [
        5994,
        4032,
        0
      ],
      "appearance": {
        "channelsVisible": [
          false,
          true,
          true
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            0,
            0,
            255
          ],
          [
            255,
            0,
            0
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
      }
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 12,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/plasmid_repeat/transit_cyter_Cycle_03.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-CytERM (Trans-IT 2020)",
    "position": "top-center",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "ER remodeling",
      "zoom": -0.51,
      "target": [
        10587,
        9413,
        0
      ],
      "appearance": {
        "channelsVisible": [
          false,
          true,
          true
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            0,
            0,
            255
          ],
          [
            255,
            0,
            0
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
      }
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 12,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/plasmid_repeat/lf3000_sec61_Cycle_02.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-Sec61β (Lipofectamine)",
    "position": "top-center",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "ER remodeling",
      "zoom": -0.51,
      "target": [
        11070,
        3818,
        0
      ],
      "appearance": {
        "channelsVisible": [
          false,
          true,
          true
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            0,
            0,
            255
          ],
          [
            255,
            0,
            0
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
      }
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 12,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/plasmid_repeat/transit_sec_Cycle_01.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-Sec61β (Trans-IT 2020)",
    "position": "top-center",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "ER remodeling",
      "zoom": -0.51,
      "target": [
        9912,
        1666,
        0
      ],
      "appearance": {
        "channelsVisible": [
          false,
          true,
          true
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            0,
            0,
            255
          ],
          [
            255,
            0,
            0
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
      }
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 12,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/plasmid_repeat/lf3000_climp_Cycle.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-Climp63 (Lipofectamine)",
    "position": "top-center",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "ER remodeling",
      "zoom": -1.621,
      "target": [
        11242,
        13229,
        0
      ],
      "appearance": {
        "channelsVisible": [
          false,
          true,
          true
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            0,
            0,
            255
          ],
          [
            255,
            0,
            0
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
      }
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 12,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://nyu1.osn.mghpcc.org/barkley-replication/plasmid_repeat/transit_climp_Cycle_01.zarr",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-Climp63 (TransIT-2020)",
    "position": "top-center",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "ER remodeling",
      "zoom": -0.332,
      "target": [
        6544,
        6534,
        0
      ],
      "appearance": {
        "channelsVisible": [
          false,
          true,
          true
        ],
        "channelColors": [
          [
            0,
            255,
            0
          ],
          [
            0,
            0,
            255
          ],
          [
            255,
            0,
            0
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
      }
    }
  ],
  "scaleBar": {
    "maxWidth": 100,
    "position": "bottom-right",
    "fontSize": 12,
    "font": "Arial",
    "color": "rgba(255,255,255,0.9)"
  }
}
:::
::::

:::{important} Alternative hypothesis
All four mCherry-ER reporters show at least one cell with ostensible ER remodeling (see the preset views).
Therefore, it is possible that the previous investigators misinterpreted mCherry-ER reporter artifacts as an outcome of reovirus infection.
:::

:::{dropdown} Transfection protocol
Lipofectamine 3000 (L3000015, Invitrogen) was used with 12-well plates; 62.5ul Opti-MEM (31985-062, Gibco) was mixed with 2.5ul P3000 reagent and 1.25ug DNA, and another tube of 62.5ul Opti-MEM was mixed with 1.875ul lipofectamine 3000 reagent. 
The tubes were mixed, incubated for 20 minutes, then added dropwise to the samples.
TransIT-2020 Reagent (MIR 5400, Mirus) was used with 12-well plates; 125ul Opti-MEM was mixed with 1.25ug DNA, mixed gently, then 3.75ul TransIT-2020 was added and mixed, followed by 20 minutes of incubation and dropwise addition to the samples.
:::