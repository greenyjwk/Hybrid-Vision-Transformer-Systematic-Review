# Systematic Review of Hybrid Vision Transformer Architectures for Radiological Image Analysis


### Comparative analysis of the existing hybrid architectures
It performed based on the criteria defined in Sec.2.2. Studies are grouped based on the targeted
applications. ‘Transf.’, ‘Util.’ refers to Transformer and Utility respectively.

| Reference                        | Application  | Architecture | Merging                       | Transf. Util. | Transf. Backbone              | CNN Backbone                          |
|----------------------------------|--------------|--------------|-------------------------------|---------------|--------------------------------|---------------------------------------|
| U-net Transformer [1]           | Segmentation | Sequential   | Fusing                        | Encoder       | Multi-head Cross-Attention     | U-Net                                 |
| UTNet [2]                         | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Multi-head Self-Attention     | U-Net                                 |
| CPT U-Net [3]                   | Segmentation | Parallel     | Fusing                        | Encoder Decoder | Pyramid Vision Transformer   | U-Net                                 |
| UNETR [4]                        | Segmentation | Sequential   | Feature Reshaping             | Encoder       | Vision Transformer            | U-Net                                 |
| Swin UNETR [5]                   | Segmentation | Sequential   | Feature Reshaping Fusing      | Encoder       | Swin Transformer              | U-Net                                 |
| COTRNet [6]                      | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Light Vision Transformer      | U-Net                                 |
| Cotr [7]                         | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Deformable Transformer-encoder | U-Net                               |
| Hybrid ViT and CNN [8]           | Segmentation | Sequential   | Fusing                        | Encoder Decoder | Vision Transformer           | U-Net                                 |
| TransBTS [9]                     | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Light Vision Transformer      | U-Net                                 |
| Trans U-Net [10]                  | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Vision Transformer           | U-Net |
| Bitr U-Net [11]                   | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Vision Transformer           | U-Net, CBAM |
| After U-Net [12]                  | Segmentation | Sequential   | Feature Reshaping             | Encoder       | Axial Fusion Transformer      | U-Net |
| WAU [13]                          | Segmentation | Sequential   | Feature Reshaping             | Decoder       | Window Attention              | Group Conv, Depthwise Separable CNN   |
| HCTN [14]                         | Segmentation | Parallel     | Feature Reshaping             | Encoder       | Vision Transformer            | U-Net|
| Hybrid CNN-Transformer Non-Contrast [15] | Segmentation | Parallel | Fusing                        | Encoder       | Hierarchical Transformer      | U-Net|
| D-TA U-net [16]                  | Segmentation | Parallel     | Fusing                              | Encoder       | Swin Transformer             | U-Net       |
| MLABHCTMI [17]| Segmentation | Parallel| Fusing|Encoder/Decoder | Transformer| U-Net|
| UCTNet [18]| Segmentation | Sequential| Feature Reshaping| Encoder/Decoder | Transformer| U-Net|
| HybridMT-ESTAN [19]| Classification/Segmentation| Parallel| Feature Reshaping Fusing| Encoder| Swin Transformer| ResNet|
| ChexViT [20]| Classification| Sequential   | Feature Reshaping Positional Encoding | Encoder    | Vision Transformer| CheXNet [49]|
| TECNN [21] | Classification | Parallel| Feature Reshaping Fusing| Encoder| Vision Transformer| DenseNet  |
| SLATER [22] | Classification | Sequential| Feature Reshaping Positional Encoding | Decoder   | Cross-Attention| Specialized CNN|
| 3D Transformer GAN [23] | Reconstruction| Sequential   | Feature Reshaping Positional Encoding | Encoder Decoder | Vision Transformer| Specialized CNN|
| T2Net [24] |Reconstruction| Sequential|| Encoder| Task-Attention| Specialized CNN |
| MIST-Net [25] | Reconstruction | Sequential| Feature Reshaping Fusing | Decoder| Soft-Attention Swin Transformer | Specialized CNN|
| Ultrasound ViT [30] | Regression | Sequential   | Feature Mapping                     | Encoder       | Bert                         | ResNetAE/DenseNet                  |
| DTN [25] |Regression| Sequential   | Feature Reshaping Fusing            | Encoder/Decoder | Dual Transformer            | Specialized CNN                    |
| ViT-V-Net [26] | Registration| Sequential   | Feature Reshaping Positional Encoding | Encoder    | Vision Transformer           | Specialized CNN |
| Transmorph [23] |Registration| Sequential   | Feature Reshaping                   | Encoder       | Swin Transformer             | U-Net                              |
| ResViT [29] | Image Synthesis                 | Sequential   | Feature Reshaping| Encoder       | Vision Transformer| Specialized CNN |
| TransCT [27]| Restoration| Parallel     | Feature Reshaping                   | Encoder Decoder | Vision Transformer         | Specialized CNN |
| Multi-View ViT [26]| Combining Views                 | Sequential   | Feature Reshaping                   | Encoder       | Cross View-Attention         | ResNet |
| AlignTransformer [52]| Report Generation| Sequential   | Feature Reshaping                   | Encoder       | Align Hierarchical-Attention | ResNet      |
| R2Gen [28]| Report Generation | Sequential   | Feature Reshaping                   | Encoder Decoder | Vision Transformer         | Pretrained (ResNet, VGG) |



### Benchmark Table
Benchmarking criteria definition. Inaccessibility of the models are marked as ’–’ which restrict to calculate the
benchmarking criteria.

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


### Comparative analysis of the existing hybrid architectures
It performed based on the criteria defined in Sec.2.2. Studies are grouped based on the targeted
applications. ‘Transf.’, ‘Util.’ refers to Transformer and Utility respectively.


|Model|Benchmarking rating|Target dimension|Parameter(M)|Inference time(GFLOPs)|Sample Size|Community adoption rate|Performance|
|-----|------------------|----------------|------------|---------------------|-----------|---------------------|------------|
|U-net Transformer|Opaque|High|-50|-|Public,single|91|80|
|UTNet|High|High|-50|-50|Public,multiple|166|80|
|CPT U-Net|Medium|High|-100|-150|Public,multiple|2.06|80|
|UNETR|High|High|-100|-50|Public,multiple|957|80|
|Swin UNETR|Low|High|-100|-150|Public,single|356.33|90|
|COTRNet|Opaque|High|-|-|Public,single|7|80|
|Cotr|Low|High|-50|-150|Public,single|189.33|80|
|Hybrid ViT and CNN|Opaque|High|-|-|Public,single|1.5|80|
|TransBTS|High|High|-50|-300|Public,multiple|9|80|
|Trans U-Net|Medium|High|-100|-1000|Public,multiple|1456|-70|
|Bitr U-Net|Low|High|-50|-150|Public,single|31.33|90|
|After U-Net|Opaque|High|-50|-|Public,single|76.5|80|
|WAU|High|High|-50|-50|Public,multiple|27.5|80|
|HCTN|Opaque|High|-|-|Public,single|3|80|
|Hybrid CNN-Transformer Non-Contrast|High|High|-50|-5|Public,multiple|10|80|
|D-NetNet|Medium|High|-100|-50|Public,single|6|80|
|MCAReTNet|High|High|-5|-5|Public,multiple|1|80|
|UCTNet|High|High|-100|-50|Public,multiple|6|80|
|Hybrid MCSPBSN|Opaque|High|-|-|Private,single|8|80|
|ChanViT|Opaque|Low|-|-|Public,single|1|80|
|TRCNet|Opaque|High|-50|-|Public,multiple|32|95|
|SEATER|High|High|-50|-150|Public,multiple|97.5|95|
|3D Transformer GAN|Opaque|High|-50|-|Private,single|54.67|95|
|T2Net|Low|High|-5|-100|Public,single|27.5|80|
|MSN-Net|Medium|High|-50|-300|Public,single|18|95|
|Ultrasound ViT|Medium|High|-800|-300|Public,single|21.33|80|
|DTN|Opaque|High|-|-|Private,single|21.33|80|
|ViViT-Net|Low|High|-50|-700|Private,single|65.33|80|
|Transmorph|Medium|High|-50|-1000|Public,multiple|166|80|
|RevViT|Medium|High|-100|-900|Public,multiple|173|80|
|TransCT|Medium|High|-50|-500|Public,single|54.67|90|
|Multi-View ViT|High|Low|-50|-10|Public,single|21.67|80|
|AlignTransformer|Opaque|Low|-|-|Public,single|45.33|-80(BLEU)|
|R2Gen|Medium|Low|-100|-50|Public,multiple|122.67|-50(BLEU)|


## Reference
1. U-net transformer: Self and cross attention for medical image segmentation
2. UTNet: a hybrid transformer architecture for edical image segmentation
3. Cross Pyramid Transformer makes U-net stronger in medical image segmentation
4. Unetr: Transformers for 3d medical image segmentation
5. Swin unetr: Swin transformers for semantic segmentation of brain tumors in mri images
6. Automated kidney tumor segmentation with convolution and transformer network
7. Cotr: Efficiently bridging cnn and transformer for 3d medical image segmentation
8. Hybrid Transformer and Convolution for Medical Image Segmentation
9. Transbts: Multimodal brain tumor segmentation using transformer
10. TransUNet: Rethinking the U-Net architecture design for medical image segmentation through the lens of transformers
11. Bitr-unet: a cnn-transformer combined network for mri brain tumor segmentation
12. After-unet: Axial fusion transformer unet for medical image segmentation
13. More than encoder: Introducing transformer decoder to upsample
14. Hybrid CNNtransformer network for interactive learning of challenging musculoskeletal images
15. Hybrid CNN-Transformer Network With Circular Feature Interaction for Acute Ischemic Stroke Lesion Segmentation on Non-Contrast CT Scans
16. D-TrAttUnet: Toward hybrid CNN-transformer architecture for generic and subtle segmentation in medical images
17. Multi-level Augmentation Boosts Hybrid CNNTransformer Model for Semi-supervised Cardiac MRI Segmentation
18. UCTNet: Uncertaintyguided CNN-Transformer hybrid networks for medical image segmentation
19. Breast Ultrasound Tumor Classification Using a Hybrid Multitask CNN-Transformer Network
20. CheXViT: CheXNet and Vision Transformer to Multi-Label Chest X-Ray Image Classification
21. Combining the Transformer and Convolution for Effective Brain Tumor Classification Using MRI Images
22. Unsupervised MRI reconstruction via zero-shot learned adversarial transformers
23. 3D transformer-GAN for high-quality PET reconstruction
24. Task transformer network for joint MRI reconstruction and super-resolution
25. Ultrasound Video Transformers for Cardiac Ejection Fraction Estimation,”
26. Learning dual transformer network for diffeomorphic registration
27. Vit-v-net: Vision transformer for unsupervised volumetric medical image registration
28. Transmorph: Transformer for unsupervised medical image registration
29. ResViT: Residual vision transformers for multimodal medical image synthesis
30. TransCT: dual-path transformer for low dose computed tomography
31. Multi-view analysis of unregistered medical images using cross-view transformers
32. Aligntransformer: Hierarchical alignment of visual regions and disease tags for medical report generation
33. Generating radiology reports via memory-driven transformer
