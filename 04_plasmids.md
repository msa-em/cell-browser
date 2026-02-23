---
title: Plasmids
numbering:
  enumerator: 3.%s
label : plasmids_page
---

---

## mCherry-ER reporters

mCherry-KDEL was the same construct used in the original study; mCherry-ER-3 plasmid (55041, Addgene), which retains mCherry in the lumen of the ER.
Barkley included mCherry-CytERM-N-17 (55024, Addgene) to retain mCherry on the cytoplasmic side.
mCherry-CytERM was considered a positive control for ER remodelling because organized smooth endoplasmic reticulum (OSER) whorls form through fluorescent protein dimerization [@doi:10.1083/jcb.200306020] in roughly 5% of transfected cells [@doi:10.1038/nmeth.3891].
Calreticulin should also be detectable in OSER whorls with immunofluorescence imaging [@doi:10.1083/jcb.200306020].
Two additional constructs were included with ER proteins fused to mCherry; mCh-Climp63 (136293, Addgene) and mCh-Sec61β (49155, Addgene).
mCherry-Climp63 was a control for ER remodelling, given its role in determining ER morphology [@doi:10.1016/j.cell.2010.11.007], while mCherry-Sec1β was considered a general ER marker [@doi:10.1126/science.aay7108].

## Lipofectamine 3000 (left) and TransIT-2020 (right) reagents

HeLa cells were imaged after one day of transfection with mCherry-ER reporters.
Illumination settings in the mCherry channel were set based on the mCherry-KDEL sample transfected with TransIT-2020.
In comparison, transfection efficiency and protein expression was better with lipofectamine, causing saturated signal in these samples.
All four mCherry-ER constructs show irregular ER morphologies, including mCherry-KDEL.

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

### mCherry-Sec61β

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

### mCherry-Climp63

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

---

:::{dropdown} Transfection protocol
Lipofectamine 3000 (L3000015, Invitrogen) was used with 12-well plates; 62.5ul Opti-MEM (31985-062, Gibco) was mixed with 2.5ul P3000 reagent and 1.25ug DNA, and another tube of 62.5ul Opti-MEM was mixed with 1.875ul lipofectamine 3000 reagent. The tubes were mixed, incubated for 20 minutes, then added dropwise to the samples.
TransIT-2020 Reagent (MIR 5400, Mirus) was used with 12-well plates; 125ul Opti-MEM was mixed with 1.25ug DNA, mixed gently, then 3.75ul TransIT-2020 was added and mixed, followed by 20 minutes of incubation and dropwise addition to the samples.
:::
