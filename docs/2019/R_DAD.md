## Object Detection based on Region Decomposition and Assembly (AAAI 2019) [\[arxiv\]](https://arxiv.org/abs/1901.08225)

论文认为二阶段网络中存在的受遮挡的`proposal`会影响模型的性能，因此提出`R-DAD`模型，即对`RPN`输出的`proposal`进行区域分解，然后再区域整合。

<p align="center">
  <img src="../../imgs/r-dad.jpg" alt="R-DAD framework" width="850px" />
</p>

### 论文创新点

1. 提出`multi-scale RPN`，即对`RPN`输出的`proposal`的长和宽乘以一系列系数，得到一系列以原始`proposal`中心进行缩放的`proposal`；
2. 把每个`proposal`按照水平或垂直平分线分成四个区域；
3. 对每个区域使用`region assembly block (RAB)`进行融合。

### 论文不足

1. 论文并没有解析`proposal`如此划分的原因，同时也没有对比其它划分方法；
2. 论文中的`multi-scale region proposal (MRP)`网络并非原创；
3. 网络的复杂度比`baseline`大。
