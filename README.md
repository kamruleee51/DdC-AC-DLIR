## [Deep learning image registration for cardiac motion estimation in adult and fetal echocardiography via a focus on anatomic plausibility and texture quality of warped image](https://arxiv.org/abs/2309.00831)

<p align="justify"> Temporal echocardiography image registration is important for cardiac motion estimation, myocardial strain assessments, and stroke volume quantifications. Deep learning image registration (DLIR) is a promising way to achieve consistent and accurate registration results with low computational time. DLIR seeks the image deformation that enables the moving image to be warped to match the fixed image. We propose that, during DLIR training, a greater focus on the warped moving image's anatomic plausibility and image texture can support robust results, and we show that it has sufficient robustness to be applied to both fetal and adult echocardiography. Our proposed framework (as shown in the following Fig.1) includes (1) an anatomic shape-encoded constraint to preserve physiological myocardial and left ventricular anatomical topologies in the warped image, (2) a data-driven texture constraint to preserve good texture features in the warped image, and (3) a multi-scale training algorithm to improve accuracy. Our experiments demonstrate a strong correlation between the shape-encoded constraint and good anatomical topology and between the data-driven texture constraint and image textures. They improve different aspects of registration results in a non-overlapping way. We demonstrate that these methods can successfully register both fetal and adult echocardiography using our multi-demographic fetal dataset and the public CAMUS adult dataset, despite the inherent differences between adult and fetal echocardiography. Our approach also outperforms traditional non-DL gold standard registration approaches, including optical flow and Elastix, and could be translated into more accurate and precise clinical quantification of cardiac ejection fraction, demonstrating potential for clinical utility. </p>

<p align="justify">
</p>
<p align="center">
<img width="1000" alt="DLIR_model" src="https://github.com/user-attachments/assets/3391636e-9b66-4076-a4d1-b0e65c8f5626">
</p>


### Implementation: <br>  
**Task 1** involves training the mask topology encoder (part of block **B**) using the provided scripts (**LV:** *VAE_LV.ipynb* and **MYO:** *VAE_LV.ipynb*). All the masks are utilized for training this VAE, and the masks are augmented using the script (*VAE_Augmentation.ipynb*). These augmentations include **HorizontalFlip** and **CenterCrop** from the [albumentations library](https://albumentations.ai/). The trained VAE will be used as a pre-trained model and frozen in our proposed DLIR. Examples of the outputs of the VAE for LV and MYO reconstructions are shown below:
  
<p align="justify">
</p>
<p align="center">
<img width="700" alt="LV_masks" src="https://github.com/user-attachments/assets/7f388f68-54b7-4c73-aae1-a528b16ef68a">
</p>

<p align="justify">
</p>
<p align="center">
<img width="700" alt="MYO_masks" src="https://github.com/user-attachments/assets/423e43ea-b4c2-4e50-8a15-be88910fcbc3">
</p>

In **Task 2**, we use the pre-trained VAE model from Task 1 to extract anatomical topology for the warped and fixed mask. Then, we combine and train blocks **A**, **B**, and **C** for our **Texture-Anatomic-DLIR** using the provided script _Texture_Anatomic_DLIR.ipynb_. For multi-scale training, the network is initially trained with an input resolution of 32x32. Then, this trained model is used as a pre-trained model for the subsequent higher resolutions such as 64x64 and so on (details in the [paper](https://arxiv.org/abs/2309.00831)). The loss values and corresponding DICE-score improvements should be similar to the following loss/DICE over the epoch.

<p align="justify">
</p>
<p align="center">
<img width="1000" alt="Loss" src="https://github.com/user-attachments/assets/63a73032-cc55-40d6-b57d-0368ebb6982f">
</p>

[![Everything Is AWESOME](https://i.sstatic.net/q3ceS.png)](https://youtu.be/StTqXEQ2l-Y?t=35s "Everything Is AWESOME")

**Mandatory citation if this repo is useful:**<br>
@article{hasan2023multi,<br>
  title={Multi-scale, Data-driven and Anatomically Constrained Deep Learning Image Registration for Adult and Fetal Echocardiography.},<br>
  author={Hasan, Md Kamrul and Zhu, Haobo and Yang, Guang and Yap, Choon Hwai},<br>
  journal={arXiv:2309.00831},<br>
  year={2023}<br>
}


### Contact: <br>
MD KAMRUL HASAN || Research Postgraduate (Ph.D.)\
Department of Bioengineering || Imperial College London (ICL)\
80 Wood Ln, London W12 7TA, United Kingdom\
E-mail: k.hasan22@imperial.ac.uk or kamruleeekuet@gmail.com <br>
[Google Scholar](https://scholar.google.com/citations?user=36WXELIAAAAJ&hl=en) || [LinkedIn](https://www.linkedin.com/in/md-kamrul-hasan-0903051/) || [Website](https://med-ai.netlify.app/) 
