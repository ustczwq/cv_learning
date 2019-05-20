<!-- page_number : true -->

# Dynamic Convolution Implementation

- [Dynamic Filter Networks](https://arxiv.org/abs/1605.09673)
- [Selective Kernel Networks](https://arxiv.org/abs/1903.06586)

---
# Dynamic Kernels in Color Constancy
- Why dynamic kernels
  - adaptive attention
  - confidence weight of each patch in each channel 
- Why non-local
  - respective fields
  - global statistical regularities
- **Implementation**
  - Representational ability

---
# Dynamic Filter
<div align='center'>
  <img src='filter.png'>
</div>

$$G(i, j) = \mathcal F_\theta^{(i, j)}(I_B(i, j))$$

---
# Selective Kernel Networks
<div align='center'>
  <img src='selective.png'>
</div>

$$\mathbf z = \mathcal F_{fc}(\mathbf s) = \delta(\mathcal B(\mathbf Ws))$$

$$a_c = \frac{e^{\mathbf{A_c z}}}{e^{\mathbf{A_c z}} + e^{\mathbf{B_c z}}}, b_c = \frac{e^{\mathbf{B_c z}}}{e^{\mathbf{A_c z}} + e^{\mathbf{B_c z}}}$$

---
# Related Works

---
# Network In Network

<div align='center'>
  <img src='NIN.png'>
</div>

- MLP (~~GLM~~)
  - Abstraction Capability
- GAP (~~Fully Connected~~)
  - Prevent Overfitting

---
# Inception

<div align='center'>
  <img src='GoogleNet.png' width=300>
</div>

- GoogleNet (Naive & V1)
- Inception-V2
- Inception-V3
- Inception-V4

---
# ResNeXt

<div align='center'>
  <img src='ResNeXt.png'>
</div>

- ResNet + Inception
- Multi-branch
- Homogeneous

---
# Network Architecture

<img src='net.png'>


---
<div align='center'>
  <img src='filter.png'>
  <img src='selective.png'>
</div>


---
# Implementation Details
## Dynamic Scaling
- Local Similarity
- Dilated Convolution
## Guidance Map
- Non-local
- Kernels: patch consistency 
