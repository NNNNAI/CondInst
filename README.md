# CondInst
This repository is an unofficial pytorch implementation of [Conditional Convolutions for Instance Segmentation](https://arxiv.org/abs/2003.05664). The model with ResNet-101 backbone achieves 37.1 mAP on COCO val2017 set.

## Install
The code is based on [detectron2](https://github.com/facebookresearch/detectron2). Please check [Install.md](https://github.com/facebookresearch/detectron2/blob/master/INSTALL.md) for installation instructions.

## Training 
Follows the same way as detectron2.

Single GPU:
```
python train_net.py --config-file configs/CondInst/hrnet_w32_condpose.yaml
```
Multi GPU(for example 8):
```
python train_net.py --num-gpus 8 --config-file configs/CondInst/MS_R_101_3x.yaml
```
Please adjust the IMS_PER_BATCH in the config file according to the GPU memory.

