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
No rationale was provided in the mBio study for using this M1-P208S mutant, so it was substituted for wildtype reovirus strain T1L in the replication study.
The difference is wildtype reovirus tends to form filamentous viral factories, while the M1(T1L)-P208S virus would have formed globular factories.
A stock of unpurified reovirus strain Type 3 Dearing (T3D), which forms globular viral factories, was included in this experiment to compare these morphologies.
Others have reported using MOI 100 due to the low permissivity of HeLa cells to reovirus [@doi:10.1128/jvi.00199-19], so ten-fold dilutions from MOI 0 to 100 were tested.
Infected cells were visualized with α-μNS chicken serum and AlexaFluor647-conjugated secondary antibodies.
Most HeLa cells were infected with reovirus T1L at MOI 100, so this was used for replication experiments.

:::{tip}
Adjust the contrast in the reovirus μNS channel to better observe infected cells.
:::

### MOI 0

::::{grid} 2 2 2 2
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample1.zarr/",
  "height": "350px"
}
:::
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample5.zarr/",
  "height": "350px"
}
:::
::::

### MOI 1

::::{grid} 2 2 2 2
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample4.zarr/",
  "height": "350px"
}
:::
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample8.zarr/",
  "height": "350px"
}
:::
::::

### MOI 10

::::{grid} 2 2 2 2
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample3.zarr/",
  "height": "350px"
}
:::
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample6.zarr/",
  "height": "350px"
}
:::
::::

### MOI 100

::::{grid} 2 2 2 2
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample2.zarr/",
  "height": "350px"
}
:::

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment3/sample7.zarr/",
  "height": "350px"
}
:::
::::

:::{attention}
Observe the calreticulin channel for alleged reovirus-induced ER stress.
MOI 0 is an uninfected control.
The ER of uninfected cells can be compared within populations of infected samples.
:::
