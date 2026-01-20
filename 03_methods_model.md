---
title: Model
numbering:
  enumerator: 3.%s
label : model_page
---

## Cell culture

HeLa CCL-2 cells were cultured in Dulbecco’s modification of Eagle’s Medium (DMEM) (50-003-PB, Corning) supplemented with 10% fetal bovine serum (FS-0500-AD, Atlas).
Antibiotics were not used in the replication study, although the original study used 100 U/ml penicillin G, 100μg/ml streptomycin and 0.25μg/ml amphotericin B.

## Imaging

Coverslips were imaged on an Olympus Fluoview FV3000 laser-scanning confocal microscope with a 100X objective lens using immersion oil. 
The pinholes were maximally opened to capture the widest depth of field in all channels.
Z-draft compensation was used to autofocus the samples during acquisition of a 10x10 or 15x15 grid (5% overlap) with a motorized XY stage (Olympus IX3-SSU).
Therefore, data collection was fully-motorized in XYZ for an unbiased sample of the population from an immunofluorescence experiment.

## Transfected-infected cell model

This experiment aims to observe cells with a co-incidence of plasmid transfection and virus infection.
In the original study, cells were transfected before virus infection, each incubated for twenty four hours.
The cells in this model were imaged after two days of transfection and one day of infection.
A confounding variable is interference of viral infection from transfection, so two transfection reagents were compared.
Transfection with TransIT-2020 (Mirus Bio) was favourable for subsequent reovirus infection, which was the reagent used in the original study.
This microscopy map is an early look at the replication experiment.

### Transfection of mCherry-KDEL with TransIT-2020 before reovirus infection

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample2.zarr/",
  "height": "600px"
}

:::

All samples were infected with reovirus strain T1L at MOI 100 and were stained with reovirus and calreticulin antibodies.
In the original study, aberrant ER was shown as bright concentrations of mCherry in cells expressing mCherry-KDEL, described as 'aggregated' and 'collapsed' ER elements induced by reovirus.
Replicate microscopy maps show that this phenotype is observed in both infected and uninfected cells transiently expressing mCherry-KDEL, suggesting that it is not attributed to the virus.
Changes in ER morphology between infected and uninfected cells are unclear in the calreticulin channel, which supports the null hypothesis that reovirus does not remodel the ER.
Barkley made these interpretations from the embedded microscopy maps, using the same data available to the public for scrutiny.

### Untransfected control (left) and transfection with lipofectamine (right)

::::{grid} 2 2 2 2

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample3.zarr/",
  "height": "350px"
}

:::

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample1.zarr/",
  "height": "350px"
}

:::

::::
