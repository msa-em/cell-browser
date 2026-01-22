---
title: Model
numbering:
  enumerator: 3.%s
label : model_page
---

---

## Cells

HeLa CCL-2 cells were cultured in Dulbecco’s modification of Eagle’s Medium (DMEM) (50-003-PB, Corning) supplemented with 10% fetal bovine serum (FS-0500-AD, Atlas).
Antibiotics were not used in the replication study, although the original study used 100 U/ml penicillin G, 100μg/ml streptomycin and 0.25μg/ml amphotericin B.

## Imaging

Data collection was fully-motorized for unbiased samples of replicate immunofluorescence experiments.
The coverslips were imaged with an Olympus Fluoview FV3000 confocal microscope using a 100X objective lens in immersion oil. 
Pinholes in each channel were opened to capture the widest depth of field.
Acquisition of 10x10 or 15x15 grids (5% overlap) with the Olympus IX3-SSU motorized XY stage were autofocused with Z-drift compensation.
Care was taken to avoid spectral overlap, but aberrations are possible.

---

# Results

## Immunofluorescence imaging of transfected-infected cells

This replication experiment aimed to observe cells with a co-incidence of plasmid transfection and virus infection.
In the original study, cells were transfected before virus infection, each incubated for twenty four hours.
A confounding variable was interference of viral infection from transfection, so two reagents were tested.
All samples were infected with reovirus strain T1L at MOI 100 and were co-stained for reovirus and ER antigens.

### mCherry-KDEL transfection with TransIT-2020 before reovirus infection

Transfection with TransIT-2020 (Mirus Bio) was favourable for subsequent reovirus infection.

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/experiment5/sample2.zarr/",
  "height": "600px"
}

:::

### Untransfected control (left) and transfection with lipofectamine (right)

Lipofectamine 3000 transfection reduced cell confluence and reovirus infection in this model.

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