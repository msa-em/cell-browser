---
title: Plasmids
numbering:
  enumerator: 3.%s
label : plasmids_page
---

## mCherry-ER reporters

mCherry-KDEL was the same construct used in the original study; mCherry-ER-3 plasmid (55041, Addgene), which retains mCherry in the lumen of the ER.
Barkley included mCherry-CytERM-N-17 (55024, Addgene) to retain mCherry on the cytoplasmic side.
mCherry-CytERM was considered a positive control for ER remodelling because organized smooth endoplasmic reticulum (OSER) whorls form through fluorescent protein dimerization [@doi:10.1083/jcb.200306020] in ~5% of transfected cells [@doi:10.1038/nmeth.3891].
Calreticulin should also be detectable in OSER whorls with immunofluorescence imaging [@doi:10.1083/jcb.200306020].
Two additional constructs were included with ER proteins fused to mCherry; mCh-Climp63 (136293, Addgene) and mCh-Sec61β (49155, Addgene).
mCherry-Climp63 was a control for ER remodeling, given its role in determining ER morphology [@doi:10.1016/j.cell.2010.11.007], while mCherry-Sec1β was considered a general ER marker [@doi:10.1126/science.aay7108].

## Lipofectamine 3000 (left) and TransIT-2020 (right)

HeLa cells were imaged after one day of transfection with mCherry-ER reporters.
Illumination settings in the mCherry channel were set based on the mCherry-KDEL sample transfected with TransIT-2020.
Transfection efficiency and protein expression was better with lipofectamine, so there was pixel saturation in these samples.
Barkley found irregular ER morphologies with lipofectamine transfection of mCherry-ER plasmids, especially mCherry-Sec61β and mCherry-Climp63.
Transfection of mCherry-KDEL with TransIT-2020, as done in the original study, was less susceptible to artifacts.

::::{grid} 2 2 2 2
:::{any:bundle} https://LadInTheLab.github.io/microATLAS-widget/widget.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample3.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-KDEL",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 22,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Zoom to ER remodeling",
      "zoom": 0.074,
      "target": [
        7507,
        3372,
        0
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample7.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-KDEL",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 22,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Zoom to ER remodeling",
      "zoom": 0.074,
      "target": [
        5703,
        1706,
        0
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample2.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-CytERM",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 22,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Zoom to ER remodeling",
      "zoom": 0.074,
      "target": [
        6561,
        5919,
        0
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample6.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-CytERM",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 22,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Zoom to ER remodeling",
      "zoom": 0.074,
      "target": [
        5346,
        5514,
        0
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample4.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-Sec61β",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 22,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Zoom to ER remodeling",
      "zoom": 0.074,
      "target": [
        5296,
        5118,
        0
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample8.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-Sec61β",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 22,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Zoom to ER remodeling",
      "zoom": 0.074,
      "target": [
        7222,
        3355,
        0
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample1.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-Climp63",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 22,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Zoom to ER remodeling",
      "zoom": 0.074,
      "target": [
        4553,
        6248,
        0
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
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample5.zarr/",
  "width": "323px",
  "height": "323px",
  "title": {
    "text": "mCherry-Climp63",
    "position": "bottom-left",
    "margin": 12,
    "fontSize": 22,
    "font": "Arial",
    "color": "rgba(255,255,255,0.95)",
    "style": "text"
  },
  "views": [
    {
      "name": "Zoom to ER remodeling",
      "zoom": 0.074,
      "target": [
        6622,
        1307,
        0
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
::::

:::{important} Alternative hypothesis
All four mCherry-ER reporters show at least one cell with ostensible ER remodeling (see the preset views).
Therefore, it is possible that the previous investigators misinterpreted mCherry-ER reporter artifacts as an outcome of reovirus infection.
:::

:::{dropdown} Transfection protocol
Lipofectamine 3000 (L3000015, Invitrogen) was used with 12-well plates; 62.5ul Opti-MEM (31985-062, Gibco) was mixed with 2.5ul P3000 reagent and 1.25ug DNA, and another tube of 62.5ul Opti-MEM was mixed with 1.875ul lipofectamine 3000 reagent. The tubes were mixed, incubated for 20 minutes, then added dropwise to the samples.
TransIT-2020 Reagent (MIR 5400, Mirus) was used with 12-well plates; 125ul Opti-MEM was mixed with 1.25ug DNA, mixed gently, then 3.75ul TransIT-2020 was added and mixed, followed by 20 minutes of incubation and dropwise addition to the samples.
:::