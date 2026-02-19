---
title: Discussion
numbering:
  enumerator: 0.%s
label : discussion_page
---

There is no consensus on the scientific method (or knowledge, see [epistemology](<wiki:Epistemology>)), but a general principle is reproducibility.
Repeatability in microscopy is shown with quantitative analyses.
However, without numerical results, representative images alone cannot communicate repeatability.
The reality is that representative images can show rare, idealized, or exaggerated examples to embellish results.
Microscopists are incentivized to show the best evidence and omit contradictory data.
Figures are not to be confused with data.
Data is the raw file from the microscope, while figures are visual representations of data shaped by the microscopist.
Indeed, peer review by coauthors, principal investigators, reviewers, and readers is often limited to the information provided in figures.
The literature is full of exciting outcomes, but at the bench, data is messy, nuanced, and experiments are prone to failure. 

This bottleneck is expanded using virtual microscopy, which is relevant for the broader bioimaging community.
For example, the OME-Zarr format supports several modalities including multiplexed imaging, spatial transcriptomics, light-sheet, infrared, scanning EM and digital pathology.
To maximize accessibility for readers, it was important to embed viewports that retrieved data from the cloud, which was supported by this journal.
Virtual microscopy requires a computer with internet connection, but this limitation is unimportant for contemporary and future publishing which is online.
This new tool gives readers unprecedented exposure to data, promoting open peer review and critical evaluation.
Web-based microscopy maps are trivial to make and share on Github [@doi:10.1242/jcs.262198], so reviewers could request that authors share data with virtual microscopy in the peer review process of other journals.
Fraud prevention could incentivize publishers to adopt this technology and offer it to microscopists as an alternative to representative images.

Barkley recognized the value of virtual microscopy for replication studies.
This process involves automated sampling of reasonable populations from which the original claim should be reliably observed.
Barkley replicated an experiment that reported representative images without numerical results.
The original study showed apparent ER remodelling in reovirus-infected cells expressing mCherry-KDEL.
In our replication study, Barkley observed ER remodelling in cells expressing mCherry-KDEL in the absence of reovirus.
This suggests that artifacts from mCherry-ER reporters could have been misinterpreted as a symptom of viral infection.
In replicate experiments, it was not clear that reovirus affected ER morphology, certainly not to the extent of fragmentation, collapse, and aggregation as originally described.
This conclusion challenges the claim of reovirus-induced ER remodelling [@doi:10.1128/mBio.01253-18] but it is open to public scrutiny.

There are at least ten examples of objective representative image selection cited in a recent article [@doi:10.1109/BIP60195.2023.10379342].
This means that researchers have proposed various methods but there is no agreement, in part because it remains challenging to define 'representativeness' (https://doi.org/10.1016/s0006-3495(99)77379-0).
Thus, the task of image selection is unsuitable for computer algorithms because interpeting the output is subjective and context-dependent.
It could be that the two-step approach to image selection [@doi:10.1109/BIP60195.2023.10379342] requires labels for generalization ([](#fig9c) and [](#fig9f)).
In that case, a future direction could be image categorization with an upstream classifier model before downstream objective image selection.

::::{grid} 1 1 1 1

:::{any:bundle} https://curvenote.github.io/widgets/widgets/vizarr-viewer.js

{
  "source": "https://barkley-replication.s3.us-east-2.amazonaws.com/mNGmuNS_mCherryKDEL.zarr/",
  "height": "600px"
}

:::

::::