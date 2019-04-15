## TensorMask: A Foundation for Dense Object Segmentation [\[arxiv\]](https://arxiv.org/abs/1903.12174)

`sliding-window`的方法在目标检测中使用得很多，并且效果也不错，而在`instance segmentation`中却缺少`sliding-window`这一方法，本文的主要动机就是为了填补这一空缺。

<p align="center">
  <img src="../../imgs/tensormask.jpg" alt="natural_vs_aligned" width=600px/>
  <br />
  Fig. Natural representation vs Aligned representation.
</p>

### 论文创新点

1. 使用结构化的`4D tensor`来表示`mask`：`(V, U, H, W)`；
2. 定义了`4D tensor mask`的`natural representation`和`aligned representation`，并且给出了两者的变换公式；
3. 定义了在`4D tensor`上运算的`up_align2nat`操作，即对`(V, U)`进行上抽样；
4. 定义了`tensor bipyramid`的特征表示方法，以及定义了`swap_align2nat`操作。

### 论文不足

1. 因为要对每个`sliding-window`输出一个`mask`，因此计算量比`Mask R-CNN`大；
2. 检测效果比`Mask R-CNN`差一点；
