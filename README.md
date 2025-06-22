# MOSD-UNet
Research on Scratch Defect Segmentation of Steel Surfaces Using MOSD-UNet Within a Semi-Supervised Self-Training Framework

# 简介
 a lightweight segmentation model for detecting steel surface scratch defects, termed MOSD-UNet (Metal Object Scratch Detection U-Net)
 
# 环境依赖
Deep Learning Toolkit	                                PyTorch 2.7.0+cu118

Computer Vision Toolkit                                 OpenCV-Python 4.11.0.86

python                                         3.10.13

pandas                                         2.2.3

albumentations                                 0.5.0

# 目录结构描述

├── input                // The dataset

│   ├── neu_A           // Labeled image dataset

│   │   ├── train  

│   │   │   ├── images

│   │   │   │   ├── "00xxxx.jpg"

│   │   │   ├── masks

│   │   │   │   ├── 0

│   │   │   │   │   ├── "00xxxx.png"

│   │   ├── val  

│   │   │   ├── images

│   │   │   │   ├── "00xxxx.jpg"

│   │   │   ├── masks

│   │   │   │   ├── 0

│   │   │   │   │   ├── "00xxxx.png"



│   ├── neu           // Image dataset without labels for model prediction

│   │   ├── images

│   │   │   ├── "00xxxx.jpg"


│   │   ├── masks

│   │   │   ├── 0

│   │   │   │   ├── "00xxxx.png"


│   ├── neu_mix           // Labeled image dataset and Image dataset without labels for model prediction are mixed for training

│   │   ├── train  

│   │   │   ├── images

│   │   │   │   ├── "00xxxx.jpg"

│   │   │   ├── masks

│   │   │   │   ├── 0

│   │   │   │   │   ├── "00xxxx.png"

│   │   ├── val  

│   │   │   ├── images

│   │   │   │   ├── "00xxxx.jpg"

│   │   │   ├── masks

│   │   │   │   ├── 0

│   │   │   │   │   ├── "00xxxx.png"



├── models                          // The model

│   ├── neu_xxx_UNet_xxx_wods

│   │   ├── bestmodel.pth          //model best {weights}.pt

│   │   ├── config.yml

│   │   ├── lastmodel.pth

│   │   ├── log.csv

├── outputs                         // The model

│   ├── neu_xxx_UNet_xxx_wods

│   │   ├── 0          

│   │   │   ├── "00xxxx.png"


├── archs.py            // The MOSD-UNet model written in python

├── losses.py           // The loss function written in python

├── metrics.py          // The iou_score/dice_coef/precision_recall_f1  written in python

├── train.py            // The train written in python

├── utils.py            // some {utilities}.py

├── val.py              // Verify the metrics of the current model

└── ReadMe.md           // Introduction
