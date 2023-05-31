# hw2

## Task1 的代码说明
文件train.ipynb包括ResNet34的定义，cutmix, cutout, mixup三种数据增强的函数，以及网络的训练和测试部分。实验中使用到的CIFAR-100数据集的获取也在代码中，运行时会下载到根目录中。

文件plot_three_pic.ipynb是用于绘制第一问中“三张训练样本分别经过 cutmix, cutout, mixup 后进行可视化”的9张图。

要想运行这部分代码，可以下载后放到colab或者Kaggle这些有免费GPU使用的平台上，依次运行相应的单元格就可。

## Task2 的代码说明
本部分包括两个模型 FCOS 和 Faster R-CNN。分别在两个文件夹中。

### Faster R-CNN
在trainer.py中训练faster RCNN，需要在utils.config.py文件里voc_data_dir = 后加上自己的VOC文件路径。faster-rcnn-visualization.ipynb对训练结果可视化。

### FCOS
基于pytorch的FCOS复现，实现对PASCAL VOC数据集的训练和预测

#### 使用方法

启动Visdom
```shell
python -m visdom.server
```
开始训练
```shell
python train.py
```

训练时可访问[Visdom](http://localhost:8097)查看训练进度
