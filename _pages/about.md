---
permalink: /
title: ""
excerpt: "About the paper"
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---
<embed src="/pdfs/network.pdf" type="application/pdf" />
<h1 style="font-size: 50px; font-family: 'Sama Devanagari';"> Learnable Cost Metric Based Multi-View Stereo for Point Cloud Reconstruction
</h1>

## Authors

 <a href="https://orcid.org/0009-0003-2940-8499" target="_blank">
        <img src="https://orcid.org/sites/default/files/images/orcid_16x16(1).gif" alt="ORCID logo">
        Guidong Yang
</a>
 , Xunkuai Zhou, Chuanxiang Gao, Xi Chen, and Ben M. Chen, Fellow, IEEE

<img src="/images/Classification_Sample_Images.png"/>

## Abstract
3D reconstruction is essential to defect localization. This paper proposes LCM-MVSNet, a novel multi-view stereo (MVS) network with learnable cost metric (LCM) for more accurate and complete dense point cloud reconstruction. To adapt to the scene variation and improve the reconstruction quality in non-Lambertian low-textured scenes, we propose LCM to adaptively aggregate multi-view matching similarity into the 3D cost volume by leveraging sparse point hints. The proposed LCM benefits the MVS approaches in four folds, including depth estimation enhancement, reconstruction quality improvement, memory footprint reduction, and computational burden alleviation, allowing the depth inference for high-resolution images to achieve more accurate and complete reconstruction. Additionally, we improve the depth estimation by enhancing the shallow feature propagation via a bottom-up pathway and strengthen the end-to-end supervision by adapting the focal loss to reduce ambiguity caused by sample imbalance. Extensive experiments are carefully conducted on three benchmark datasets to validate that our method achieves state-of-the-art performance on the \textit{DTU} and \textit{BlendedMVS} dataset, and exhibits strong generalization ability with a competitive performance on the \textit{Tanks and Temples} benchmark. Furthermore, we deploy our LCM-MVSNet into our UAV-based infrastructure defect inspection system for reconstruction-based defect localization, demonstrating the effectiveness, efficiency, and scalability of our method. More experiment results can be found in the Appendix~\footnote{shorturl.at/xFRSU}.


Multi-View Stereo (MVS) aims to recover the 3D representation of a scene by leveraging stereo correspondences from multiple calibrated 2D images. Recently, learning-based MVS approaches have significantly surpassed traditional methods in various benchmarks. These deep MVS methods split the MVS process into two stages: learning-based depth map estimation and depth map filtering & fusion. By leveraging powerful feature extraction and cost volume representation, deep MVS methods can achieve superior reconstruction accuracy and completeness. However, there are areas for improvement in these methods, especially in handling over-smoothing around object boundaries.

## Introduction
## Feature Pyramid Extraction

Recent learning-based methods adopt a coarse-to-fine depth estimation strategy, utilizing Feature Pyramid Networks (FPN) to extract multi-scale image features for constructing cost volumes at varying resolutions. However, issues such as over-smoothing around object boundaries arise due to a lack of shallow feature information containing essential low-level features like local textures and edges. To address this, the authors introduced a bottom-up pathway to augment the propagation of low-level features. This also enlarges the receptive field to incorporate global context information, ensuring accurate and robust feature matching, especially in low-textured regions. The feature pyramid extraction network uses multi-view images as input, outputting multi-level feature pyramids for each image. These pyramids consider factors like the level ordinal, channel number of the feature map, and the height and width of the feature map.


<a href="https://youtube.com/watch?v=UJ3akL3gH68" target="_blank">
        <img src="https://s.ytimg.com/yts/img/favicon-vfl8qSV2F.ico" alt="YouTube logo" width="16" height="16">
        YouTube
    </a>
<iframe width="420" height="315"
src="https://www.youtube.com/embed/UJ3akL3gH68?autoplay=1&mute=1">
</iframe>

### Defect Detection
### 3D Reconstruction System
### GIS-based Registration

## Acknowledgements