---
title: Model
numbering:
  enumerator: 2.%s
label : model_page
---

---

## Cells

HeLa CCL-2 cells were cultured in Dulbecco’s modification of Eagle’s Medium (DMEM) (50-003-PB, Corning) supplemented with 10% fetal bovine serum (FS-0500-AD, Atlas).
Antibiotics were not used in the replication study, although the original study used 100 U/ml penicillin G, 100μg/ml streptomycin and 0.25μg/ml amphotericin B.

## Imaging

Data collection was fully-motorized for unbiased sampling of replicate immunofluorescence experiments.
Coverslips were imaged with an Olympus Fluoview FV3000 confocal microscope using a 100X objective lens (Olympus, model UPLAPO100X, NA 1.50) in immersion oil. 
Pinholes in each channel were maximized to capture the widest depth of field.
Grids of 10x10 (100 fields) or 15x15 (225 fields) were acquired with a motorized stage (Olympus IX3-SSU) and Z-drift compensation.

---

# Results

## Immunofluorescence imaging of transfected-infected cells

This experiment aims to observe a co-incidence of plasmid transfection and virus infection in cells.
In the original study, cells were transfected before virus infection, each incubated for twenty four hours.
A confounding variable was interference of viral infection from plasmid transfection, so two transfection reagents were tested in this model.
All samples were infected with reovirus strain T1L and the viral and ER antigens were co-stained.
Transfection with TransIT-2020 appeared favourable for subsequent reovirus infection ([](#fig2a)).
Lipofectamine transfection reduced cell confluence and reovirus infection in this model ([](#fig2b)) compared to the untransfected control ([](#fig2c)).

::::{figure}
:label: fig2a
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample2.zarr/",
  "height": "600px"
}

:::
Figure legend. Mirus TransIT-2020.
::::

::::{figure}
:label: fig2b
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample1.zarr/",
  "height": "600px"
}
:::
Figure legend. Lipofectamine.
::::

::::{figure}
:label: fig2c
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample3.zarr/",
  "height": "600px"
}
:::
Figure legend. Untransfected control.
::::
