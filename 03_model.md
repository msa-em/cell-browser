---
title: Model
numbering:
  enumerator: 3.%s
label : model_page
---

## Cells

HeLa CCL-2 cells were cultured in Dulbecco’s modification of Eagle’s Medium (DMEM) (50-003-PB, Corning) supplemented with 10% fetal bovine serum (FS-0500-AD, Atlas).
Antibiotics were not used in the replication study, although the original study used 100 U/ml penicillin G, 100μg/ml streptomycin and 0.25μg/ml amphotericin B.

## Imaging

Coverslips were imaged on an Olympus Fluoview FV3000 laser-scanning confocal microscope with a 100X objective lens using immersion oil. 
Pinholes were maximally opened to capture the widest depth of field.
Z-draft compensation autofocused the samples during acquisition of 10x10 or 15x15 field grids (5% overlap) with a motorized XY stage (Olympus IX3-SSU).
Data collection was fully-motorized for unbiased samples of the replicate immunofluorescence experiments.

## Transfected-infected cell model

This experiment aims to observe cells with a co-incidence of plasmid transfection and virus infection.
In the original study, cells were transfected before virus infection, each incubated for twenty four hours.
Therefore, the cells were imaged after two days of transfection and one day of infection.
A confounding variable is interference of viral infection from transfection, so two transfection reagents were compared in the transfected-infected cell model.
All samples were infected with reovirus strain T1L at MOI 100 and were co-stained with reovirus and calreticulin antibodies and DAPI.

### mCherry-KDEL transfection with TransIT-2020 before reovirus infection

Transfection with TransIT-2020 (Mirus Bio) was favourable for subsequent reovirus infection, which was the reagent used in the original study.

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample2.zarr/",
  "height": "600px"
}

:::

### Untransfected control (left) and transfection with lipofectamine (right)

Lipofectamine 3000 transfection was less favourable in this model because of reduced cell confluence and reovirus infection.

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