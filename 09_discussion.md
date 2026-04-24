---
title: Discussion
numbering:
  enumerator: 0.%s
---

Every academic discipline has its own ways of deciding what counts as valid knowledge (see [epistemology](<wiki:Epistemology>)).
If biomedical researchers endorse [empiricism](<wiki:Empiricism>) and objectivity, then why are representative images sufficient to make claims?
A representative image definitively shows that an observation is possible, but a single image cannot describe frequency or variance.
It is like [Schrödinger's cat](<wiki:Schrödinger's_cat>), where unobserved systems have combinations of outcomes that are never observed simultaneously.
Virtual microscopy makes this easily exploitable system significantly harder to game.
A general principle of the [scientific method](<wiki:Scientific_method>) is [reproducibility](<wiki:Reproducibility>).
Repeatability is often described using quantitative analysis, but without numerical results, representative images cannot communicate repeatability.
The reality is that representative images can show rare, idealized, or exaggerated examples to embellish results.
Microscopists are incentivized to show compelling evidence and omit contradictory data.
The literature is full of exciting outcomes, but at the bench, experiments are nuanced and prone to failure.

Representative images are figures, which should not be confused with data.
Data is the unprocessed file from the microscope, while figures are visual representations of data, shaped by the microscopist.
Figures are the interface for peer review between the experimentalist and coauthors, principal investigators, reviewers and readers.
Indeed, peer review seldom involves data and scientific discourse is limited by the information provided in figures.
This bottleneck is expanded by virtual microscopy, which is practical to the broader bioimaging community.
For example, OME-Zarr [@doi:10.1007/s00418-023-02209-1] supports several modalities including multiplexed imaging, spatial transcriptomics, light-sheet, infrared, scanning EM and digital pathology.
To maximize accessibility for readers, embedded interactive viewers retrieve data from cloud storage, which was supported by this journal.
Virtual microscopy requires an internet connection, but this limitation is relatively unimportant for contemporary and future publishing.
Web-based microscopy maps are trivial to make and share on Github [@doi:10.1242/jcs.262198], so they can be readily requested by reviewers of all journals.
Fraud prevention could incentivize publishers to adopt this technology as an alternative to static figures.
Because it nurtures open and rigorous peer review, microscopists and principal investigators might find virtual microscopy advantageous to make more robust claims with their bioimaging data.

Barkley advocated for the use of virtual microscopy as an unbiased method to replicate highly magnified representative images.
This process involves automated sampling of reasonable populations from which the original claim should be reliably observed.
Virtual microscopy is unbiased to the extent that the data was sampled with robotics and is shared interactively on the web.
To test this approach, an immunofluorescence imaging experiment in reovirus-infected cells [@doi:10.1128/mBio.01253-18] was reexamined with virtual microscopy.
Barkley hypothesized that fluorescent proteins could have restructured the ER [@doi:10.1083/jcb.200306020], which was not addressed by the previous investigators.
In replication attempts, ER remodeling was observed in transfected cells expressing mCherry-KDEL in the absence of reovirus.
This suggests that artifacts from mCherry-ER reporters could have been misinterpreted as an outcome of infection.
Otherwise, it was not clear that reovirus affected ER morphology, certainly not to the extent of fragmentation, collapse, and aggregation as described, though we recognized this interpretation was influenced by confirmation bias.
Virtual microscopy improves the use, interpretation, and communication of scientific data, subjecting the results of replication experiments to unbiased peer review.
