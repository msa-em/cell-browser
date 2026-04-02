---
title: Discussion
numbering:
  enumerator: 0.%s
---

Every academic discipline has its own ways of deciding what counts as valid knowledge (see [epistemology](<wiki:Epistemology>)).
If biomedical researchers endorse [empiricism](<wiki:Empiricism>) and objectivity, then why are representative images sufficient to make claims?
A representative image definitively shows that an observation is possible, but a single image cannot describe frequency or variance.
There is disagreement on the [scientific method](<wiki:Scientific_method>), but a general principle is [reproducibility](<wiki:Reproducibility>).
Repeatability in microscopy involves quantitative analyses, but without numerical results, representative images cannot communicate repeatability.
The reality is that representative images can show rare, idealized, or exaggerated examples to embellish results.
Microscopists are incentivized to show compelling evidence and omit contradictory data.
The literature is full of exciting outcomes, but at the bench, experiments are nuanced and prone to failure.

Representative images are figures, which should not be confused with data.
Data is the unprocessed file from the microscope, while figures are visual representations of data, shaped by the microscopist.
Figures are the interface for peer review between the experimentalist and coauthors, principal investigators, reviewers and readers.
Indeed, peer review seldom involves data and scientific discourse is limited by the information provided in figures.
This bottleneck is expanded by virtual microscopy, which is practical to the broader bioimaging community.
For example, OME-Zarr [@doi:10.1007/s00418-023-02209-1] supports several modalities including multiplexed imaging, spatial transcriptomics, light-sheet, infrared, scanning EM and digital pathology.
To maximize accessibility for readers, embedded interactive viewports retrieve data from cloud storage, which was supported by this journal.
Virtual microscopy requires an internet connection, but this limitation is relatively unimportant for contemporary and future publishing.
Web-based microscopy maps are trivial to make and share on Github [@doi:10.1242/jcs.262198], so they can be readily requested by reviewers of all journals.
Fraud prevention could incentivize publishers to adopt this technology as an alternative to static figures.
Because it nurtures open and rigorous peer review, microscopists and principal investigators might find virtual microscopy advantageous to make more robust claims with their bioimaging data.

Barkley advocated for the use of virtual microscopy as an unbiased method to replicate highly magnified representative images.
This process involves automated sampling of reasonable populations from which the original claim should be reliably observed.
Virtual microscopy is unbiased insofar as the data is collected with robotics and is shared interactively on the web.
To test this approach to replication, an immunofluorescence imaging experiment in reovirus-infected cells [@doi:10.1128/mBio.01253-18] was reexamined with virtual microscopy.
Barkley thought that fluorescent proteins could have restructured the ER [@doi:10.1083/jcb.200306020], which was not addressed by the previous investigators.
In replication attempts, ER remodeling was observed in transfected cells expressing mCherry-KDEL in the absence of reovirus.
This suggests that artifacts from mCherry-ER reporters could have been misinterpreted as an outcome of infection.
Otherwise, it is not clear that reovirus affects ER morphology, certainly not to the extent of fragmentation, collapse, and aggregation as described.
Barkley concluded that reovirus-induced ER remodeling was unsubstantiated due to confounding experimental artifacts, though this interpretation was influenced by confirmation bias.
Coauthors were asked to provide independent interpretations of the data.
Recently, reovirus-induced ER remodeling was associated with annexin a2 [@doi:10.1128/jvi.01389-25].

There are at least ten examples of objective representative image selection [@doi:10.1109/BIP60195.2023.10379342], but what is 'representative' in a dataset needs further deliberation.
To this end, image categorization with an upstream classifier model could be a productive future direction for this task.
Criteria to evaluate methods of representative image selection were also lacking, though a reasonable benchmark is the consistency in which members of the majority class are selected (https://doi.org/10.1016/s0006-3495(99)77379-0).
This frames representative image selection as the inverse of anomaly detection, however, not all biological datasets are classifiable.
