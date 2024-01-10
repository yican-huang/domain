# domain
# 域适应论文调研
## Prior-based Domain Adaptive Object Detection for Hazy and Rainy Conditions
ECCV
### 摘要
雾霾和下雨等恶劣天气条件会破坏捕获图像的质量，导致在干净图像上训练的检测网络在这些图像上表现不佳。为了解决这个问题，我们提出了一种无监督的基于先验的域对抗对象检测框架，用于使检测器适应雾霾和多雨的条件。特别是，我们使用通过图像形成原理获得的特定于天气的先验知识来定义一种新颖的先验对抗性损失。用于训练适应过程的先验对抗性损失旨在减少特征中特定于天气的信息，从而减轻天气对检测性能的影响。此外，我们在对象检测管道中引入了一组残余特征恢复块，以消除特征空间的扭曲，从而实现进一步的改进。对雨天和雾霾条件下的各种数据集（Foggy-Cityscapes、RainyCityscapes、RTTS 和 UFDD）进行的评估证明了所提出方法的有效性。
### 网络
[![pF9GeBD.md.png](https://s11.ax1x.com/2024/01/10/pF9GeBD.md.png)](https://imgse.com/i/pF9GeBD)

## One-Shot Unsupervised Domain Adaptation With Personalized Diffusion Models
CVPR
## 摘要
这篇文章介绍了一种新的方法，用于解决单样本无监督域适应（OSUDA）的问题，即从一个有标签的源域适应到一个只有一个无标签数据的目标域。该方法的主要思想是利用文本到图像扩散模型（DM），根据目标域的外观和源域的语义概念，生成一个合成的目标数据集，然后用一个通用的UDA方法来训练一个分割模型。该方法分为三个阶段：
个性化阶段：在这个阶段，作者使用单个目标图像的多个裁剪来微调一个预训练的文本到图像DM模型，使其能够生成目标域的风格的图像。
数据生成阶段：在这个阶段，作者利用微调后的DM模型，通过给定一些类别名称作为文本提示，来生成一个包含多样化和真实性的目标域图像的数据集。
自适应分割阶段：在这个阶段，作者将标记的源域数据和生成的无标记的目标域数据结合起来，使用一个UDA方法（如DAFormer或HRDA）来训练一个分割模型。
## 网络图
[![pF9GuAH.md.png](https://s11.ax1x.com/2024/01/10/pF9GuAH.md.png)](https://imgse.com/i/pF9GuAH)

## A domain adaptation YOLOv5 model for industrial defect inspection
Measurement
### 网络图
[![pF9G13t.md.png](https://s11.ax1x.com/2024/01/10/pF9G13t.md.png)](https://imgse.com/i/pF9G13t)
[![pF9GYDS.md.png](https://s11.ax1x.com/2024/01/10/pF9GYDS.md.png)](https://imgse.com/i/pF9GYDS)

其实网络创新方面是几乎没有的，用的就是yolo作为主干网络，最大平均差异 (MMD) [38,39] 在 DAYOLOv5 中应用，以最小化源域和目标域之间的距离。但是贵在实验做得比较丰富。还是有些启发的。

[![pF9GaNj.md.png](https://s11.ax1x.com/2024/01/10/pF9GaNj.md.png)](https://imgse.com/i/pF9GaNj)

这篇文章做的是钢材的检测，采用的不是UDA的思想，他要做的是在少量的带标注目标域的数据的情况下，也能在目标域下有较好的检测效果。

## Domain Adaptive Object Detection for Autonomous Driving under Foggy Weather
CCFB：Winter Conference on Applications of Computer Vision
### 摘要
大多数自动驾驶的目标检测方法通常假设训练数据和测试数据之间具有一致的特征分布，但当天气差异很大时，情况并非总是如此。由于域间隙，在晴朗天气下训练的目标检测模型在雾天可能不够有效。本文提出了一种新颖的域自适应目标检测框架，用于雾天自动驾驶。我们的方法利用图像级和对象级自适应来减少图像风格和对象外观的域差异。为了进一步增强模型在具有挑战性的样本下的能力，我们还提出了一个新的对抗性梯度反转层，对困难样本进行对抗性挖掘以及领域适应。此外，我们建议通过数据增强生成辅助域，以实施新的域级度量正则化。公共基准的实验结果表明了该方法的有效性和准确性。
### 网络结构图
[![pF9G0Cn.md.png](https://s11.ax1x.com/2024/01/10/pF9G0Cn.md.png)](https://imgse.com/i/pF9G0Cn)
