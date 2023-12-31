# Hybrid Vision Transformer Systematic Review


### Hybrid Design Category
- Parallel: ViT and other techniques are located in parallel
- Fusing: ViT between Encoder and Decoder
- Stacking: ViT and CNN are implemented sequentially
- Gen NN: ViT in Generative Model


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
| MR image super resolution by combining feature disentanglement CNNs and vision transformers[8] | 2022 | ViT(UNETR) + CNN / Gen NN /  | Restoration | fastMRI and The IXI dataset | MRI | fastMRI:500, IXI dataset:500 |
| Learning dual transformer network for diffeomorphic registration[9] | 2021 | ViT + CNN / Gen NN / Stacking | Diffeomorphic Registration | OASIS with 425 T1-weighted brain MRI scans | MRI |
| [Multi-view analysis of unregistered medical images using cross-view transformers[10]](https://github.com/gvtulder/cross-view-transformers) | 2021 | ViT + CNN / Stacking | Combining multiple MR Image View without registration | CheXpert and CBIS-DDSM | MRI | cheXpert: 23628 samples, CBIS-DDSM: 708 samples
| PubMedCLIP[11] | 2021 | ViT + CNN / Stacking | Vision Question and answer | VQA-RAD and SLAKE | X-ray | 
| Ultrasound video transformers for cardiac ejection fraction estimation[12] | 2021 | ViT + CNN / Stacking | Cardiac Ejection Fraction Prediction | Echonet-Dynamic dataset | Ultrasound | 
| More than encoder: Introducing transformer decoder to upsample[13] | 2022 | ViT + CNN / Stacking | Segmentation | MSD Task01 BrainTumour, Synapse, ACDC | MRI | MSD Brain: 484 multimodal multisite MRI data, Synapse: 30 cases, ACDC: 100 cases
| [MIST-Net[14]](https://zenodo.org/records/6368099) | 2022 | ViT + CNN / Stacking | Reconstruction | NIH-AAPM-Mayo Low-dose CT| CT |
| [TECNN[15]](https://zenodo.org/records/6368099) | 2023 | ViT + CNN / parallel | Classification | BraTS 2018, Figshare | MRI |
| Hybrid Transformer and Convolution for Medical Image Segmentation[16] | 2022 | ViT + CNN / Stacking | Segmentation | Synapse, multiorgan segmentation | CT |
| Medical image segmentation using levit-unet++: A case study on gi tract data[17] | 2022 | ViT + CNN / Stacking | Segmentation | UW-Madison GI Tract Image Segmentation| MRI | 
| [TransBTS[18]](https://github.com/Rubics-Xuan/TransBTS) | 2021 | ViT + CNN / Between | Segmentation | BraTS 2019/2020 | MRI | 
| [Swin UNETR[19]](https://github.com/Project-MONAI/research-contributions/tree/main/SwinUNETR) | 2021 | ViT + CNN / Stacking(Swin Transformer in Encoder) | Segmentation | BraTS 2021 | MRI | 
| [TransCT[20]](https://github.com/zzc623/TransCT) | 2021 | ViT + CNN / Stacking | Restoration | 2016 NIH AAPM-Mayo Clinic Low-Dose CT | CT |
| [T2Net[21]](https://github.com/chunmeifeng/T2Net) | 2021 | ViT + CNN / Stacking | Reconstruction & Super Resolution| public IXI, clinical brain MRI Dataset | MRI |
| [TranSMS[22]](https://github.com/icon-lab/TranSMS) | 2022 | ViT + CNN / Parallel | Reconstruction & Super Resolution| in-house MPI, Open MPI Dataset | MPI |


# Reference
1. TransFuse: Fusing Transformers and CNNs for Medical Image Segmentation
2. U-net transformer: Self and cross attention for medical image segmentation
3. UTNet: A Hybrid Transformer Architecture for Medical Image Segmentation
4. Bitr-unet: a cnn-transformer combined network for MRI brain tumor segmentation
5. After-unet: Axial fusion transformer unet for medical image segmentation
6. A transformer-based framework for automatic COVID19 diagnosis in chest CTs
7. Unsupervised MRI reconstruction via zero-shot learned adversarial transformers
8. MR image super resolution by combining feature disentanglement CNNs and vision transformers
9. Learning dual transformer network for diffeomorphic registration
10. Multi-view analysis of unregistered medical images using cross-view transformers
11. PubMedCLIP: How Much Does CLIP Benefit Visual Question Answering in the Medical Domain?
12. Ultrasound video transformers for cardiac ejection fraction estimation
13. More than encoder: Introducing transformer decoder to upsample
14. Multi-domain Integrative Swin Transformer network for Sparse-View Tomographic Reconstruction
15. Combining the Transformer and Convolution for Effective Brain Tumor Classification Using MRI Images
16. Hybrid Transformer and Convolution for Medical Image Segmentation
17. Medical image segmentation using levit-unet++: A case study on gi tract data
18. TransBTS: Multimodal Brain Tumor Segmentation Using Transformer
19. Swin unetr: Swin transformers for semantic segmentation of brain tumors in MRI images
20. TransCT: Dual-path Transformer for Low Dose Computed Tomography
21. Task Transformer Network for Joint MRI Reconstruction and Super-Resolution
22. TranSMS: Transformers for super-resolution calibration in magnetic particle imaging
