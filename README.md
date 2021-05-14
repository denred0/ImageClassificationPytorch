# Image Classification PyTorch

Use pretrained models to train your data.





## :closed_book: Table of content
- [What's New](#whats-new)
- [Introduction](#introduction)
- [Models](#models)
- [Features](#features)
- [Results](#results)
- [Getting Started (Documentation)](#getting-started-documentation)
- [Train, Validation, Inference Scripts](#train-validation-inference-scripts)
- [Awesome PyTorch Resources](#awesome-pytorch-resources)
- [Licenses](#licenses)
- [Citing](#citing)

## :clipboard: What's New <a name="whats-new"></a>


## :computer: Installation

```python
pip install image-classification-pytorch
```

## ✨ Quick start

## :telescope: Inference

## :chart_with_downwards_trend: Models

## :file_folder: Data preparation

## 🛡️ License




```python
import image_classification_pytorch as icp
```
```python
# Images of each class in its own folder with the class name. 
# Examples of folders: homer_simpson, bart_simpson etc. 
from google.colab import drive
drive.mount('/content/gdrive')
!unzip -q /content/gdrive/My\ Drive/datasets/image_classification_pytorch/data_simpsons.zip -d train
```
```python
# add model
tf_efficientnet_b4_ns = {'model_type': 'tf_efficientnet_b4_ns', 'im_size': 380, 'im_size_test': 380, 'batch_size': 8, 'mean': [0.485, 0.456, 0.406], 'std': [0.229, 0.224, 0.225]}
models = [tf_efficientnet_b4_ns]
```
```python
# create trainer
trainer = ICPTrainer(models=models, data_dir='data_simpsons')
# start training
trainer.fit_test()
```

## Colab Quick start
[image_classification_pytorch_get_started.ipynb](https://colab.research.google.com/drive/1M7oJDizCOrFTDJz0CaDy-ClvDMUvmlnv?usp=sharing)
