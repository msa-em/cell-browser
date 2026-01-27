---
title: NucleusNet
numbering:
  enumerator: 10.%s
label : nucleusnet_page
---

One-hundred coverslips were sampled over twenty-one passages of the same cell line ([](#fig10a)).
[CV-1 cells](https://www.atcc.org/products/ccl-70) were seeded at varying densities then were fixed after at least one day, so the cell cycles were asynchronous.
Nuclei were visualized with DAPI which binds to DNA.
As expected, there was variation in cell confluence and signal intensity between experiments, and even between regions of the same coverslip ([](#sfig12b)).
One million single-cell cropped images were processed from ROI masks segmented in 1600 stitched images ([](#fig10b)).

::::{figure}
:label: fig10a

:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/NucleusNet-coverslip/Run72.dzi"
}
:::

An example coverslip. Experiment 72 was chosen because four stitched images ranked in the top ten with an average number and brightness of ROIs ([](#table3)).
::::

::::{figure}
:label: fig10b

:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/NucleusNet-cellpose/Run25.dzi"
}
:::

Overlay of cellpose segmentation masks. Experiment 25 was chosen because two stitched images ranked in the top ten most average ROI count and intensity. ROI colour was randomized.
::::

## NucleusNet-10K

A small version of the dataset, NucleusNet-10K, represents a random sample of ~1% of NucleusNet.
100 random cropped images from each experiment are shown in chronological order by row ([](#fig10c)).
The map shows variation in signal intensity across experiments, which could warrant the normalization or standardization of pixel intensities.
There is another [example](https://www.allencell.org/deep-cell-zoom.html) of this visualization strategy with 200,000 human-induced pluripotent stem cells.

::::{figure}
:label: fig10c

:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/nucleusnet-10k/nucleusnet_10k.dzi"
}
:::

**Figure 10.3:** NucleusNet-10K: one hundred random images from one hundred experiments (n=10,000).
::::

---

# Autoencoder-based representative image selection

1. Computation of theoretical average images

An autoencoder model was trained on NucleusNet for 50 epochs ([](#sfig12c).
Theoretical latent vectors were calculated using measures of central tendency, including the arithmetic mean, median and geometric median.
Averaged latent vectors were decoded to synthesize theoretical representative images of the nucleus ([](#fig10d)).
Theoretical representative images do not necessarily look like real data [@doi:10.1109/BIP60195.2023.10379342].
They appeared to blend all image features from the dataset, and there is what appears to be background signal around the theoretical nucleus.

:::{figure} #fig10d_data
:label: fig10d
:placeholder: ./figures/fig10d.png
Figure legend.
:::

2. Determination of a prototypical image

Vectors corresponding to real images were ranked by euclidean distance to the theoretical mean of latent space.
Using this measure for simplicity yielded one representative image ([](#fig10e)).

```{figure} ./figures/fig10e.png
:label: fig10e
Representative image from NucleusNet, defined by nearest Euclidean distance to the mean latent vector: ROI_300 from the Run11BR_bottom_right stitched image.
```

---

# Materials and Methods

## Cell culture

The CV-1 cell line is fibroblast-like and derived from the kidney of an African green monkey.
CV-1 cells were cultured in Eagle's minimal essential medium supplemented with 10% fetal bovine serum at 37 degrees celsius with 5 percent environmental carbon dioxide to buffer pH.
At each passage, six glass-bottom cell culture dishes with a 20mm diameter coverslip (Mattek Corporation, P35G-1.5-20-C) were seeded with varied densities of CV-1 cells (~1e4-5e4 cells) to promote heterogeneous cell confluence.

## Sample preparation

The samples were fixed with 4% paraformaldehyde for twenty minutes after one to three days of incubation when the cells approached confluence.
After fixation, the samples were washed with phosphate buffered saline (PBS) then were refrigerated at 4 degrees celsius for storage.
Nuclei were labelled with Nucblue Fixed Cell ReadyProbes Reagent (DAPI) (ThermoFisher Scientific, R37606) in 1 milliliter of PBS for at least 30 minutes then were imaged in the staining solution at room temperature.

## Image acquisition

Large regions of no. 1.5 glass coverslips were sampled using a motorized stage (IX3-SSU) on a laser scanning confocal microscope (Olympus Fluoview FV3000) with an oil immersion objective lens at 100X magnification (Olympus, model UPLAPO100X, NA 1.50).
The pinhole diameter was opened to 800μm to maximize the depth of field.
N=2500 fields were imaged in a 50x50 tile grid (snake pattern by rows: right down left down) with 5% overlap at each edge.
Z-drift compensation was active to maintain autofocus.
The confocal microscope was on a pressurized CleanBench isolation laboratory table (TMC Vibration Control).

```{list-table} Illumination and image processing controls on the Olympus Fluoview FV3000 microscope.
:label: table1

* - Excitation wavelength
  - 405nm
* - Emission wavelength
  - 418nm-496nm
* - Laser intensity
  - 0.12%-0.15%
* - Detector sensitivity
  - 500V
* - Gain
  - 1.0X
* - Offset
  - 3%
* - Field resolution
  - 1024x1024 pixels
* - Pixel size
  - 8.0453 pixels/micrometer
* - Pixel type
  - uint16
* - Bits per pixel
  - 12
```

## Data pre-processing

```{figure} ./figures/sampling.png
:label: sampling
:align: center
:width: 100%
An overview of data collection and pre-processing. A) Tiles were imaged in a 50x50 grid. B) Then stitched into 25x25 tile grids (quarters). C) Quarters were cropped into four stitched images.
```

1. Conversion to 8-bit .TIF format

Raw 12-bit files are in the proprietary Olympus .oir file format with metadata.
The raw were converted to 8-bit TIF format using FIJI [@doi:10.1038/nmeth.2019] and were renamed 0-2500.tif corresponding to the order that the tiles were imaged.

2. Tiles stitched with Microscopy Image Stitching Tool (MIST)

The size of a full stitched image approaches the maximum value that a 32-bit integer can hold, therefore the N=2500 .tif files were divided into sub-folders containing n=625 images corresponding to four quarters ([](#sampling)).
The images in these sub-folders were stitched into 25x25 tile panoramas using the MIST plugin [@doi:10.1038/s41598-017-04567-y] in FIJI.
MIST was useful to correct for inaccurate step sizes that sometimes occurred with the motorized stage.

```{list-table} MIST plugin settings.
:label: table2

* - Filename pattern type
  - Sequential
* - Starting point
  - Upper left
* - Direction
  - Horizontal continuous
* - Grid width
  - 25
* - Grid height
  - 25
* - Grid start tile
  - 0
* - Timeslices
  - 0
* - Filename pattern
  - {pppp}.tif
* - Blending mode
  - Linear
* - Compression mode 
  - Uncompressed
* - Pixel size metadata
  - Mirometer X 8.0453 Y 8.0453
```

The stitched quarter was displayed and saved, named by run and position.
For example, Run53TL was from the top left quarter of the 53rd imaging experiment.
The stitched quarters were then cropped into four quarters, yielding n=16 stitched images per coverslip ([](#sampling)) and N=1600 stitched images from all one-hundred experiments.

3. Segmentation with cellpose

Nuclei were masked in the stitched images using a custom [cellpose](https://github.com/MouseLand/cellpose) model [@doi:10.1038/s41592-020-01018-x].
Cellpose was suitable for segmentation because cell division created instances where two nuclear bodies were separated in space but should count as one ROI.
Specifically, mitotic figures in [anaphase](#anaphase) or [telophase](#telophase) were considered one ROI, and [micronuclei](<wiki:Micronucleus>) and nuclei were masked together.
There were also instances where two or more distinct nuclei made contact but should be separate masks.
Masking by the cellpose segmentation model can be evaluated on ten representative stitched images [here](https://russellbarkley.github.io/cellpose_masks/) ([](#tableS1)).
Unique masks were assigned random colours in the overlay to help differentiate ROIs.

The cellpose nucleus model was re-trained on N=125000 fields from NucleusNet, including n=1000 fields with manually-segmented nuclei.
The weights for the chosen model, CP_20250418_Nuclei_1Kmasks, were deposited in /data/cellpose/.
Advanced parameters in the graphical user interface were adjusted to flow_threshold: 0.5, cellprob_threshold: -2.0, diameter (pixels): 152.91.
The cellpose model segmented the nuclei in all stitched images and the mask files were saved as PNG files where each region of interest (ROI) is defined by a unique pixel value.

4. Cropped single cell masked dataset

The orientation of a cell is known to confound the vector embedding of autoencoder models trained on single-cell microscopy data, motivating the development of orientation-invariant autoencoder models [@doi:10.1038/s41467-024-45362-4].
Similarly, a multi-encoder variational autoencoder model controlled for several transformational features like orientation that were 'uninformative' in single-cell analyses [@doi:10.1038/s42003-022-03218-x].
Nuclei were [pre-aligned](https://github.com/jmhb0/o2vae/tree/master/prealignment) by fitting and rotating a rectangle to the cellpose mask.
Nuclei were center-cropped and all values outside of the mask were set to zero in the cropped images.
This was notable because it left background signal around the nucleus, which later emerged in reconstructions from the autoencoder.
Otherwise, cropped images in NucleusNet were not processed further.