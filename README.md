## Multi-scale, Data-driven and Anatomically Constrained Deep Learning Image Registration for Adult and Fetal Echocardiography

<p align="justify"> Temporal echocardiography image registration is a foundation for clinical quantifications such as cardiac motion estimation, myocardial strain assessments, and stroke volume quantifications. In earlier implementations, deep learning image registration (DLIR) has shown promising results and is consistently accurate and exact. It also requires less computing effort. We suggest focusing on warped moving image anatomic plausibility and image quality to improve DLIR performance. Past DLIR implementations focused on adult echocardiography, not fetal. Our framework for DLIR for fetal and adult echo includes an anatomic shape-encoded loss to preserve physiological myocardial and left ventricular anatomical topologies in warped images, a data-driven loss trained adversarially to preserve good image texture features, and a multi-scale training scheme of a data-driven and anatomically constrained algorithm to improve accuracy. Our results reveal that good anatomical topology and image textures highly correlate with shape-encoded and data-driven adversarial losses. Their combination is justified since they boost registration performance in distinct ways. We show that these techniques can register adult and fetal echocardiograms well using the publicly accessible CAMUS adult echo dataset and our private multi-demographic fetal echo dataset, despite fundamental differences. Our method outperforms Optical Flow and Elastix, non-DL gold standard registration methods. </p>

<img width="693" alt="Shape_Encoder" src="https://github.com/kamruleee51/DdC-AC-DLIR/assets/32570071/6c0f7808-27b3-4ea7-baeb-c0968174f82b">

<img width="479" alt="Discriminator" src="https://github.com/kamruleee51/DdC-AC-DLIR/assets/32570071/218a7e98-aa54-4a2a-a39c-c06542e19d13">

# Codes are uploading soon!!


