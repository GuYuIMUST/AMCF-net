# AMCF-Net
## Introduction
**AMCF-Net: A Novel Adaptive Multi-Channel Fusion Network for Computer-Aided Diagnosis of Lung Nodules in Chest Computed Tomography** 


## Results

### AMCF-Net
###Comparison with the state-of-the-art methods:
        | model      | Accuracy| F1-score| G-mean  | SPE     |   SEN   | Params  | FLOPs   |  
        |------------|---------|---------| --------|---------|---------|---------|---------|
        | MMEL-net   | 90      | 88.97   | 88.56   | 93.9    | 83.7    |28       | --      | 
        | TransUnet  | 84.62   | 80.38   | 81.29   | 93.17   | 70.92   |--       | --      | 
        | VGG16-T    | 86.58   | 82.62   | 79.03   | 72.63   | 86      |--       | --      | 
        | CNN        | 89.85   | 89      | --      | --      | 90      |--       | --      | 
        | Res-U-net  | 87.3    | 87.1    | 87.3    | 94.8    | 80.4    |--       | --      |  
        | SSA-net    | 89.13   | 84.85   | 86.2    | 98.18   | 75.68   |--       | --      | 
        | HSCNN      | 84      | 78.21   | 78.89   | 88.9    | 70      |--       | --      | 
        | DGMM-net   | 88      | 91      | --      | --      | 70      |--       | --      | 
        | CNN        | 84.8    | 84.64   | 84.82   | 90.64   | 79.5    |--       | --      | 
        | MRC-DNN    | 90      | 87.54   | 87.72   | 95      | 81      |--       | --      | 
        | DeepLung   | 90.24   | 90.45   | 90.48   | 88.94   | 92.04   | 678.69  | --      |
        | NASLung    | 90.77   | 89.29   | 90.08   | 95.04   | 85.37   | 16.84   | --      |
        | deep CNN   | 95.40   | 95.24   | 93.93   | 83.17   | 94.69   | --      | --      | 
        | AMCF(ours) | 90.22   | 86.57   | 87.72   | 98.19   | 86.49   | 5.01    | 107.59  | 
        
        
 ###Overall Network Ablation Study:  
        | Base | ADSE | MCFM   | H-loss | Accuracy| F1-score| G-mean  |   SPE   |   SEN   | Params |  FLOPs   |  
        |  √  |      |        |        |  86.96  |  81.82  | 83.86   |  96.36  |  72.92  |  6.85  |  126.17  |
        |  √  | √   |        |        |  88.04  |  84.46  | 83.21   |  92.73  |  78.38  |  6.86  |  143.17  |
        |  √  |      | √     |        |  86.96  |  82.86  | 85.25   |  94.55  |  78.38  |  4.73  |  90.59   |
        |  √  |      |        |    √  |  86.96  |  83.33  | 85.85   |  87.27  |  86.49  |  6.85  |  126.17  |
        |  √  | √   | √     |        |  89.13  |  84.85  | 86.2    |  96.36  |  78.38  |  5.01  |  107.59  |  
        |  √  | √   |        |    √  |  89.13  |  85.71  | 87.55   |  94.55  |  81.01  |  6.86  |  143.17  |
        |  √  |      | √     |    √  |  89.13  |  85.29  | 86.91   |  96.36  |  87.38  |  4.73  |  90.59   |
        |  √  | √   | √     |    √  |  90.22  |  86.57  | 87.72   |  98.19  |  86.49  |  5.01  |  107.59  |
       

## Usage
To run our code, you only need one GeForce RTX 4090(24G memory).

#### Preprocessing
You need to download the LUNA16 dataset by yourself and adjust the corresponding paths.

#### Train and Eval
main.py

#### Test
test_wn.py

To ensure the code can run, we provide versions of some libraries.

- python-3.7.13
- numpy-1.21.5
- pytorch-1.21.1
- pandas-1.3.5
- opencv-python-4.8.1

## Acknowledgement 

If there are any missing citations, please contact us. It is an unintentional omission, and we will add the citations accordingly.

 **This code is based on the implementation of  [NAS-Lung](https://github.com/fei-hdu/NAS-Lung)，[DeepLung](https://github.com/uci-cbcl/DeepLung), [LayerCAM](https://github.com/PengtaoJiang/LayerCAM-jittor) .**

## Selected References

If there are any missing citations, please contact us. It is an unintentional omission, and we will add the citations accordingly.

- Jiang, H., Gao, F., Xu, X., Huang, F., and Zhu, S.J.N., 'Attentive and Ensemble 3d Dual Path Networks for Pulmonary Nodules Classification', 2020, 398, pp. 422-430.
- Jiang, H., Shen, F., Gao, F., and Han, W.J.P.R., 'Learning Efficient, Explainable and Discriminative Representations for Pulmonary Nodules Classification', Pattern Recognit, 2021, 113, p. 107825.
- Jiang, P.T., Zhang, C.B., Hou, Q.B., Cheng, M.M., and Wei, Y.C., 'Layercam: Exploring Hierarchical Class Activation Maps for Localization', Ieee Transactions on Image Processing, 2021, 30, pp. 5875-5888.
