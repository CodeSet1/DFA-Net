# DFA-Net: An Efficient Diffusion With Directional Frequency Feature Augmentation for Low-Light Image Enhancement
This is the official code for **DFA-Net: An efficient diffusion with frequency directional feature augmentation for low-light image enhancement**.

## Pipeline
![](./Figures/pipeline.png)

## Abstract
Existing diffusion-based low-light image enhancement (LLIE) methods have achieved remarkable restoration quality at the cost of substantial computational complexity, limiting their practical deployment. To address this challenge, we propose an efficient Diffusion-based Frequency Augmentation Network (DFA-Net), which exploits the compact representation of image structures in the frequency domain for efficient restoration. Our key insight reveals that directional frequency features are pivotal for accurate texture restoration in LLIE. Capitalizing on this, we propose a novel Mamba-based Directional Feature Augmentation (MDFA) module that efficiently enhances frequency-domain features while significantly reducing both computational complexity and parameter count. Subsequently, a frequency diffusion refinement is proposed to suppress amplified noise while preserving fine-grained details. Unlike existing diffusion-based solutions, we suggest dynamically balancing color restoration and artifact suppression through an adaptive interaction between high- and low-frequency components, \ie, the adaptive cross-frequency guidance. Extensive experiments demonstrate that DFA-Net achieves state-of-the-art performance on public benchmarks with a minimal parameter footprint—utilizing only 9.25\% of the parameters and 20.71\% fewer computational costs compared to prevailing diffusion-based LLIE methods. The practical utility of DFA-Net is further validated through a low-light face detection application.

### 1. Download the project.
Please run the following command to ensure that you deploy our project locally.

```python
git clone https://github.com/YhuoyuH/RetinexMamba.git
```

### Dependencies
```
pip install -r requirements.txt
````

## Datasets
The LOLv1 datasets can be downloaded from this [link](https://drive.google.com/file/d/1L-kqSQyrmMueBh_ziWoPFhfsAh50h20H/view). 
The LOLv2 datasets can be downloaded from this [link](https://drive.google.com/file/d/1Ou9EljYZW8o5dbDCf9R34FS8Pd8kEp2U/view).
Please refer to [[Project Page of RetinexNet.]](https://daooshee.github.io/BMVC2018website/)

## Pretrained Weights
The pretrained model, `DFA-Net.pth`, which can reproduce the quantitative results in the paper, is in the `weights` directory. We will organize and upload it as soon as possible.


## How to train?
You need to modify ```datasets/dataset.py``` slightly for your environment, and then
```
python train.py  
```

## How to test?
```
python evaluate.py
```
## Visual comparison
![](./Figures/comparison.png)
