---
title: Discussion
numbering:
  enumerator: 0.%s
label : discussion_page
---

There is no consensus definition of science or the scientific method, but an essential principle is reproducibility.
Repeatability in microscopy is often shown with quantitative analyses.
However, without numerical results, representative images alone cannot communicate repeatability.
The reality is that representative images can show rare, idealized, or exaggerated examples to embellish results.
Microscopists are incentivized to show their best evidence and readers are none the wiser because the primary data is inaccessible.
This bottleneck in scientific communication can be expanded with virtual microscopy.
Barkley presented stitched panoramas of confocal data, but the approach is relevant to the broader bioimaging community.
For example, OME-Zarr supports several modalities including multiplexed imaging, spatial transcriptomics, light-sheet, infrared, scanning EM and digital pathology.
To improve accessibility for readers, it was important to use cloud storage and embedded viewers, which was supported by this journal.
Virtual microscopy requires an internet connection, but this limitation is unimportant because present and future scientific discourse uses computers, not paper.
This new tool for scientific communication can give all parties unprecedented exposure to data for review and critical evaluation.
Fraud prevention could incentivize publishers to adopt this technology to provide an alternative to representative images.

Barkley pushed for the utility of virtual microscopy in replication studies.
Unbiased replication involves automated sampling of reasonable populations from which the original claim should be reliably observed.
Barkley replicated a study that reported representative images without numerical results.
The original report observed ER remodelling in reovirus-infected cells expressing mCherry-KDEL.
In our replication study, Barkley observed ER remodelling in cells expressing mCherry-KDEL in the absence of reovirus infection.
This suggests that artifacts could have been misinterpreted as reovirus-induced ER remodelling in the original study.
In replicate microscopy maps, it was not clear that ER morphology was affected by reovirus, certainly not to the extent of fragmentation, collapse, and aggregation as originally described.
This conclusion challenges the claim of reovirus-induced ER remodelling [@doi:10.1128/mBio.01253-18] but it is open to scrutiny, just look for yourself.

Representative images are chosen by humans, who are flawed and biased, but the process of image selection is challenging to automate.
An approach with autoencoders was demonstrated, but it is irresponsible to use this method because neural networks are black boxes.
There is opportunity to improve the model with representation learning, but interpretability remains opaque.
Further, it could be that this approach requires label information for generalization ([](#fig9c) and [](#fig9f)).
To truly prevent cherry-picking, image selection can be avoided with virtual microscopy.
