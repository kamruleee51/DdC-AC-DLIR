## [Multi-scale, Data-driven and Anatomically Constrained Deep Learning Image Registration for Adult and Fetal Echocardiography](https://arxiv.org/abs/2309.00831)

<p align="justify"> Temporal echocardiography image registration is a foundation for clinical quantifications such as cardiac motion estimation, myocardial strain assessments, and stroke volume quantifications. In earlier implementations, deep learning image registration (DLIR) has shown promising results and is consistently accurate and exact. It also requires less computing effort. We suggest focusing on warped moving image anatomic plausibility and image quality to improve DLIR performance. Past DLIR implementations focused on adult echocardiography, not fetal. Our framework for DLIR for fetal and adult echo includes an anatomic shape-encoded loss to preserve physiological myocardial and left ventricular anatomical topologies in warped images, a data-driven loss trained adversarially to preserve good image texture features, and a multi-scale training scheme of a data-driven and anatomically constrained algorithm to improve accuracy. Our results reveal that good anatomical topology and image textures highly correlate with shape-encoded and data-driven adversarial losses. Their combination is justified since they boost registration performance in distinct ways. We show that these techniques can register adult and fetal echocardiograms well using the publicly accessible CAMUS adult echo dataset and our private multi-demographic fetal echo dataset, despite fundamental differences. Our method outperforms Optical Flow and Elastix, non-DL gold standard registration methods. </p>

<p align="justify">
Table: The architecture of the topological shape encoder to learn the latent vectors of LV and MYO. Conv: Convolution layer with a dilation of 1; BN: Batch normalization for each mini-batch; ReLU: Rectified linear unit; FC: Fully connected layer; TConv: Transpose convolution layer for the upsampling with a dilation of 1; SIG: Sigmoid activation at the output; B: Mini-batch size; and $d$: Latent vector dimension ($\mathcal{Z}^d$).
</p>
<p align="center">
<img width="750" alt="Shape_Encoder" src="https://github.com/kamruleee51/DdC-AC-DLIR/assets/32570071/6c0f7808-27b3-4ea7-baeb-c0968174f82b">
</p>


<p align="justify">
Table: Discriminator's architecture to learn the intensity images' attributes ($I_F$ and $I_W=I_M\circ \varphi$) in adversarial training to retrieve the texture features in the moved intensity images ($I_W=I_M\circ \varphi$). Conv: Convolution layer with a dilation of 1; IN: Instance normalization for each mini-batch; LReLU: Leaky Rectified linear unit; FC: Fully connected layer; SIG: Sigmoid activation at the output; and B: Mini-batch size.
</p>
<p align="center">
<img width="779" alt="Discriminator" src="https://github.com/kamruleee51/DdC-AC-DLIR/assets/32570071/218a7e98-aa54-4a2a-a39c-c06542e19d13">
</p>


# Codes are uploading soon!!


