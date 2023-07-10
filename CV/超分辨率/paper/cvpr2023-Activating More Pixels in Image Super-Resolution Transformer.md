# Activating More Pixels in Image Super-Resolution Transformer
> 魔改Transformer

## Abstract
基于Transformer的方法，在低级视觉任务中（如：图像超分辨率）有着很高的表现。
但是，通过归因分析（attribution analysis）发现，这一网络只能使用**有限空间范围**的输入信息。
提出了混合注意力Transformer（Hybrid Attention Transformer， HAT），结合了通道注意力（channel attention）和基于窗口的自注意力机制（window-based self-attention schemes）的互补优势； 同时引入交叉注意力模块（cross-attention module）提升相邻窗口特征的交互。
在训练阶段，采用了相似任务预训练策略（same-task pre-train strategy）。
