## [Deep learning image registration for cardiac motion estimation in adult and fetal echocardiography via a focus on anatomic plausibility and texture quality of warped image](https://arxiv.org/abs/2309.00831)

<p align="justify"> Temporal echocardiography image registration is important for cardiac motion estimation, myocardial strain assessments, and stroke volume quantifications. Deep learning image registration (DLIR) is a promising way to achieve consistent and accurate registration results with low computational time. DLIR seeks the image deformation that enables the moving image to be warped to match the fixed image. We propose that, during DLIR training, a greater focus on the warped moving image's anatomic plausibility and image texture can support robust results, and we show that it has sufficient robustness to be applied to both fetal and adult echocardiography. Our proposed framework includes (1) an anatomic shape-encoded constraint to preserve physiological myocardial and left ventricular anatomical topologies in the warped image, (2) a data-driven texture constraint to preserve good texture features in the warped image, and (3) a multi-scale training algorithm to improve accuracy. Our experiments demonstrate a strong correlation between the shape-encoded constraint and good anatomical topology and between the data-driven texture constraint and image textures. They improve different aspects of registration results in a non-overlapping way. We demonstrate that these methods can successfully register both fetal and adult echocardiography using our multi-demographic fetal dataset and the public CAMUS adult dataset, despite the inherent differences between adult and fetal echocardiography. Our approach also outperforms traditional non-DL gold standard registration approaches, including optical flow and Elastix, and could be translated into more accurate and precise clinical quantification of cardiac ejection fraction, demonstrating potential for clinical utility. </p>



### Contact: <br>
MD KAMRUL HASAN || Research Postgraduate (Ph.D.)\
Department of Bioengineering || Imperial College London (ICL)\
80 Wood Ln, London W12 7TA, United Kingdom\
E-mail: k.hasan22@imperial.ac.uk or kamruleeekuet@gmail.com <br>
Google Scholar: https://scholar.google.com/citations?user=36WXELIAAAAJ&hl=en



<p align="justify">
Table: Discriminator's architecture to learn the intensity images' attributes ($I_F$ and $I_W=I_M\circ \varphi$) in adversarial training to retrieve the texture features in the moved intensity images ($I_W=I_M\circ \varphi$). Conv: Convolution layer with a dilation of 1; IN: Instance normalization for each mini-batch; LReLU: Leaky Rectified linear unit; FC: Fully connected layer; SIG: Sigmoid activation at the output; and B: Mini-batch size.
</p>
<p align="center">
<img width="779" alt="Discriminator" src="https://github.com/kamruleee51/DdC-AC-DLIR/assets/32570071/218a7e98-aa54-4a2a-a39c-c06542e19d13">
</p>
