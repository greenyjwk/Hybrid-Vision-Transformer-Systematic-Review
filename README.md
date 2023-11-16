# Hybrid-Vision-Transformer-Systematic-Review


### Hybrid Design Category
- Parallel: ViT and other technique are located in parallel
- Fusing: ViT between Encdoer and Decoder
- ViT in Generative Model: Gen NN

| Title | Year | Hybrid Design | Task | Dataset | Modality |
| ------------------------- |  -------- | -------- | -------- | -------- | -------- |
| TransFuse: Fusing Transformers and CNNs for Medical Image Segmentation | 2021 | ViT + CNN / Parallel | Segmentation | Prostate Multi-modality MRIs from the Medical Segmentation Decathl | MRI |
| U-net transformer: Self and cross attention for medical image segmentation | 2021 | ViT + CNN / Fusing | Segmentation | TCIA | CT |
| UTNet: A Hybrid Transformer Architecture for Medical Image Segmentation | 2021 | ViT + CNN / Stacking | Segmentation | multi-vendor cardiac magnetic resonance imaging | MRI |
| Bitr-unet: a cnn-transformer combined network for mri brain tumor segmentation | 2021 | ViT + CNN / Fusing | Segmentation | BRaTS dataset | MRI |
| After-unet: Axial fusion transformer unet for medical image segmentation | 2021 | ViT + CNN / Fusing | Segmentation | Abdomen CT Image | CT |
| A transformer-based framework for automatic COVID19 diagnosis in chest CTs | 2021 | Swin ViT + CNN / Stacking | Segmentation + Classification | MIA-COV19D competition dataset | CT |
| Unsupervised MRI reconstruction via zero-shot learned adversarial transformers | 2022 | Swin ViT + CNN / Gen NN / | Reconstruction | single-coil brain MRI data from IXI + fastMRI | MRI |
| Mr image super resolution by combining feature disentanglement cnns and vision transformers | 2022 | Swin ViT + CNN / Gen NN /  | Restoration | fastMRI and The IXI dataset | MRI |
| Learning dual transformer network for diffeomorphic registration | 2021 | ViT + CNN / Gen NN / Stacking | Registration | OASIS with 425 T1-weighted brain MRI scans | MRI |
| Multi-view analysis of unregistered medical images using cross-view transformers | 2021 | ViT + CNN / Stacking | Combining multiple MR Image View without registration | CheXpert, CBIS-DDSM | MRI |


| Learning to generate clinically coherent chest X-ray reports | 2021 | ViT + CNN / Stacking | Combining multiple MR Image View without registration | MIMIC-CXR | X-rays |
