---
title: Discussion
numbering:
  enumerator: 10.%s
label : discussion_page
---

Every academic discipline has its ways of deciding what counts as valid knowledge (see [epistemology](<wiki:Epistemology>)).
If biomedical researchers endorse [empiricism](<wiki:Empiricism>) and objectivity, then why are representative microscopy images sufficient to make claims?
A representative image definitively shows that an observation is possible, but it does not describe frequency or variance.
There is disagreement on the scientific method, but a general principle is reproducibility.
Repeatability in microscopy can be described with quantitative analyses.
However, without numerical results, representative images cannot communicate repeatability.
The reality is that representative images can show rare, idealized, or exaggerated examples to embellish results.
Microscopists are incentivized to show compelling evidence and omit contradictory data.
The literature is full of exciting outcomes, but at the bench, data is messy, nuanced, and experiments are prone to failure.

Representative images are figures, which is not to be confused with data.
Data is the raw file from the microscope, while figures are visual representations of data, shaped by the microscopist.
Figures are the interface for peer review between the experimentalist and coauthors, principal investigators, reviewers and readers.
Indeed, peer review seldom involves data and discourse is limited to the information provided in figures.
This bottleneck can be expanded with virtual microscopy, which is practical to the broader bioimaging community.
For example, the OME-Zarr format supports several modalities including multiplexed imaging, spatial transcriptomics, light-sheet, infrared, scanning EM and digital pathology.
To maximize accessibility for readers, we embedded interactive viewports that stream data from the cloud, which was supported by this journal.
Virtual microscopy requires an internet connection, but this limitation is relatively unimportant for contemporary publishing.
This new tool gives readers unprecedented exposure to data, promoting open peer review.
Web-based microscopy maps are trivial to make and share on Github [@doi:10.1242/jcs.262198], so virtual microscopy could be requested from reviewers during peer review in other journals.
Fraud prevention could incentivize journals to adopt this technology as an alternative to static figures.
Scientists and principal investigators could use virtual microscopy to make more robust claims.
For example, below are microscopy maps of transfected cells expressing moxGFP::μNS.
The wildtype full-length construct on the left formed more [biomolecular condensates](<wiki:Biomolecular_condensates>) than the mutant on the right:

::::{grid} 2 2 2 2
:::{any:bundle} https://curvenote.github.io/widgets/widgets/openseadragon.mjs
{
    "tileSources": "https://russellbarkley.github.io/moxGFPmuNS/FL_MR.dzc"
}
:::
::::

Barkley recognized the value of virtual microscopy for replication studies.
This process involves automated sampling of reasonable populations from which the original claim should be reliably observed.
Barkley replicated an experiment that reported representative images without numerical results.
The original study showed apparent ER remodelling in reovirus-infected cells expressing mCherry-KDEL.
In our replication study, Barkley observed ER remodelling in cells expressing mCherry-KDEL in the absence of reovirus.
This suggests that artifacts from mCherry-ER reporters could have been misinterpreted as a symptom of viral infection.
In replicate experiments, it was not clear that reovirus affected ER morphology, certainly not to the extent of fragmentation, collapse, and aggregation as originally described.
This conclusion challenges the claim of reovirus-induced ER remodelling [@doi:10.1128/mBio.01253-18] but it is open to public scrutiny.

There are at least ten examples of objective representative image selection that were cited in the most recent article [@doi:10.1109/BIP60195.2023.10379342].
However, there is no consensus, in part because it is challenging to define representativeness (https://doi.org/10.1016/s0006-3495(99)77379-0).
The task of image selection remains unsuitable for computer algorithms because interpeting the output is subjective and context-dependent.
It could be that the two-step approach to image selection [@doi:10.1109/BIP60195.2023.10379342] requires labels for generalization ([](#fig9c) and [](#fig9f)).
Perhaps these methods would benefit from image categorization with an upstream classifier model before objective image selection.