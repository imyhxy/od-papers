## LSTD: A Low-Shot Transfer Detector for Object Detection (AAAI 2019) [\[arxiv\]](https://arxiv.org/abs/1803.01529)

目标检测网络通常需要大量的训练样本，当训练样本严重不足时我们需要使用`weakly-supervised`或者`semi-supervised`的方式进行训练，但是即使使用了前面两种方法，对于`low-shot`的情况，仍然不能达到令人满意的效果。
在本文中，作者通过提出新的**知识迁移**方法，使`target model`能更好地利用`source model`的知识。

<p align="center">
  <img src="../../imgs/lstd_1.jpg" alt="lstd_1" width="700px" />
</p>

<p align="center">
  <img src="../../imgs/lstd_2.jpg" alt="lstd_2" width="700px" />
</p>

### 论文创新点：

1. 提出`LSTD`模型：`LSTD`模型结合了`SSD`和`Faster RCNN`的特点，即预测没有类别属性的边界框和使用`coarse-to-fine`的分类方方式；
2. 提出了`Background Depression`和`Transfer Knowledge`两种`Regularization`方式，使得`target model`能在`low-shot`情况下有更好的效果。

### 论文不足：

论文中没有提及复杂度的分析，用`LSTD`和`SSD`，`Faster RCNN`比较不太公平。
