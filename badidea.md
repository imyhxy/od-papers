## Improve Object Detection by Data Enhancement based on Generative Adversarial Nets [\[arxiv\]](https://arxiv.org/abs/1903.01716)

论文创新点：
1. 使用GAN分割出前、背景，然后对物体做数据增强
1. GAN：用ResNet 101作为生成器（特征提取网络），生成对**前景**和**背景**作分割的二值mask，用Ground Truth mask和生成的mask与原图相乘，分别得到真实样本和虚假样本，使用Perceptual Loss训练一个辨别器
1. 对图片中mask为1的部分使用数据增强，然后将增强后的图片输入到DSSD中，DSSD和GAN的特征提取网络使用相同的参数

论文缺点：
1. 没有太多novelty
1. 提升并不大（78.6% -> 78.7)
