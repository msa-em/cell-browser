---
title: Discussion
numbering:
  enumerator: 0.%s
label : discussion_page
---

Every academic discipline has its own ways of deciding what counts as valid knowledge (see [epistemology](<wiki:Epistemology>)).
If biomedical researchers endorse [empiricism](<wiki:Empiricism>) and objectivity, then why are representative images sufficient to make claims?
A representative image definitively shows that an observation is possible, but a single image cannot describe frequency or variance.
There is disagreement on the [scientific method](<wiki:Scientific_method>), but a general principle is [reproducibility](<wiki:Reproducibility>).
Repeatability in microscopy involves quantitative analyses, but without numerical results, representative images cannot communicate repeatability.
The reality is that representative images can show rare, idealized, or exaggerated examples to embellish results.
Microscopists are incentivized to show compelling evidence and omit contradictory data.
The literature is full of exciting outcomes, but at the bench, experiments are nuanced and prone to failure.

Representative images are figures, which is not to be confused with data.
Data is the raw file from the microscope, while figures are visual representations of data, often shaped by the microscopist.
Figures are the interface for peer review between the experimentalist and coauthors, principal investigators, reviewers and readers.
Indeed, peer review seldom involves data and scientific discourse is limited by the information provided in figures.
This bottleneck can be expanded with virtual microscopy, which is practical to the broader bioimaging community.
For example, OME-Zarr [@doi:10.1007/s00418-023-02209-1] supports several modalities including multiplexed imaging, spatial transcriptomics, light-sheet, infrared, scanning EM and digital pathology.
To maximize accessibility for readers, embedded interactive viewports retrieve data from cloud storage, which was supported by this journal.
Virtual microscopy requires an internet connection, but this limitation is relatively unimportant for contemporary and future publishing.
Web-based microscopy maps are trivial to make and share on Github [@doi:10.1242/jcs.262198], so they can be readily requested by reviewers of all journals.
Fraud prevention could incentivize publishers to adopt this technology as an alternative to static figures.
Because it nurtures open and rigorous peer review, microscopists and principal investigators might find virtual microscopy advantageous to make more robust claims with their bioimaging data.

:::{attention} Molecular biology example
Which moxGFP::μNS construct formed more biomolecular condensates? Left or right?
:::

::::{grid} 2 2 2 2
:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/moxGFPmuNS/FL.dzi"
}
:::
:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/moxGFPmuNS/MR.dzi"
}
:::
::::

:::{dropdown} Reveal the answer
The sample on the **left**, moxGFP:μNS(1-721), condenses more than the mutant (right).
:::

:::{dropdown} Methodological notes
CV-1 cells were seeded on 35mm glass-bottom dishes (20mm coverslips, no 1.5 glass).
pCI-neo moxGFP::μNS(1-721) and moxGFP::μNS(472-721) plasmids were transfected for 24 hours before PFA fixation.
2500 fields (50x50 grid) were imaged (100X objective).
Data was converted to 8-bit TIF, stitched, then converted to DZI format, hosted on Github Pages, and is viewed with OpenSeadragon.
:::

Barkley recognized the value of using virtual microscopy for replication studies.
This process involves automated sampling of reasonable populations from which the original claim should be reliably observed.
To test this, Barkley replicated an experiment that reported images without numerical results.
The original study showed apparent ER remodelling in reovirus-infected cells expressing mCherry-KDEL.
In replication attempts, ER remodelling can be observed in transfected cells expressing mCherry-KDEL in the absence of reovirus.
This suggests that experimental artifacts from mCherry-ER reporters could have been misinterpreted as an outcome of infection.
Otherwise, it is not clear that reovirus affects ER morphology, certainly not to the extent of fragmentation, collapse, and aggregation as originally described.
This conclusion challenges the claim of reovirus-induced ER remodelling [@doi:10.1128/mBio.01253-18], but it is uniquely open to scrutiny.

There are at least ten examples of objective representative image selection [@doi:10.1109/BIP60195.2023.10379342], yet there is no consensus on what is typical, so the task of image selection remains unsuitable for computer algorithms.
To this end, image categorization with an upstream classifier model could be an interesting future direction, because the two-step approach to image selection [@doi:10.1109/BIP60195.2023.10379342] was more effective with labels ([](#fig9a) and [](#fig9e)).
An important consideration is whether the dataset contains [continuous or discrete variables](<wiki:Continuous_or_discrete_variable>).
Classification would be futile with continuous data that lacks distinct phenotypes, in which case it makes sense to try the global average.
