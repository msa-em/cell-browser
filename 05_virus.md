---
title: Virus
numbering:
  enumerator: 4.%s
label : virus_page
---

## Infection protocol

Stocks of purified reovirus T1L were titrated in L-929 cells to estimate the concentration of plaque-forming units (PFU).
L-929, or L cells are permissive to reovirus infection and were also used for virus titration in the original study, so there was consistency in the calculation of multiplicity of infection (MOI).
To clarify, MOI was PFU/cell, and PFU was estimated on L-929 cells in both the original and replication study.
For infection, purified reovirus was diluted in a volume of 100μl of serum-free DMEM which was adsorbed to cells for one hour at room temperature with agitation every ten minutes.
Thereafter, pre-warmed serum-containing DMEM was added to the cells, and the samples were incubated for one day before fixation.

## Mammalian reovirus strains T1L (left) and T3D (right)

Parker described the morphology of reovirus strain Type 1 Lang (T1L) factories as _filamentous_ and T3D factories as _globular_ and found the M1(T1L)-P208S mutation that disrupted an interaction between μ2 and microtubules that determined the filamentous phenotype [@doi:10.1128/JVI.76.9.4483-4496.2002].
No rationale was provided in the mBio study for using this M1(T1L)-P208S mutant, so it was substituted for wildtype reovirus strain T1L in the replication study.
The difference is wildtype reovirus tends to form filamentous viral factories, while the M1(T1L)-P208S virus would have formed globular factories.
A stock of unpurified reovirus strain Type 3 Dearing (T3D), which forms globular viral factories, was included in this experiment to compare these morphologies.
Others have reported using MOI 100 due to the low permissivity of HeLa cells to reovirus [@doi:10.1128/jvi.00199-19], so ten-fold dilutions from MOI 0 to 100 were tested.
Infected cells were visualized with α-μNS chicken serum and AlexaFluor647-conjugated secondary antibodies.
Most HeLa cells were infected with reovirus T1L at MOI 100, so this was used for replication experiments, an increase from MOI 1 used in the original study.

:::{tip}
Adjust the contrast in the reovirus μNS channel to readily observe reovirus-infected cells.
:::

### MOI 0

::::{grid} 2 2 2 2
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample1.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "T1L MOI 0",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Edit",
      "description": "Increased contrast in reovirus channel",
      "zoom": -4.928,
      "target": [
        4886,
        4886,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true,
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
            2182
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "default": true
    }
  ],
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample5.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "T3D MOI 0",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Edit",
      "description": "Increased contrast in reovirus channel",
      "zoom": -4.928,
      "target": [
        4886,
        4886,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true,
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
            2129
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "default": true
    }
  ],
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample4.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "T1L MOI 1",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Edit",
      "description": "Increased contrast in reovirus channel",
      "zoom": -4.928,
      "target": [
        4886,
        4886,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true,
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
            2049
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "default": true
    }
  ],
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample8.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "T3D MOI 1",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 16,
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

### MOI 10

::::{grid} 2 2 2 2
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample3.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "T1L MOI 10",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Edit",
      "description": "Increased contrast in reovirus channel",
      "zoom": -4.928,
      "target": [
        4886,
        4886,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true,
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
            2076
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "default": true
    }
  ],
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample6.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "T3D MOI 10",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Edit",
      "description": "Increased contrast in reovirus channel",
      "zoom": -4.928,
      "target": [
        4886,
        4886,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true,
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
            2102
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "default": true
    }
  ],
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample2.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "T1L MOI 100",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Edit",
      "description": "Increased contrast in reovirus channel",
      "zoom": -4.928,
      "target": [
        4886,
        4886,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true,
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
            2235
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "default": true
    }
  ],
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample7.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "T1L MOI 100",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 16,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Edit",
      "description": "Increased contrast in reovirus channel",
      "zoom": -4.928,
      "target": [
        4886,
        4886,
        0
      ],
      "appearance": {
        "channelsVisible": [
          true,
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
            2182
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "default": true
    }
  ],
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

:::{attention}
Observe the calreticulin channel for alleged reovirus-induced ER stress.
The uninfected control is MOI 0.
ER morphology can also be compared in populations of infected cells.
:::
