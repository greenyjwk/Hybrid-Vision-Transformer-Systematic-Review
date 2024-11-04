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
| Trans U-Net [22]                  | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Vision Transformer           | U-Net                                 |
| Bitr U-Net [40]                   | Segmentation | Sequential   | Feature Reshaping Positional Encoding | Encoder | Vision Transformer           | U-Net, CBAM                           |
| After U-Net [41]                  | Segmentation | Sequential   | Feature Reshaping             | Encoder       | Axial Fusion Transformer      | U-Net                                 |
| WAU [42]                          | Segmentation | Sequential   | Feature Reshaping             | Decoder       | Window Attention              | Group Conv, Depthwise Separable CNN   |
| HCTN [43]                         | Segmentation | Parallel     | Feature Reshaping             | Encoder       | Vision Transformer            | U-Net                                 |
| Hybrid CNN-Transformer Non-Contrast [44] | Segmentation | Parallel | Fusing                        | Encoder       | Hierarchical Transformer      | U-Net                                 |
| D-TA U-net [45]                  | Segmentation | Parallel     | Fusing                              | Encoder       | Swin Transformer             | U-Net       |
| MLABHCTMI [46]                   | Segmentation | Parallel     | Fusing                              | Encoder/Decoder | Transformer               | U-Net       |
| UCTNet [47]                      | Segmentation | Sequential   | Feature Reshaping                   | Encoder/Decoder | Transformer               | U-Net                              |
| HybridMT-ESTAN [48]              | Classification/Segmentation     | Parallel     | Feature Reshaping Fusing            | Encoder       | Swin Transformer             | ResNet                             |
| ChexViT [17]                     | Classification                  | Sequential   | Feature Reshaping Positional Encoding | Encoder    | Vision Transformer           | CheXNet [49]                       |
| TECNN [19]                       | Classification                  | Parallel     | Feature Reshaping Fusing            | Encoder       | Vision Transformer           | DenseNet                           |
| SLATER [50]                      |                                 | Sequential   | Feature Reshaping Positional Encoding | Decoder   | Cross-Attention              | Specialized CNN                    |
| 3D Transformer GAN [18]          | Reconstruction                  | Sequential   | Feature Reshaping Positional Encoding | Encoder Decoder | Vision Transformer     | Specialized CNN                    |
| T2Net [31]                       |                                 | Sequential   |                                      | Encoder       | Task-Attention               | Specialized CNN                    |
| MIST-Net [50]                    |                                 | Sequential   | Feature Reshaping Fusing            | Decoder       | Soft-Attention Swin Transformer | Specialized CNN                |
| Ultrasound ViT [30]              | Regression                      | Sequential   | Feature Mapping                     | Encoder       | Bert                         | ResNetAE/DenseNet                  |
| DTN [25]                         |                                 | Sequential   | Feature Reshaping Fusing            | Encoder/Decoder | Dual Transformer            | Specialized CNN                    |
| ViT-V-Net [51]                   | Registration                    | Sequential   | Feature Reshaping Positional Encoding | Encoder    | Vision Transformer           | Specialized CNN                    |
| Transmorph [23]                  |                                 | Sequential   | Feature Reshaping                   | Encoder       | Swin Transformer             | U-Net                              |
| ResViT [29]                      | Image Synthesis                 | Sequential   | Feature Reshaping                   | Encoder       | Vision Transformer           | Specialized CNN                    |
| TransCT [27]                     | Restoration                     | Parallel     | Feature Reshaping                   | Encoder Decoder | Vision Transformer         | Specialized CNN                    |
| Multi-View ViT [26]              | Combining Views                 | Sequential   | Feature Reshaping                   | Encoder       | Cross View-Attention         | ResNet                             |
| AlignTransformer [52]            | Report Generation               | Sequential   | Feature Reshaping                   | Encoder       | Align Hierarchical-Attention | ResNet                             |
| R2Gen [28]                       |                                 | Sequential   | Feature Reshaping                   | Encoder Decoder | Vision Transformer         | Pretrained (ResNet, VGG)           |





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
