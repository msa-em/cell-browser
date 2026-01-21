---
title: NucleusNet
numbering:
  enumerator: 8.%s
label : nucleusnet_page
---

# NucleusNet: one million single-cell microscopy images

## 1600 tiled panoramas

Artificial intelligence models need to train on lots of data, motivating Barkley to create a large collection cropped images of the [cell nucleus](<wiki:Cell_nucleus>), called NucleusNet.
It is the sum of 100 automated imaging experiments that sampled ~37.25cm² of cultured cells, yielding 1,061,277 cropped single-cell images extracted from 1600 stitched panoramas.
Images of cell monolayers were collected over twenty-one passages of the same cell line.
[CV-1 cells](https://www.atcc.org/products/ccl-70) were seeded at varying densities then were fixed in paraformaldehyde (PFA) after at least one day of incubation, so the populations had asynchronous cell cycles.
Fixed cells were stained with DAPI which binds to DNA, making the cell nucleus fluoresce upon excitation with ultraviolet light.
As expected, we observed variation in cell confluence and signal intensity between experiments, and even between regions of the same coverslip ([](#sfig1a)).
Ten stitched images closest to the centroid were selected to represent those with an average number and brightness of ROIs ([](#table1)).

## 1,061,277 single-cell images

Nuclei were masked in the stitched images with a custom [cellpose](https://github.com/MouseLand/cellpose) segmentation model [@doi:10.1038/s41592-020-01018-x].
Cellpose was suitable for segmentation because cell division created instances where two nuclear bodies were separated in space but should count as one ROI.
Specifically, mitotic figures in [anaphase](#anaphase) or [telophase](#telophase) were considered one ROI, and [micronuclei](<wiki:Micronucleus>) and nuclei were masked together.
There were also instances where two or more distinct nuclei made contact but should be separate masks.
Barkley re-trained and tuned the cellpose model until it handled these challenges sufficiently.
Browse the ten representative stitched images ([](#table3)) from [](#sfig1a) to evaluate the cellpose segmentation model using an overlay.
Unique masks were assigned random colours to help differentiate ROIs.
False-positive detections by cellpose were rare but expected as a consequence of high-throughput automation.

**Figure 1A: Embed OpenSeadragon viewer with this [image](https://russellbarkley.github.io/cellpose_masks/)**

::::{figure}
:label: open_seadragon_demo

:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "prefixUrl": "images/",
    "tileSources": "https://openseadragon.github.io/example-images/duomo/duomo.dzi"
}
:::
::::

::::{figure}

:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/NucleusNet-10K-DZI/images/nucleusnet_10k.dzi"
}
:::

::::

## NucleusNet-10K

A small version (n=10,000) of the single-cell dataset was created with one-hundred random images from each imaging session.
An interactive cell browser was made that shows random examples from NucleusNet-10K [](#fig1b), so every reader will see a different subset of the collection.
Generally, nuclei were properly centered, well segemented, and pre-aligned in the cropped images.
Pixels were set to zero outside of the mask, leaving background signal around the nucleus, which was notable because this property seemed to emerge in the reconstructions from the trained autoencoder.
Otherwise, cropped images in this version of NucleusNet were not processed further.

:::{figure} #nucleusnet10k_cellbrowser
:label: fig1b
:placeholder: ./figures/cellbrowser.png
Figure legend.
:::

With collections of images in the literature, it is common to see several random examples presented in a static figure.
Barkley fused NucleusNet-10K into a 100x100 tile grid and embedded the stitched image (Figure 1C).
Experiments were reported in chronological order by row from top to bottom and clearly there was variation in signal intensity between experiments.
This observation would warrant image pre-processing techniques that normalize or standardize pixel intensities in NucleusNet.
Interestingly, there is another [example](https://www.allencell.org/deep-cell-zoom.html) of this visualization strategy used to present 200,000 single-cell images of human-induced pluripotent stem cells.

**Figure 1C: Embed OpenSeadragon viewer with NucleusNet-10K**

# Materials and Methods

## Cell culture

The CV-1 cell line is fibroblast-like and derived from the kidney of an African green monkey.
CV-1 cells were cultured in Eagle's minimal essential medium supplemented with fetal bovine serum (10% volume/volume) at 37 degrees celsius with 5 percent environmental carbon dioxide to buffer pH.
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

```{figure} ./figures/fig4.png
:label: fig4
:align: center
:width: 100%

An overview of data collection and pre-processing. 
A) Tiles were imaged in a 50x50 grid. 
B) Then stitched into 25x25 tile grids (quarters). 
C) Quarters were cropped into four stitched images.
```

1. Conversion to 8-bit .TIF format

Raw 12-bit files are in the proprietary Olympus .oir file format with metadata.
The raw were converted to 8-bit TIF format using FIJI [@doi:10.1038/nmeth.2019] and were renamed 0-2500.tif corresponding to the order that the tiles were imaged.

2. Tiles stitched with Microscopy Image Stitching Tool (MIST)

The size of a full stitched image approaches the maximum value that a 32-bit integer can hold, therefore the N=2500 .tif files were divided into sub-folders containing n=625 images corresponding to four quarters ([](#fig4)).
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
The stitched quarters were then cropped into four quarters, yielding n=16 stitched images per coverslip ([](#fig4)) and N=1600 stitched images from all one-hundred experiments.

(cellpose-segmentation)=
3. Segmentation with cellpose

Nuclei were masked in the stitched images using a custom [cellpose](https://github.com/MouseLand/cellpose) model [@doi:10.1038/s41592-020-01018-x].
The pre-trained cellpose nucleus model was re-trained on N=125000 fields from NucleusNet, including n=1000 fields with manually-segmented nuclei.
Weights were saved as CP_20250418_Nuclei_1Kmasks.
Advanced parameters in the graphical user interface were adjusted to flow_threshold: 0.5, cellprob_threshold: -2.0, diameter (pixels): 152.91.
The cellpose model segmented the nuclei in all stitched images and the mask files were saved as PNG files where each region of interest (ROI) is defined by a unique pixel value.

```{admonition} Bias in NucleusNet from data processing methods
:class: warning
The detection of nuclei and the accuracy of the masks relied on the cellpose model. There are undesirable artifacts like blank images and inaccurate masks in the dataset, and sampling was likely inconsistent between stitched images due to variations in signal intensity. The cellpose model was re-trained and hand-tuned by a human. Training was also semi-supervised with manual masks. Thus, there are human and model biases.
```

4. Cropped single cell masked dataset

The orientation of a cell is known to confound the vector embedding of autoencoder models trained on single-cell microscopy data, motivating the development of orientation-invariant autoencoder models [@doi:10.1038/s41467-024-45362-4].
Similarly, a multi-encoder variational autoencoder model controlled for several transformational features like orientation that were 'uninformative' in single-cell analyses [@doi:10.1038/s42003-022-03218-x].
Barkley [pre-aligned](https://github.com/jmhb0/o2vae/tree/master/prealignment) and by fitting and rotating a minimal area rectangle to the cellpose mask.
Nuclei were center-cropped and all values outside of the mask were set to zero in the cropped images.

## Deep zoom microscopy maps

Microscopy maps are a novel visualization strategy to present large high-magnification microscopy images as zoomable digital maps.
There are free and open-source options to create microscopy maps [@doi:10.1242/jcs.262198].
[VIPS](https://www.libvips.org/) was used to generate the Deep Zoom image (.dzi) image tile pyramid and [OpenSeadragon](https://openseadragon.github.io/) v4.1.0 viewed the tiles.
OpenSeadragon v5.0.0+ had unstable performance on mobile devices.
Code and data was hosted on Github Pages.