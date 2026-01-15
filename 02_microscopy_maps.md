---
title: Microscopy Maps
numbering:
  enumerator: 2.%s
label : maps_page
---

Virtual nanoscopy was the methodology used to provide unbiased access to high-resolution gigapixel microscopy images with downloadable tools [@doi:10.1083/jcb.201201140].
It described the automated acquisition of image tiles that were then processed into multi-resolution image pyramids to be viewed as digital maps.
There are many ways to make and share microscopy maps, including free and open-source methods [@doi:10.1242/jcs.262198].
As described elsewhere [@doi:10.1242/jcs.262198], one method is to convert stitched images to the deep zoom image (DZI) file format, which is a multi-resolution image pyramid, to be hosted and viewed on Github. 
For publication in static figures, a link or QR code then takes the reader away from the article to view the map.
Here, OpenSeadragon was embedded into the article to view microscopy maps in DZI format hosted on Github as a free and open-source demonstration of virtual nanoscopy in the literature.
An advanced method that was suggested was to reformat the raw data to the next generation file format OME-Zarr to host in S3 storage for retrieval [@doi:10.1242/jcs.262198].


Here, two different approaches were 

and an advanced approach is to reformat raw data to OME-Zarr for hosting and retrieval in S3 storage.

- BioFormats used to convert raw native microscopy data files into OME-Zarr format.
- OME-Zarr format is a cloud-optimized next generation file format that can chunk data into a multi-resolution pyramid.
- Hosted in S3 storage.
- Chunks retrieved by Vizarr as readers interact with the map.