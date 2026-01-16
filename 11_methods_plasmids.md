---
title: Plasmids
numbering:
  enumerator: 2.%s
label : plasmids_page
---

# Transfection protocol

Lipofectamine 3000 (L3000015, Invitrogen) was used with 12-well plates; 62.5ul Opti-MEM (31985-062, Gibco) was mixed with 2.5ul P3000 reagent and 1.25ug DNA, and another tube of 62.5ul Opti-MEM was mixed with 1.875ul lipofectamine 3000 reagent. The tubes were mixed, incubated for 20 minutes, then added dropwise to the samples.
TransIT-2020 Reagent (MIR 5400, Mirus) was used with 12-well plates; 125ul Opti-MEM was mixed with 1.25ug DNA, mixed gently, then 3.75ul TransIT-2020 was added and mixed, followed by 20 minutes of incubation and dropwise addition to the samples.

# mCherry-ER reporters

The mCherry-KDEL construct was the same as the original study; mCherry-ER-3 plasmid (55041, Addgene), which retained mCherry in the lumen of the ER.
Barkley included mCherry-CytERM-N-17 (55024, Addgene) to retain mCherry on the cytoplasmic side of the ER.
mCherry-CytERM was considered a positive control for ER remodelling because of the propensity of fluorescent proteins to cause organized smooth endoplasmic reticulum (OSER) whorls [@doi:10.1083/jcb.200306020].
Two additional constructs were included with ER proteins fused to mCherry; mCh-CLIMP63 (136293, Addgene) and mCh-SEC61β (49155, Addgene).
mCherry-CLIMP-63 was a control for ER remodelling, given its role in determining ER morphology [@doi:10.1016/j.cell.2010.11.007], while mCherry-SEC61β was considered a general ER marker [@doi:10.1126/science.aay7108].

## mCherry-ER plasmid transfection with Lipofectamine 3000 (left) or Mirus Transit2020 (right)

HeLa cells were transfected with four mCherry-ER reporter constructs using two different transfection reagents for twenty four hours.
The cells were fixed then stained with calreticulin antibodies (ER marker) and DAPI (nucleus marker).
One hundred fields in a 10x10 grid were imaged.
Transfection efficiency and protein expression was better with lipofectamine.
All four mCherry-ER constructs show aberrant ER morphology in the microscopy maps, including the mCherry-KDEL construct used in the original study.
To be more specific - in the mCherry channel of all eight maps, there are cells with concentrated regions of signal that could be interpreted as irregular ER morphology.
The original study reported these observations and described them as collapsed and aggregated ER elements caused by reovirus.
Our data shows that aberrant ER morphologies are observed in cells expressing mCherry-ER constructs in the absence of reovirus.
Therefore, an alternative explanation is that artifacts were misinterpreted as virus-induced ER remodelling.

### mCherry-KDEL

::::{grid} 2 2 2 2

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample3.zarr/",
  "height": "350px"
}

:::

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample7.zarr/",
  "height": "350px"
}

:::

::::

### mCherry-CytERM

::::{grid} 2 2 2 2

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample2.zarr/",
  "height": "350px"
}

:::

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample6.zarr/",
  "height": "350px"
}

:::

::::

### mCherry-SEC61β

::::{grid} 2 2 2 2

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample4.zarr/",
  "height": "350px"
}

:::

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample8.zarr/",
  "height": "350px"
}

:::

::::

### mCherry-CLIMP-63

::::{grid} 2 2 2 2

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample1.zarr/",
  "height": "350px"
}

:::

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment2/sample5.zarr/",
  "height": "350px"
}

:::

::::