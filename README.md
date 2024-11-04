# Hybrid Vision Transformer Systematic Review


### Hybrid Design Category
- Parallel: ViT and other techniques are located in parallel
- Fusing: ViT between Encoder and Decoder
- Stacking: ViT and CNN are implemented sequentially
- Gen NN: ViT in Generative Model

| Reference                        | Application  | Architecture | Merging                       | Transf. Util. | Transf. Backbone              | CNN Backbone                          |
|----------------------------------|--------------|--------------|-------------------------------|---------------|--------------------------------|---------------------------------------|
| U-net Transformer [36]           | Segmentation | Sequential   | Fusing                        | Encoder       | Multi-head Cross-Attention     | U-Net                                 |
| UTNet [7]                         | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Multi-head Self-Attention     | U-Net                                 |
| CPT U-Net [20]                   | Segmentation | Parallel     | Fusing                        | Encoder Decoder | Pyramid Vision Transformer   | U-Net                                 |
| UNETR [37]                        | Segmentation | Sequential   | Feature Reshaping             | Encoder       | Vision Transformer            | U-Net                                 |
| Swin UNETR [38]                   | Segmentation | Sequential   | Feature Reshaping Fusing      | Encoder       | Swin Transformer              | U-Net                                 |
| COTRNet [21]                      | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Light Vision Transformer      | U-Net                                 |
| Cotr [39]                         | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Deformable Transformer-encoder | U-Net                               |
| Hybrid ViT and CNN [24]           | Segmentation | Sequential   | Fusing                        | Encoder Decoder | Vision Transformer           | U-Net                                 |
| TransBTS [10]                     | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Light Vision Transformer      | U-Net                                 |
| Trans U-Net [22]                  | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Vision Transformer           | U-Net |
| Bitr U-Net [40]                   | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Vision Transformer           | U-Net, CBAM |
| After U-Net [41]                  | Segmentation | Sequential   | Feature Reshaping             | Encoder       | Axial Fusion Transformer      | U-Net |
| WAU [42]                          | Segmentation | Sequential   | Feature Reshaping             | Decoder       | Window Attention              | Group Conv, Depthwise Separable CNN   |
| HCTN [43]                         | Segmentation | Parallel     | Feature Reshaping             | Encoder       | Vision Transformer            | U-Net|
| Hybrid CNN-Transformer Non-Contrast [44] | Segmentation | Parallel | Fusing                        | Encoder       | Hierarchical Transformer      | U-Net|
| D-TA U-net [45]                  | Segmentation | Parallel     | Fusing                              | Encoder       | Swin Transformer             | U-Net       |
| MLABHCTMI [46]                   | Segmentation | Parallel     | Fusing                              | Encoder/Decoder | Transformer               | U-Net       |
| UCTNet [47]                      | Segmentation | Sequential   | Feature Reshaping                   | Encoder/Decoder | Transformer               | U-Net|
| HybridMT-ESTAN [48]              | Classification/Segmentation     | Parallel     | Feature Reshaping Fusing            | Encoder       | Swin Transformer| ResNet  |
| ChexViT [17]                     | Classification                  | Sequential   | Feature Reshaping Positional Encoding | Encoder    | Vision Transformer           | CheXNet [49]|
| TECNN [19] | Classification | Parallel     | Feature Reshaping Fusing            | Encoder       | Vision Transformer           | DenseNet  |
| SLATER [50] | Classification | Sequential   | Feature Reshaping Positional Encoding | Decoder   | Cross-Attention              | Specialized CNN                    |
| 3D Transformer GAN [18] | Reconstruction                  | Sequential   | Feature Reshaping Positional Encoding | Encoder Decoder | Vision Transformer     | Specialized CNN|
| T2Net [31] |Reconstruction| Sequential   |                                      | Encoder       | Task-Attention               | Specialized CNN |
| MIST-Net [50] | Reconstruction | Sequential   | Feature Reshaping Fusing            | Decoder       | Soft-Attention Swin Transformer | Specialized CNN                |
| Ultrasound ViT [30] | Regression | Sequential   | Feature Mapping                     | Encoder       | Bert                         | ResNetAE/DenseNet                  |
| DTN [25] |Regression| Sequential   | Feature Reshaping Fusing            | Encoder/Decoder | Dual Transformer            | Specialized CNN                    |
| ViT-V-Net [51] | Registration| Sequential   | Feature Reshaping Positional Encoding | Encoder    | Vision Transformer           | Specialized CNN |
| Transmorph [23] |Registration| Sequential   | Feature Reshaping                   | Encoder       | Swin Transformer             | U-Net                              |
| ResViT [29] | Image Synthesis                 | Sequential   | Feature Reshaping| Encoder       | Vision Transformer| Specialized CNN |
| TransCT [27]| Restoration| Parallel     | Feature Reshaping                   | Encoder Decoder | Vision Transformer         | Specialized CNN |
| Multi-View ViT [26]| Combining Views                 | Sequential   | Feature Reshaping                   | Encoder       | Cross View-Attention         | ResNet |
| AlignTransformer [52]| Report Generation| Sequential   | Feature Reshaping                   | Encoder       | Align Hierarchical-Attention | ResNet      |
| R2Gen [28]| Report Generation | Sequential   | Feature Reshaping                   | Encoder Decoder | Vision Transformer         | Pretrained (ResNet, VGG) |


|Reference                  |Modality       |Parameters(M)|Inference Time(GFLOPs)|Sample Size                              |Performance                        |
|---------------------------|---------------|-------------|-----------------------|------------------------------------------|-----------------------------------|
|U-net Transformer [36]     |CT             |42.5         |-                      |TCIA (public): 82 total                  |Dice: 0.78                         |
|UTNet [7]                  |MR             |14.4         |40.9                   |M&MS [53] Training: 150/Test: 200        |Dice: 0.88                         |
|CPT U-Net [20]             |CT             |12.3         |150.6                  |Synapse (public) 30                      |Dice: 0.81                         |
|UNETR [37]                 |CT/MRI         |92.5         |41                     |BTCV:20 objects, MSD: 484 ct/MRI, BraTS21|Dice: 0.89                         |
|Swin UNETR [38]            |MRI            |61.9         |394.8                  |Training: 1251/Val: 219                 |Dice: 0.92                         |
|COTRNet [21]               |CT             |-            |-                      |Kits21                                   |Dice: 0.61                         |
|Cotr [39]                  |CT             |41.9         |399.2                  |Training: 240/Val: 60                   |Dice: 0.61                         |
|Hybrid ViT and CNN [24]    |MRI            |-            |-                      |Synapse, BraTS21                        |Dice: 0.92                         |
|TransBTS [10]              |MRI            |32.9         |333.0                  |Training: 335/Val: 125                  |Dice: 0.87                         |
|Trans U-Net [22]           |CT/MRI         |105.1        |1186.9                 |Training: 18/Val: 12                    |Dice: 0.77                         |
|Bitr U-Net [40]            |MRI            |43.4         |186.2                  |BraTS21                                 |Dice: 0.92                         |
|After U-Net [41]           |MRI            |-            |-                      |BCV Training: 18/Test: 12               |-                                 |
|WAU [42]                   |CT/MRI         |21.8         |15.94                  |Synapse: 18                             |Dice: 0.83                         |
|HCTN [43]                  |X-Ray/MRI      |-            |-                      |STS Training: 45/Val: 5                 |Dice: 0.88                         |
|Hybrid CNN-Transformer [44]|CT             |38.94        |3.75                   |AISD Training: 305/Val: 52              |Dice: 0.61                         |
|D-TrAttNet [45]            |CT             |70.13        |28.47                  |BM Seg Dataset 1517                     |Dice: 0.84                         |
|MLABHCTMI [46]             |MRI            |1.8          |4.6                    |ACDC Training: 140/Val: 20/Test: 40     |Dice: 0.86                         |
|UCTNet [47]                |CT/MRI/Demoscopic|58.8       |21.7                   |ACDC Training: 70/Val: 10/Test: 20      |Dice: 0.92                         |
|HybridMT-ESTAN [48]        |Ultrasound     |-            |-                      |Private Dataset Total: 3320             |AUC: 0.82                          |
|ChexViT [17]               |X-Ray          |-            |-                      |ChestX-Ray14[54] Training: 36,524/Val: 25,596|AUC: 0.83               |
|TECNN [19]                 |MRI            |22.5         |-                      |BraTS, Figshare Training: 998+/Val: 285+/Test: 142+|Precision: 0.967 F1-Score: 0.968|
|SLATER [55]                |MRI            |36.0         |174.8                  |IXI Training: 25/Val: 5/Test: 10        |SSIM(72): 97.77                    |
|3D Transformer GAN [18]    |PET            |42.0         |-                      |Brain MRI                               |SSIM: 0.956                        |
|T2Net [31]                 |MRI            |1.4          |140.3                  |IXI Dataset, Clinical MRI Dataset Training: 420/Val: 60/Test: 120|SSIM: 0.87|
|MIST-Net [50]              |CT             |11.8         |576.0                  |2016 NIH AAPM/Mayo Challenge Training: 474 sinograms|MAE: 6.77                 |
|Ultrasound ViT [30]        |Echocardiogram |346.8        |521.7                  |Echonet-Dynamic Training: 7522/Val: 1504/Test: 1504|Dice: 0.76                 |
|DTN [25]                   |MRI            |-            |-                      |Oasis, IXI BraTS Training: 256/Val: 19/Test: 150|Dice: 0.72                 |
|ViT-V-Net [51]             |MRI            |31.5         |778.4                  |In-House T1 Weight Training: 182/Val: 26/Test: 52|Dice: 0.72                  |
|Transmorph [23]            |CT/MRI/XCAT    |46.7         |1427.0                 |Oasis Training: 256/Val: 19/Test: 150   |Dice: 0.816                        |
|ResViT [29]                |CT/MRI         |123.4        |973.0                  |IXI, BrainS, CT-MRI Training: 59/Val: 92/Test: 42|SSIM T1, T2->FLAIR: 0.836   |
|TransCT [27]               |CT             |12.6         |598.7                  |2016 NIH AAPM/Mayo Challenge Training: 7 patients/Val: 1/Test: 2|SSIM: 0.92             |
|Multi-View ViT [26]        |X-Ray          |23.6         |9.5                    |CheXpert Training: 23628 (16810 patients)|AUC: 0.834                        |
|AlignTransformer [52]      |X-Ray          |-            |-                      |MIMIC CXR Training: 368,960 Val: 2,991 Test: 5,159|BLEU1: 0.378              |
|R2Gen [28]                 |X-Ray          |78.4         |35.4                   |MIMIC CXR Training: 368,960 Val: 2,991 Test: 5,159|BLEU1: 0.353              |






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
