---
title: Discussion
numbering:
  enumerator: 0.%s
label : discussion_page
---

There is no consensus on the scientific method, but a core principle is reproducibility.
Repeatability in microscopy is shown with quantitative analyses.
However, without numerical results, representative images alone cannot communicate repeatability.
The reality is that representative images can show rare, idealized, or exaggerated examples to embellish results.
Microscopists are incentivized to show the best evidence and hide the rest.
This bottleneck in scientific communication is expanded with virtual microscopy, which is relevant to the broader bioimaging community.
For example, OME-Zarr supports several modalities including multiplexed imaging, spatial transcriptomics, light-sheet, infrared, scanning EM and digital pathology.
To maximize accessibility for readers, it was important to use cloud storage and embedded viewers, which was supported by this journal.
Virtual microscopy requires an internet connection, but this limitation is unimportant because scientific publishing is now online, not on paper.
This new tool for scientific communication gives all parties unprecedented exposure to primary data, promoting open review and critical evaluation.
Web-based microscopy maps are sharable on Github [@doi:10.1242/jcs.262198], so reviewers can use virtual microscopy in the peer review process of other journals.
Fraud prevention could incentivize publishers to adopt this technology as an alternative visualization tool.

Barkley recognized the value of virtual microscopy for replication studies.
This process involves automated sampling of reasonable populations from which the original claim should be reliably observed.
Barkley replicated an experiment that reported representative images without numerical results.
The original study showed apparent ER remodelling in reovirus-infected cells expressing mCherry-KDEL.
In our replication study, Barkley observed ER remodelling in cells expressing mCherry-KDEL in the absence of reovirus.
This suggests that artifacts from mCherry-ER reporters could have been misinterpreted as a symptom of infection.
In replicate experiments, it was not clear that reovirus affected ER morphology, certainly not to the extent of fragmentation, collapse, and aggregation as originally described.
This conclusion challenges the claim of reovirus-induced ER remodelling [@doi:10.1128/mBio.01253-18] and it is open to public scrutiny.

The task of image selection was difficult to automate.
An approach was demonstrated, but it was irresponsible to use autoencoders because neural networks are black boxes.
There is room for improvement with representation learning, but the interpretability remains opaque.
It could be that this approach requires labels for generalization ([](#fig9c) and [](#fig9f)).
To truly prevent cherry-picking, image selection should be avoided using virtual microscopy.
