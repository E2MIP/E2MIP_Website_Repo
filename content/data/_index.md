---
title: Data
weight: 2
---

Two datasets are used for this challenge. Their complementary nature allows for assessing different aspects of the development phase.

### 🗃️ Dataset 1 (Lung Nodule) 
Here, the public LIDC-IDRI dataset will be used. It contains more than 1.000 CT images of patients with lung nodules. All images have been annotated by experts with segmentations (for nodules > 3mm) and a malignancy rating. The corresponding publications give a detailed description of the dataset ([10.7937/K9/TCIA.2015.LO9QL9SX](https://doi.org/10.7937/K9/TCIA.2015.LO9QL9SX) , [10.1118/1.3528204](https://doi.org/10.1118/1.3528204) )
The dataset can be downloaded from the [The Cancer Imaging Archive (TCIA)](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=1966254). Beside the images and annotations, this includes additional description and details of the dataset. 

### 🗃️ Dataset 2 (Fetal brain MRI)
This dataset consists of T2-weighted and diffusion-weighted MRI scans of fetal brains. The brain has been manually segmented by an expert to provide ground truth labels. The dimensions of T2-weighted and diffusion-weighted MRI images, respectively, are 256 x 256 x S and 128 x 128 x S voxels, where S is the number of slices in the scan. In other words, the size of each 2D slice for T2-weighted and diffusion-weighted scans are 256 x 256 and 128 x 128, respectively. The within-slice resolutions vary. Scans are available as NIfTI files (.nii.gz).
