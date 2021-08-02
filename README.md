# nnunet on BRATS2020 dataset
nnU-Net
In 3D biomedical image segmentation, dataset properties like imaging modality, image sizes, voxel spacings, class ratios etc vary drastically. For example, images in the Liver and Liver Tumor Segmentation Challenge dataset are computed tomography (CT) scans, about 512x512x512 voxels large, have isotropic voxel spacings and their intensity values are quantitative (Hounsfield Units). The Automated Cardiac Diagnosis Challenge dataset on the other hand shows cardiac structures in cine MRI with a typical image shape of 10x320x320 voxels, highly anisotropic voxel spacings and qualitative intensity values. In addition, the ACDC dataset suffers from slice misalignments and a heterogeneity of out-of-plane spacings which can cause severe interpolation artifacts if not handled properly.

In current research practice, segmentation pipelines are designed manually and with one specific dataset in mind. Hereby, many pipeline settings depend directly or indirectly on the properties of the dataset and display a complex co-dependence: image size, for example, affects the patch size, which in turn affects the required receptive field of the network, a factor that itself influences several other hyperparameters in the pipeline. As a result, pipelines that were developed on one (type of) dataset are inherently incomaptible with other datasets in the domain.

nnU-Net is the first segmentation method that is designed to deal with the dataset diversity found in the domain. It condenses and automates the keys decisions for designing a successful segmentation pipeline for any given dataset.

nnU-Net makes the following contributions to the field:

Standardized baseline: nnU-Net is the first standardized deep learning benchmark in biomedical segmentation. Without manual effort, researchers can compare their algorithms against nnU-Net on an arbitrary number of datasets to provide meaningful evidence for proposed improvements.
Out-of-the-box segmentation method: nnU-Net is the first plug-and-play tool for state-of-the-art biomedical segmentation. Inexperienced users can use nnU-Net out of the box for their custom 3D segmentation problem without need for manual intervention.
Framework: nnU-Net is a framework for fast and effective development of segmentation methods. Due to its modular structure, new architectures and methods can easily be integrated into nnU-Net. Researchers can then benefit from its generic nature to roll out and evaluate their modifications on an arbitrary number of datasets in a standardized environment.
