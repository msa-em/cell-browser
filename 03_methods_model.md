---
title: Model
numbering:
  enumerator: 3.%s
label : model_page
---

## Cell culture

HeLa CCL-2 cells were cultured in Dulbecco’s modification of Eagle’s Medium (DMEM) (50-003-PB, Corning) supplemented with 10% fetal bovine serum (FS-0500-AD, Atlas).
Antibiotics were not used in the replication study, although the original study used 100 U/ml penicillin G, 100ug/ml streptomycin and 0.25ug/ml amphotericin B.

## Transfected-infected cell model

This experiment aims to observe cells with a co-incidence of plasmid transfection and virus infection.
In the original study, cells were transfected before virus infection, each incubated for twenty four hours.
The cells in this model were imaged after two days of transfection and one day of infection.
A confounding variable is interference of viral infection from transfection, so two transfection reagents were compared.
Transfection with TransIT-2020 (Mirus Bio) was favourable for subsequent reovirus infection, which was the reagent used in the original study.
All samples were infected with reovirus strain T1L at MOI 100 then were stained with calreticulin antibodies.
These samples are an early look at the replication experiment.
There is evidence of aberrant ER in the mCherry channel as bright concentrations of signal, observed in both transfected-uninfected and transfected-infected cells.

## Imaging

Samples were imaged on an Olympus Fluoview FV3000 laser-scanning confocal microscope with a 100X objective lens using immersion oil. 
The pinhole was opened for all channels for the widest depth of field. 
Z-draft compensation was used to autofocus the samples during acquisition. 
Each channel was excited separately and care was taken to avoid spectral overlap. 
The coordinates for a 10x10 grid with 5% overlap was set and the one hundred fields were captured using the multi-area time lapse protocol.

:::{figure}
:name: Untransfected infected cells

::::{grid} 1 1 1 1
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment1/sample1.zarr/",
  "height": "600px"
}
:::
::::

Your figure caption goes here. This appears below the viewer and can be referenced.
:::

### Untransfected cells

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample3.zarr/",
  "height": "600px"
}

:::

### Mirus Transit2020-transfected cells

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample2.zarr/",
  "height": "600px"
}

:::

### Lipofectamine 3000-transfected cells

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample1.zarr/",
  "height": "600px"
}

:::