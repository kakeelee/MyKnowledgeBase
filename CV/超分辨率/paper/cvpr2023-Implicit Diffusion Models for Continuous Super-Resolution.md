# Implicit Diffusion Models for Continuous Super-Resolution

## Abstract
现今的超分辨方法通常存在<u>过度平滑</u>和<u>伪影</u>的问题，并且大多数方法只适用于固定的放大倍数。
提出了隐式扩散模型用于[高保真连续图像超分辨率，high-fidelity continuous image super-resolution](#hfcisr), 该方法整合了[隐式神经表示，Implicit neural representation](#inr)和[去噪扩散模型，denoising diffusion model](#denoising-diffusion-model去噪扩散模型)。  
**隐式神经表示**在解码过程中学习连续分辨率的表示。



## Appendix
### high-fidelity continuous image super-resolution <a id = "hfcisr">
高保真连续图像超分辨率的目标是尽可能地减少重建过程中的伪影和平滑效果，以产生更加真实和细节丰富的超分辨率图像。这种方法在许多领域中都有应用，包括医学图像处理、卫星图像处理和视频增强等。

### Implicit neural representation（隐式神经表示） <a id = "inr">
Implicit neural representation（隐式神经表示）是一种用于表示几何形状和物体表面的方法。  
在隐式神经表示中，一个神经网络被训练来接受输入坐标，并输出一个表示该坐标处物体属性的值，例如表示该点是否在物体内部或外部。通过在整个空间中对坐标进行采样并根据神经网络的输出值确定物体的边界，可以重建出物体的形状。

### denoising diffusion model（去噪扩散模型） <a id = "ddm">
去噪扩散模型（Denoising Diffusion Model）是一种用于图像去噪的深度学习模型。它基于扩散过程的概念，通过迭代地应用一系列扩散步骤来减少图像中的噪声。

Denoising Diffusion Model的基本思想是，在每个扩散步骤中，模型会对输入图像进行一系列的变换操作，通过这些操作来逐渐减少图像中的噪声。这些变换操作可以是线性的或非线性的，它们可以通过卷积、激活函数或其他图像处理技术来实现。

在每个扩散步骤之后，模型会利用损失函数来评估输出图像与真实图像之间的差异，并通过反向传播算法来更新模型的参数。通过反复迭代这个过程，模型可以逐渐学习到如何去除输入图像中的噪声，并生成更加清晰和真实的图像。

Denoising Diffusion Model在图像去噪领域取得了很好的效果，并且在实际应用中具有广泛的潜力。它可以应用于各种类型的图像噪声去除任务，包括高斯噪声、椒盐噪声和低光照噪声等。此外，它还可以与其他图像处理技术结合使用，如超分辨率和图像增强，以进一步提高图像质量。