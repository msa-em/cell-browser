---
title: Discussion
numbering:
  enumerator: 0.%s
label : discussion_page
---

Every academic discipline has its ways of deciding what counts as valid knowledge (see [epistemology](<wiki:Epistemology>)).
If biomedical researchers endorse [empiricism](<wiki:Empiricism>) and objectivity, then why are representative images sufficient to make claims?
A representative image definitively shows that an observation is possible, but one image cannot describe its frequency or variance.
There is disagreement on the [scientific method](<wiki:Scientific_method>), but a general principle is [reproducibility](<wiki:Reproducibility>).
Repeatability in microscopy involves quantitative analyses.
However, without numerical results, representative images alone cannot communicate repeatability.
The reality is that representative images can show rare, idealized, or exaggerated examples to embellish results.
Microscopists are incentivized to show compelling evidence and omit contradictory data.
The literature is full of exciting outcomes, but at the bench, data is messy, nuanced, and experiments are prone to failure.

Representative images are figures, which is not to be confused with data.
Data is the raw file from the microscope, while figures are visual representations of data, often shaped by the microscopist.
Figures are the interface for peer review between the experimentalist and coauthors, principal investigators, reviewers and readers.
Indeed, peer review seldom involves data and scientific discourse is limited by the information provided in figures.
This bottleneck can be expanded with virtual microscopy, which is practical to the broader bioimaging community.
For example, the OME-Zarr format supports several modalities including multiplexed imaging, spatial transcriptomics, light-sheet, infrared, scanning EM and digital pathology.
To maximize accessibility for readers, embedded interactive viewports retrieve data from cloud storage, which was supported by this journal.
Virtual microscopy requires an internet connection, but this limitation is relatively unimportant for contemporary and future publishing.
Web-based microscopy maps are trivial to make and share on Github [@doi:10.1242/jcs.262198], so it can be readily requested by reviewers of all journals.
Fraud prevention could incentivize publishers to adopt this technology as an alternative to static figures.
Virtual microscopy nurtures open and rigorous peer review, so scientists and principal investigators can leverage it to make robust claims backed by data.

Barkley recognized the value of virtual microscopy for replication studies.
This process involves automated sampling of reasonable populations from which the original claim should be reliably observed.
To test this, Barkley replicated an experiment that reported images without numerical results.
The original study showed apparent ER remodelling in reovirus-infected cells expressing mCherry-KDEL.
In replication attempts, Barkley observed ER remodelling in cells expressing mCherry-KDEL in the absence of reovirus.
This suggests that experimental artifacts from the mCherry-ER reporters could have been misinterpreted as an outcome of reovirus infection.
It is not clear that reovirus affects ER morphology, certainly not to the extent of fragmentation, collapse, and aggregation as originally described.
This interpretation challenges the claim of reovirus-induced ER remodelling [@doi:10.1128/mBio.01253-18], but it is uniquely open to public scrutiny.

There are at least ten examples of objective representative image selection [@doi:10.1109/BIP60195.2023.10379342], yet there is no consensus because of the challenges in defining what is typical of a set (https://doi.org/10.1016/s0006-3495(99)77379-0).
This task of image selection remains unsuitable for computer algorithms because interpetations of the result are subjective and context-dependent.
To this end, image categorization with upstream classifier models could be an interesting future direction.
The two-step approach to image selection [@doi:10.1109/BIP60195.2023.10379342] seemed to make more sense with labels (compare [subset](#fig9c) to [dataset](#fig9f)).
