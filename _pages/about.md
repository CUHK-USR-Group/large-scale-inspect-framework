---
permalink: /
title: ""
excerpt: "About the paper"
author_profile: false
redirect_from: 
  /about/
  /about.html
---



<h1 style="text-align: center; font-size: 36px; font-family: 'system-ui';"> Learnable Cost Metric Based Multi-View Stereo for Point Cloud Reconstruction
</h1>
<h2  style="text-align: center; font-size: 25px; font-family: 'Sama Devanagari';">
    Submitted to IEEE TRANSACTIONS ON INDUSTRIAL ELECTRONICS
</h2>
<div style=" text-align: center; font-size: 17px;">
Guidong Yang<sup>1</sup> , Xunkuai Zhou<sup>1, 2</sup>, Chuanxiang Gao<sup>1</sup>,  Xi Chen<sup>1</sup>
, and <a href="http://www.mae.cuhk.edu.hk/~bmchen/">Ben M. Chen</a><sup>1</sup>, Fellow, IEEE
</div>
<div  style="text-align: center; font-size: 17px;" >
1. The Chinese University of Hong Kong &nbsp; &nbsp; &nbsp; 2.Tongji University

</div>
<div style="display: flex; flex-direction: row; margin: 10px auto; justify-content: center"> 

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px;border: none; border-radius: 5px;">
<a href="https://www.overleaf.com/project/64acc26ed265fde278ed8fb4" style="color: white; text-decoration: none;">Paper</a>
</button>

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px; border: none; border-radius: 5px;">
<a href="/dataset" style="color: white; text-decoration: none;">Dataset</a>
</button>

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px; border: none; border-radius: 5px;">
<a href="#detailed-section" style="color: white; text-decoration: none;">Supplementary</a>
</button>

</div>

<div style="text-align: center; font-family: 'American Typewriter'; font-weight: 400; "> 
<h2>Abstract</h2>
</div>
<div style="text-align: justify; text-justify:inter-ideograph;">

3D reconstruction is essential to defect localization. This paper proposes LCM-MVSNet, a novel multiview stereo (MVS) network with learnable cost metric (LCM) for more accurate and complete dense point cloud reconstruction. To adapt to the scene variation and improve the reconstruction quality in non-Lambertian low-textured scenes, we propose LCM to adaptively aggregate multiview matching similarity into the 3D cost volume by leveraging sparse point hints. The proposed LCM benefits the MVS approaches in four folds, including depth estimation enhancement, reconstruction quality improvement, memory footprint reduction, and computational burden alleviation, allowing the depth inference for high-resolution images to achieve more accurate and complete reconstruction. Additionally, we improve the depth estimation by enhancing the shallow feature propagation via a bottomup pathway and strengthen the end-to-end supervision by adapting the focal loss to reduce ambiguity caused by sample imbalance. Extensive experiments are carefully conducted on three benchmark datasets to validate that our method achieves state-of-the-art performance on the DTU and BlendedMVS dataset, and exhibits strong generalization ability with a competitive performance on the Tanks and Temples benchmark. Furthermore, we deploy our LCMMVSNet into our UAV-based infrastructure defect inspection system for reconstruction-based defect localization, demonstrating the effectiveness, efficiency, and scalability of our method. More experiment results can be found in the <a href="http://shorturl.at/xFRSU">Appendix</a>

</div>

-----

<div style="font-size: 25px; text-align: center; font-family: 'American Typewriter'; font-weight: 800; ">    Comparison with the state of the arts
</div>
<h3>
Depth estimation performance on the <i>DTU</i> dataset</h3>
<div class="image-container" style="margin: 40px auto; text-align: center;">
        <img src="images/dtu_depth-2.pdf" alt="DTU depth comparison" width="85%">
        <p>Qualitative comparison of the depth map estimations on <em>Scan13</em> (1st row) and <em>Scan33</em> (2nd row) of the <em>DTU evaluation set</em>.</p>
</div>

----
<h3>
Reconstruction performance on the<i> DTU </i> dataset </h3>

<div class="image-container" style="margin: 40px auto;text-align: center;">
    <img src="images/dtu_points-5.pdf" alt="DTU depth comparison" width="85%">
    <p> The visualization of the reconstruction errors of the four scenes including <em> Family</em>, <em>Francis</em>, <em>Auditorium</em>, and <em>Courtroom </em> on the Tanks and Temples benchmark. &tau; is the per-scene point distance threshold defined by the benchmark and darker color indicates a larger reconstruction error with respect to &tau;.</p>  
</div>

---

<h3>
Reconstruction performance on the<i> Tanks and Temples</i> dataset </h3>

<div class="image-container"  style="margin: 40px auto; text-align: center;">
    <img src="images/TNT-Compare-2.pdf" alt="DTU depth comparison" width="85%">
    <p> The visualization of the reconstruction errors of the four scenes including <em> Family</em>, <em>Francis</em>, <em>Auditorium</em>, and <em>Courtroom </em> on the Tanks and Temples benchmark.  is the per-scene point distance threshold defined by the benchmark and darker color indicates a larger reconstruction error with respect to &tau;.</p>  
</div>

---


<div style="font-size: 25px; text-align: center; font-family: 'American Typewriter'; font-weight: 800; ">  Acknowledgements  </div>

This work was supported by the InnoHK of the Government of the Hong Kong Special Administrative Region via the Hong Kong Centre for Logistics Robotics.