# Towards High-Quality and Efficient Video Super-Resolution via Spatial-Temporal Data Overfitting

## Abstract
使用深度卷积神经网络（Deep Convolutional neural networks, DNNs）的过拟合能力提升分辨率。
实现思路：在服务器传送视频到客户端之前，将视频帧分为多个chunk，通过超分辨率模型（super resolution model）对每个chunk进行过拟合（overfitting），得到一个高质量画面和高效的传输能力。

问题：
1. 保证过拟合的效果需要大量的chunk，而大量的chunk又导致了存储占用和数据传输时的带宽消耗；
2. 通过训练优化技术减少chunk数量，又会降低执行速度，无法保证实时性。

提出的解决方案：
1. 使用空域-时域信息将视频准确划分chunk，保持其数量与模型需要的数量吻合
2. “数据感知融合技术”，来降低存储需要。

将模型部署到移动设备上，实验结果表明：相较于最新技术，该方法在28fps视频流中拥有41.6的峰值信噪比（Peak Signal-to-Noise Ratio, PSNR）(14x faster, and 2.29dB better)