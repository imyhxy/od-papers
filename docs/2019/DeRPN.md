## DeRPN: Taking a further step toward more general object detection (AAAI 2019) [\[arxiv\]](https://arxiv.org/abs/1811.06700)

目前的二阶段网络大多采用`RPN`作为候选框生成网络，但是`RPN`的召回率很大程度上依靠`anchor boxes`的设定，不同的数据集对`anchor boxes`的要求不一致，这导致不改变超参数的情况下`RPN`缺乏泛化能力，本文提出一种新的`anchor`形式：`anchor string`。通过分别预测边界框的`width`和`height`，DeRPN可以使用更少的参数预测更多`aspect ratio`的框。

### 论文创新点

1. 把`anchor boxes`替换为`anchor string`，使用更少的参数预测更加多样化的框，`DeRPN`的`recall`比`RPN`有了很大的提升；
2. 提示了`scale sensitive`的`loss function`，分别计算不同尺度物体的误差，这样有效地缓解了不同尺度物体统一归一化时**占优尺度**对**弱势尺度**的削弱。
