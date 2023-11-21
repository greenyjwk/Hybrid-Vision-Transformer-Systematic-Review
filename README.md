# Hybrid Vision Transformer Systematic Review


### Hybrid Design Category
- Parallel: ViT and other technique are located in parallel
- Fusing: ViT between Encdoer and Decoder
- ViT in Generative Model: Gen NN


### Study Selection
| Title/Code | Year | Hybrid Design | Task | Dataset | Modality | Input Size
| ------------------------- |  -------- | -------- | -------- | -------- | -------- | -------- | 
| [TransFuse[1]](https://github.com/Rayicer/TransFuse) | 2021 | ViT + CNN / Parallel | Segmentation | Prostate Multi-modality MRIs from the Medical Segmentation Decathlon | MRI | MRIs from 32 patients, with volume shape of 20×320×3 |
| U-net transformer[2] | 2021 | ViT + CNN / Fusing | Segmentation | TCIA pancreas dataset / Internal multi-organ dataset(IMO) | CT | TCIA: 82 CT-scans and Multi-Organ(IMO): 85 CT Scans|
| [UTNet[3]](https://github.com/yhygao/UTNet) | 2021 | ViT + CNN / Stacking | Segmentation | multilabel, multi-vendor cardiac MRI cohort | MRI | 75 MRI from Siemens, 75 MRI from Philips
| [Bitr-unet[4]](https://github.com/BruceResearch/BiTr-Unet) | 2021 | ViT + CNN / Fusing | Segmentation | BRaTS 2021 | MRI | 200 MRI Scans
| After-unet[5] | 2021 | ViT + CNN / Fusing | Segmentation | Abdomen CT Image | CT | abdomen CT BCV:18/Thorax-85:60/SegTHOR: 30
| [A transformer-based framework for automatic COVID19 diagnosis in chest CTs[6]](https://github.com/leizhangtech/COVID19T) | 2021 | Swin ViT + CNN / Stacking | Segmentation + Classification | MIA-COV19D competition dataset | CT | 1560 CT Scans
| [Unsupervised MRI reconstruction via zero-shot learned adversarial transformers[7]](https://github.com/icon-lab/SLATER) | 2022 | Swin ViT + CNN / Gen NN / | Reconstruction | single-coil brain MRI data from IXI + fastMRI | MRI |
| [8]Mr image super resolution by combining feature disentanglement cnns and vision transformers | 2022 | Swin ViT + CNN / Gen NN /  | Restoration | fastMRI and The IXI dataset | MRI |
| [9]Learning dual transformer network for diffeomorphic registration | 2021 | ViT + CNN / Gen NN / Stacking | Registration | OASIS with 425 T1-weighted brain MRI scans | MRI |
| [10]Multi-view analysis of unregistered medical images using cross-view transformers | 2021 | ViT + CNN / Stacking | Combining multiple MR Image View without registration | CheXpert and CBIS-DDSM | MRI |
| PubMedCLIP[11] | 2021 | ViT + CNN / Stacking | Vision Question and answer | VQA-RAD and SLAKE | X-ray |
| Ultrasound video transformers for cardiac ejection fraction estimation | 2021 | ViT + CNN / Stacking | Cardiac Ejection Fraction Prediction | Echonet-Dynamic dataset | Ultrasound |



# Reference
1. TransFuse: Fusing Transformers and CNNs for Medical Image Segmentation
2. U-net transformer: Self and cross attention for medical image segmentation
3. UTNet: A Hybrid Transformer Architecture for Medical Image Segmentation
4. Bitr-unet: a cnn-transformer combined network for mri brain tumor segmentation
5. After-unet: Axial fusion transformer unet for medical image segmentation
6. A transformer-based framework for automatic COVID19 diagnosis in chest CTs
7. a
8. a
9. a
10. a
11. PubMedCLIP: How Much Does CLIP Benefit Visual Question Answering in the Medical Domain?
