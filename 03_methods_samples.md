---
title: Samples
numbering:
  enumerator: 3.%s
label : samples_page
---

## Cell culture

HeLa CCL-2 cells were cultured in Dulbecco’s modification of Eagle’s Medium (DMEM) (50-003-PB, Corning) which was supplemented with 10% fetal bovine serum (FS-0500-AD, Atlas).
Antibiotics were not added to the medium in the replication study, although in the original study the authors used 100 U/ml penicillin G, 100ug/ml streptomycin and 0.25ug/ml amphotericin B.

## Imaging

Samples were imaged on an Olympus Fluoview FV3000 laser-scanning confocal microscope with a 100X objective lens using immersion oil. 
The pinhole was opened for all channels for the widest depth of field. 
Z-draft compensation was used to autofocus the samples during acquisition. 
Each channel was excited separately and care was taken to avoid spectral overlap. 
The coordinates for a 10x10 grid with 5% overlap was set and the one hundred fields were captured using the multi-area time lapse protocol.

## Transfected-infected cell model

This model aims to observe cells with a co-incidence of plasmid transfection and virus infection.
As done in the original study, HeLa cells were transfected before virus infection, each incubated for twenty four hours.
Two transfection reagents were compared, and it appeared that Mirus Transit2020 was better for subsequent reovirus infection.
All samples were infected with reovirus strain T1L at MOI 100 then were stained with calreticulin antibodies.
These samples are an early look at the replication experiment.
There is evidence of aberrant ER in the mCherry channel as bright concentrations of signal, observed in both transfected-uninfected and transfected-infected cells.

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