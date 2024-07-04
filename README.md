# AddressCLIP
Official implementation and datasets for AddressCLIP: Empowering Vision-Language Models for City-wide Image Address Localization, accepted at ECCV 2024.

![image](https://github.com/xsx1001/AddressCLIP/assets/59325025/0bd81407-f8b8-4dcf-8901-5ad966579add#pic_center)

## Overview
**Abstract**. In this study, we introduce a new problem raised by social media and photojournalism, named Image Address Localization (IAL), which aims to predict the readable textual address where an image was taken. Existing two-stage approaches involve predicting geographical coordinates and converting them into human-readable addresses, which can lead to ambiguity and be resource-intensive. In contrast, we propose an end-to-end framework named AddressCLIP to solve the problem with more semantics, consisting of two key ingredients: i) image-text alignment to align images with addresses and scene captions by contrastive learning, and ii) imagegeography matching to constrain image features with the spatial distance in terms of manifold learning. Additionally, we have built three datasets from Pittsburgh and San Francisco on different scales specifically for the IAL problem. Experiments demonstrate that our approach achieves compelling performance on the proposed datasets and outperforms representative transfer learning methods fof vision-language models. Furthermore, extensive ablations and visualizations exhibit the effectiveness of the proposed method.

## Requirements
```
python == 3.8
clip == 1.0
torch == 2.1.1
torchvision == 0.16.1
matplotlib
scikit-image
opencv
```

## Image Address Localization Datasets

### Annotations
Download the annotations and splits of IAL-datasets used in the paper from Baidu Cloud [link](https://pan.baidu.com/s/1dLS04_aoreEYFINOXgbEQg?pwd=rnjk) or Google Drive [link](https://drive.google.com/file/d/1Lw-slVr0oT-MFYsLF8NJUP6jAH11URs2/view?usp=share_link).

Feel free to use the addresses and captions in it!

### Pitts-IAL
#### Download Pittsburgh-250k
Download the original Pittsburgh-250k dataset from [here](https://data.ciirc.cvut.cz/public/projects/2015netVLAD/Pittsburgh250k/)

#### Re-orginization
Extract the `.zip` files and put them all into `./datasets/Pitts-IAL/` folder.

### SF-IAL-Base & SF-IAL-Large
#### Download CosPlace
Follow the instruction from the [CosPlace](https://github.com/gmberton/CosPlace) to obtain the original SF-XL dataset.

We only used the images in the `/processed` folder. Download it and put it into `./datasets/processed/` folder. 

## Training
Coming soon ...

## Evaluation
Coming soon ...

## Citation
If this project is helpful for you, please cite our paper:
```
@inproceedings{Xu_2024_ECCV,
title={AddressCLIP: Empowering Vision-Language Models for City-wide Image Address Localization},
author={Xu, Shixiong and Zhang, Chenghao and Fan, Lubin and Meng, Gaofeng and Xiang, Shiming and Ye, Jieping},
booktitle={European Conference on Computer Vision (ECCV)},
year={2024}}
```

## Acknowledgements
This repository makes liberal use of code from GwcNet and beyond-image-to-depth.
