## [Deep learning image registration for cardiac motion estimation in adult and fetal echocardiography via a focus on anatomic plausibility and texture quality of warped image](https://arxiv.org/abs/2309.00831)

<p align="justify"> Temporal echocardiography image registration is important for cardiac motion estimation, myocardial strain assessments, and stroke volume quantifications. Deep learning image registration (DLIR) is a promising way to achieve consistent and accurate registration results with low computational time. DLIR seeks the image deformation that enables the moving image to be warped to match the fixed image. We propose that, during DLIR training, a greater focus on the warped moving image's anatomic plausibility and image texture can support robust results, and we show that it has sufficient robustness to be applied to both fetal and adult echocardiography. Our proposed framework (as shown in the following Fig.1) includes (1) an anatomic shape-encoded constraint to preserve physiological myocardial and left ventricular anatomical topologies in the warped image, (2) a data-driven texture constraint to preserve good texture features in the warped image, and (3) a multi-scale training algorithm to improve accuracy. Our experiments demonstrate a strong correlation between the shape-encoded constraint and good anatomical topology and between the data-driven texture constraint and image textures. They improve different aspects of registration results in a non-overlapping way. We demonstrate that these methods can successfully register both fetal and adult echocardiography using our multi-demographic fetal dataset and the public CAMUS adult dataset, despite the inherent differences between adult and fetal echocardiography. Our approach also outperforms traditional non-DL gold standard registration approaches, including optical flow and Elastix, and could be translated into more accurate and precise clinical quantification of cardiac ejection fraction, demonstrating potential for clinical utility. </p>

<p align="justify">
</p>
<p align="center">
<img width="906" alt="DLIR_model" src="https://github.com/user-attachments/assets/3391636e-9b66-4076-a4d1-b0e65c8f5626">
</p>


### Implementation: <br>  
**Task 1** involves training the mask topology encoder (part of block B) using the provided scripts (**LV:** *VAE_LV.ipynb* and **MYO:** *VAE_LV.ipynb*). All the masks are utilized for training this VAE, and the masks are augmented using the script (*VAE_Augmentation.ipynb*). These augmentations include HorizontalFlip and CenterCrop from the [albumentations library](https://albumentations.ai/). The trained VAE will be used as a pre-trained model and frozen in our proposed DLIR. Examples of the outputs of the VAE for LV and MYO reconstructions are shown below: 



### Contact: <br>
MD KAMRUL HASAN || Research Postgraduate (Ph.D.)\
Department of Bioengineering || Imperial College London (ICL)\
80 Wood Ln, London W12 7TA, United Kingdom\
E-mail: k.hasan22@imperial.ac.uk or kamruleeekuet@gmail.com <br>
Google Scholar: https://scholar.google.com/citations?user=36WXELIAAAAJ&hl=en
