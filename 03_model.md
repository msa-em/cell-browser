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

Data collection was fully-motorized for unbiased sampling of large images from replicate immunofluorescence experiments.
Grids of 10x10 (100 fields) or 15x15 (225 fields) were acquired with a robotic XY stage (IX3-SSU) and Z-drift compensation (IX3-ZDC).
Coverslips were imaged with an Olympus Fluoview FV3000 confocal microscope using a 100X objective lens (Olympus model UPLAPO100X, NA 1.50) in immersion oil. 
Pinholes in each channel were maximized to capture the widest depth of field.

---

# Results

## Immunofluorescence imaging of transfected-infected cells

This experiment aims to observe a co-incidence of plasmid transfection and virus infection in cells.
In the original study, cells were transfected before virus infection, each incubated for twenty four hours.
A confounding variable was interference of viral infection from plasmid transfection, so two transfection reagents were tested in this model.
All samples were infected with reovirus strain T1L. 
Viral and ER antigens were co-stained with reovirus μNS and calreticulin antibodies for immunofluorescence imaging.

Transfection with the TransIT-2020 reagent was better than Lipofectamine 3000 in this model.
The TransIT-2020 sample was comparable to the untransfected control in terms of cell confluence and viral infection.

::::{figure}
:label: fig2a
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample2.zarr/",
  "height": "600px"
}

:::
Transfected-infected cells. mCherry-KDEL transfection with TransIT-2020 transfection reagent was followed by reovirus T1L infection (MOI 100).
::::

::::{figure}
:label: fig2b
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample1.zarr/",
  "height": "600px"
}
:::
Transfected-infected cells. mCherry-KDEL transfection with Lipofectamine 3000 transfection reagent was followed by reovirus T1L infection (MOI 100).
::::

::::{figure}
:label: fig2c
:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js
{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample3.zarr/",
  "height": "600px"
}
:::
Untransfected control. The cells were infected with reovirus T1L (MOI 100).
::::
