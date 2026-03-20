---
title: Virus
numbering:
  enumerator: 4.%s
---

## Infection protocol

Stocks of purified reovirus T1L were titrated in L-929 cells to estimate the concentration of plaque-forming units (PFU).
L-929, or L cells are permissive to reovirus infection and were also used for virus titration in the original study, so there was consistency in the calculation of multiplicity of infection (MOI).
To clarify, MOI was PFU/cell, and PFU was estimated on L-929 cells in both the original and replication study.
For infection, purified reovirus was diluted in a volume of 100μl of serum-free DMEM which was adsorbed to cells for one hour at room temperature with agitation every ten minutes.
Thereafter, pre-warmed serum-containing DMEM was added to the cells, and the samples were incubated for one day before fixation.

## Mammalian orthoreovirus strains

Parker described the morphology of reovirus strain Type 1 Lang (T1L) factories as _filamentous_ and T3D factories as _globular_ and found the M1(T1L)-P208S mutation that disrupted an interaction between μ2 and microtubules that determined the filamentous phenotype [@doi:10.1128/JVI.76.9.4483-4496.2002].
No rationale was provided in the mBio study for using this M1(T1L)-P208S mutant, so it was substituted for wildtype reovirus strain T1L in the replication study.
The difference is wildtype reovirus tends to form filamentous viral factories, while the M1(T1L)-P208S virus would have formed globular factories.
A stock of unpurified reovirus strain Type 3 Dearing (T3D), which forms globular viral factories, was included in this experiment to compare these morphologies.
Others have reported using MOI 100 due to the low permissivity of HeLa cells to reovirus [@doi:10.1128/jvi.00199-19], so ten-fold dilutions from MOI 0 to 100 were tested.
Infected cells were visualized with α-μNS chicken serum and AlexaFluor647-conjugated secondary antibodies.
Most HeLa cells were infected with reovirus T1L at MOI 100, so this was used for replication experiments, an increase from MOI 1 used in the original study.
At MOI 1, only a few infected cells were found and pinned on the map.

::::{grid} 2 2 2 2
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample1.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "Reovirus T1L MOI 0",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Adjust contrast",
      "description": "Reovirus channel min 0 max 2000",
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
            2000
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample5.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "Reovirus T3D MOI 0",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Adjust contrast",
      "description": "Reovirus channel min 0 max 2000",
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
            2000
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample4.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "Reovirus T1L MOI 1",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Adjust contrast",
      "description": "Reovirus channel min 0 max 2000",
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
            2000
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "default": true
    }
  ],
  "annotations": [
    {
      "name": "Infected cell",
      "target": [
        7471,
        983
      ],
      "color": [
        235,
        87,
        87
      ]
    },
    {
      "name": "Infected cell",
      "target": [
        7362,
        850
      ],
      "color": [
        235,
        87,
        87
      ]
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample8.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "Reovirus T3D MOI 1",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Adjust contrast",
      "description": "Reovirus channel min 0 max 2000",
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
            2000
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
      },
      "default": true
    }
  ],
  "annotations": [
    {
      "name": "Infected cell",
      "target": [
        6460,
        2626
      ],
      "color": [
        235,
        87,
        87
      ]
    },
    {
      "name": "Infected cell",
      "target": [
        5199,
        7702
      ],
      "color": [
        235,
        87,
        87
      ]
    },
    {
      "name": "Infected cell",
      "target": [
        8381,
        6188
      ],
      "color": [
        235,
        87,
        87
      ]
    },
    {
      "name": "Infected cell",
      "target": [
        9605,
        5645
      ],
      "color": [
        235,
        87,
        87
      ]
    },
    {
      "name": "Infected cell",
      "target": [
        2486,
        8493
      ],
      "color": [
        235,
        87,
        87
      ]
    },
    {
      "name": "Infected cell",
      "target": [
        7598,
        9699
      ],
      "color": [
        235,
        87,
        87
      ]
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample3.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "Reovirus T1L MOI 10",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Adjust contrast",
      "description": "Reovirus channel min 0 max 2000",
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
            2000
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample7.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "Reovirus T3D MOI 10",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Adjust contrast",
      "description": "Reovirus channel min 0 max 2000",
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
            2000
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample2.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "Reovirus T1L MOI 100",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Adjust contrast",
      "description": "Reovirus channel min 0 max 2000",
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
            2000
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample6.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "Reovirus T3D MOI 100",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 20,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Adjust contrast",
      "description": "Reovirus channel min 0 max 1250",
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
            1250
          ]
        ],
        "blendMode": "single",
        "colormap": "viridis"
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

:::{tip}
Evaluate the calreticulin channel for alleged reovirus-induced ER remodeling.
The uninfected control is MOI 0 and ER morphology can be compared within populations.
:::
