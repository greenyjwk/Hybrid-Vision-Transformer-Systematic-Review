# Hybrid Vision Transformer Systematic Review


### Hybrid Design Category
- Parallel: ViT and other technique are located in parallel
- Fusing: ViT between Encdoer and Decoder
- ViT in Generative Model: Gen NN


### Study Selection
| Title | Year | Hybrid Design | Task | Dataset | Modality | Input Size
| ------------------------- |  -------- | -------- | -------- | -------- | -------- | -------- | 
| TransFuse[1] | 2021 | ViT + CNN / Parallel | Segmentation | Prostate Multi-modality MRIs from the Medical Segmentation Decathl | MRI |
| U-net transformer[2] | 2021 | ViT + CNN / Fusing | Segmentation | TCIA | CT |
| UTNet[3] | 2021 | ViT + CNN / Stacking | Segmentation | multi-vendor cardiac magnetic resonance imaging | MRI |
| Bitr-unet[4] | 2021 | ViT + CNN / Fusing | Segmentation | BRaTS dataset | MRI |
| After-unet[5]: Axial fusion transformer unet for medical image segmentation | 2021 | ViT + CNN / Fusing | Segmentation | Abdomen CT Image | CT |
| A transformer-based framework for automatic COVID19 diagnosis in chest CTs | 2021 | Swin ViT + CNN / Stacking | Segmentation + Classification | MIA-COV19D competition dataset | CT |
| Unsupervised MRI reconstruction via zero-shot learned adversarial transformers | 2022 | Swin ViT + CNN / Gen NN / | Reconstruction | single-coil brain MRI data from IXI + fastMRI | MRI |
| Mr image super resolution by combining feature disentanglement cnns and vision transformers | 2022 | Swin ViT + CNN / Gen NN /  | Restoration | fastMRI and The IXI dataset | MRI |
| Learning dual transformer network for diffeomorphic registration | 2021 | ViT + CNN / Gen NN / Stacking | Registration | OASIS with 425 T1-weighted brain MRI scans | MRI |
| Multi-view analysis of unregistered medical images using cross-view transformers | 2021 | ViT + CNN / Stacking | Combining multiple MR Image View without registration | CheXpert and CBIS-DDSM | MRI |
| PubMedCLIP: How Much Does CLIP Benefit Visual Question Answering in the Medical Domain? | 2021 | ViT + CNN / Stacking | Vision Question and answer | VQA-RAD and SLAKE | X-ray |
| Ultrasound video transformers for cardiac ejection fraction estimation | 2021 | ViT + CNN / Stacking | Cardiac Ejection Fraction Prediction | Echonet-Dynamic dataset | Ultrasound |



# Reference
1. TransFuse: Fusing Transformers and CNNs for Medical Image Segmentation
2. U-net transformer: Self and cross attention for medical image segmentation
3. UTNet: A Hybrid Transformer Architecture for Medical Image Segmentation
4. Bitr-unet: a cnn-transformer combined network for mri brain tumor segmentation
5. After-unet: Axial fusion transformer unet for medical image segmentation
6. a
7. a
8. 
