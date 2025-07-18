# Ancient-Coin-Classification
This repository contains Jupyter notebooks for a project on multiclass classification of Roman Republican coin images using Vision Transformer (ViT-B/16) and InceptionV3 models, implemented using TensorFlow and PyTorch.  
Ancient coin classification is a challenging task due to the variations in design, wear, and limited labelled data. This study explores the use of Convolutional Neural Networks (CNNs) and Vision Transformers (ViTs) for classifying Roman Republican coins using RRC-60 dataset. In this project, an InceptionV3-based model was improved by fine-tuning and integrating a Squeeze-and-Excitation Network (SENet), which applies a channel-wise attention mechanism to enhance feature extraction. The final InceptionV3-based model achieved 96.58% accuracy. The ViT model, leveraging self-attention mechanisms to capture global relationships in images, reached 99.10% accuracy when fully fine-tuned. Both models benefit from pretraining on ImageNet, which provides a strong feature extraction foundation before fine-tuning on the ancient coin dataset.  
A comparative analysis showed that the ViT model outperforms the InceptionV3-based model in both accuracy and inference speed, but it requires more computational resources. Experiments under low-data conditions revealed that the ViT model maintains higher classification accuracy and robustness even when trained on a limited number of samples.  
Model interpretability was analysed using Grad-CAM for the InceptionV3-based model and attention maps for the ViT model. Results highlight the effectiveness of ViTs in ancient coin classification, especially with limited data, and underscore the potential of attention mechanisms and transfer learning for this classification task.

# Repository Structure
The repository is organized as follows:

[InceptionV3.ipynb](https://github.com/AliSafaeii/Ancient-Coin-Classification/blob/main/InceptionV3.ipynb): Training and fine-tuning the InceptionV3-based models using TensorFlow.  
[ViT_Baseline.ipynb](https://github.com/AliSafaeii/Ancient-Coin-Classification/blob/main/ViT_Baseline.ipynb): Providing a baseline ViT-B/16 model using PyTorch.  
[ViT_Partial_Fine_Tuning.ipynb](https://github.com/AliSafaeii/Ancient-Coin-Classification/blob/main/ViT_Partial_Fine_Tuning.ipynb): Partially fine-tuninig a ViT-B/16 model using PyTorch.  
[ViT_Full_Fine_Tuning_80Percent.ipynb](https://github.com/AliSafaeii/Ancient-Coin-Classification/blob/main/ViT_Full_Fine_Tuning_80Percent.ipynb): Fully fine-tuning a a ViT-B/16 model using the main training set (80% of the whole dataset).  
[ViT_Full_Fine_Tuning_20Percent.ipynb](https://github.com/AliSafaeii/Ancient-Coin-Classification/blob/main/ViT_Full_Fine_Tuning_20Percent.ipynb): Fully fine-tuning a a ViT-B/16 model using 25% of the main training set (20% of the whole dataset).  
[ViT_Full_Fine_Tuning_10Percent.ipynb](https://github.com/AliSafaeii/Ancient-Coin-Classification/blob/main/ViT_Full_Fine_Tuning_10Percent.ipynb): Fully fine-tuning a a ViT-B/16 model using 12.5% of the main training set (10% of the whole dataset).  
[ViT_Full_Fine_Tuning_5Percent.ipynb](https://github.com/AliSafaeii/Ancient-Coin-Classification/blob/main/ViT_Full_Fine_Tuning_5Percent.ipynb): Fully fine-tuning a a ViT-B/16 model using 6.25% of the main training set (5% of the whole dataset).  
[GradCAM.ipynb](https://github.com/AliSafaeii/Ancient-Coin-Classification/blob/main/GradCAM.ipynb): Grad-CAM visulaiztion for the InceptionV3-based model.  
[Attention_Map.ipynb](https://github.com/AliSafaeii/Ancient-Coin-Classification/blob/main/Attention_Map.ipynb): Attention map visualization for the ViT-B/16 model.

# Dataset
The RRC-60 dataset consists of 12000 Roman Republican coin images (6000 images for each side of the coin) accross 60 classes. Only the reverse side of the coins were used in this project.  
You can download the dataset from [here](https://drive.google.com/file/d/1aG90R_09rUe1S0qXrs3cmFnLMm9jywMU/view?usp=sharing).  
You can also find some information about the dataset from [here](https://github.com/siinem/RRC-60).  
If you are using the RRC-60 dataset, please cite [1] from the reference list below.

References:  
[1] Aslan, S., Vascon, S., & Pelillo, M. (2019). Two sides of the same coin: Improved ancient coin classification using Graph Transduction Games. Pattern Recognition Letters, 131, 158–165. [Link](https://doi.org/10.1016/j.patrec.2019.12.007)  

  
[2] Zambanini, S., & Kampel, M. (2013). Coarse-to-fine correspondence search for classifying ancient coins. In J. I. Park & J. Kim (Eds.), Computer Vision – ACCV 2012 Workshops. ACCV 2012. Lecture Notes in Computer Science (Vol. 7729) (pp. 25–36). Springer. [Link](https://doi.org/10.1007/978-3-642-37484-5_3)  
