---
permalink: /
title: ""
excerpt: "About the paper"
author_profile: false
redirect_from: 
  /about/
  /about.html
---



<h1 style="text-align: center; font-size: 36px; font-family: 'system-ui';"> Towards Automated Large-Scale Infrastructure Inspection  </h1>
<h2  style="text-align: center; font-size: 25px; font-family: 'Sama Devanagari';">
    Submitted to 2024 IEEE International Conference on Robotics and Automation
</h2>
<div style=" text-align: center; font-size: 17px;">
Guidong Yang, Benyun Zhao, Jihan Zhang, Yijun Huang, Xi Chen, and <a href="http://www.mae.cuhk.edu.hk/~bmchen/">Ben M. Chen</a><sup>1</sup>, Fellow, IEEE
</div>
<div  style="text-align: center; font-size: 17px;" >
The Chinese University of Hong Kong &nbsp; &nbsp; &nbsp;

</div>
<div style="display: flex; flex-direction: row; margin: 10px auto; justify-content: center"> 

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px;border: none; border-radius: 5px;">
<a href="https://www.overleaf.com/" style="color: white; text-decoration: none;">Paper</a>
</button>

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px; border: none; border-radius: 5px;">
<a href="https://github.com/CUHK-USR-Group/Defect-Dataset" style="color: white; text-decoration: none;">Dataset</a>
</button>

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px; border: none; border-radius: 5px;">
<a href="#detailed-section" style="color: white; text-decoration: none;">Supplementary</a>
</button>

</div>

<div style="text-align: center; font-family: 'American Typewriter'; font-weight: 400; "> 
<h2>Abstract</h2>
</div>
<div style="text-align: justify; text-justify:inter-ideograph;">

3D reconstruction is essential to defect localization. This paper proposes LCM-MVSNet, a novel multi-view stereo (MVS) network with learnable cost metric (LCM) for more accurate and complete dense point cloud reconstruction. To adapt to the scene variation and improve the reconstruction quality in non-Lambertian low-textured scenes, we propose LCM to adaptively aggregate multi-view matching similarity into the 3D cost volume by leveraging sparse point hints. The proposed LCM benefits the MVS approaches in four folds, including depth estimation enhancement, reconstruction quality improvement, memory footprint reduction, and computational burden alleviation, allowing the depth inference for high-resolution images to achieve more accurate and complete reconstruction. Additionally, we improve the depth estimation by enhancing the shallow feature propagation via a bottomup pathway and strengthen the end-to-end supervision by adapting the focal loss to reduce ambiguity caused by sample imbalance. Extensive experiments are carefully conducted on three benchmark datasets to validate that our method achieves state-of-the-art performance on the <em> DTU </em>and <em>BlendedMVS</em> dataset, and exhibits strong generalization ability with a competitive performance on the <em> Tanks and Temples </em> benchmark. Furthermore, we deploy our  LCM-MVSNet into our UAV-based infrastructure defect inspection system for reconstruction-based defect localization, demonstrating the effectiveness, efficiency, and scalability of our method. More experiment results can be found in the <a href="http://shorturl.at/xFRSU">Appendix</a>.

</div>

-----

<div style="font-size: 25px; text-align: center; font-family: 'American Typewriter'; font-weight: 800; ">    Comparison with the state of the arts
</div>
<h3>
Depth estimation performance on the <i>DTU</i> dataset</h3>
<div class="image-container" style="margin: 40px auto; text-align: center;">
        <img src="images/dtu_depth-2.png" alt="DTU depth comparison" width="85%">
        <p>Qualitative comparison of the depth map estimations on <em>Scan13</em> (<em>1st</em> row) and <em>Scan33</em> (<em>2nd</em> row) of the <em>DTU evaluation set</em>.</p>
</div>

----
<h3>
Reconstruction performance on the<i> DTU </i> dataset </h3>

<div class="image-container" style="margin: 40px auto;text-align: center;">
    <img src="images/dtu_points-5.png" alt="DTU depth comparison" width="85%">
    <p>Qualitative comparison of the point cloud reconstruction of <em>Scan12</em> (<em>1st</em> row), <em>Scan13</em> (<em>2nd</em> row) and <em>Scan77</em> (<em>3rd</em> row) on the <em>DTU evaluation set</em>.</p>
</div>

---

<h3>
Reconstruction performance on the<i> Tanks and Temples</i> dataset </h3>

<div class="image-container"  style="margin: 40px auto; text-align: center;">
    <img src="images/TNT-Compare-2.png" alt="DTU depth comparison" width="85%">
    <p> The visualization of the reconstruction errors of the four scenes including <em> Family</em>, <em>Francis</em>, <em>Auditorium</em>, and <em>Courtroom </em> on the <em> Tanks and Temples</em> benchmark. <em>&tau;</em>  is the per-scene point distance threshold defined by the benchmark and darker color indicates a larger reconstruction error with respect to     <em>&tau;</em>.</p>  
</div>

---
<div style="font-size: 25px; text-align: center; font-family: 'American Typewriter'; font-weight: 800; ">   Performance in the real world
</div>

<div class="sketchfab-embed-wrapper"> <iframe title="Huzhong_downsampled" frameborder="0" style="width: 500px;" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share src="https://sketchfab.com/models/28617af9340f4ee5b6ba50b1a213ff66/embed"> </iframe> <p style="font-size: 13px; font-weight: normal; margin: 5px; color: #4A4A4A;"> <a href="https://sketchfab.com/3d-models/huzhong-downsampled-28617af9340f4ee5b6ba50b1a213ff66?utm_medium=embed&utm_campaign=share-popup&utm_content=28617af9340f4ee5b6ba50b1a213ff66" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;"> Huzhong_downsampled </a> by <a href="https://sketchfab.com/hyjcde?utm_medium=embed&utm_campaign=share-popup&utm_content=28617af9340f4ee5b6ba50b1a213ff66" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;"> hyjcde </a> on <a href="https://sketchfab.com?utm_medium=embed&utm_campaign=share-popup&utm_content=28617af9340f4ee5b6ba50b1a213ff66" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;">Sketchfab</a></p></div>
<br>
<br><br><br>
<iframe src="https://potree.github.io/potree/examples/elevation_profile.html"
width="100%"
height="600"
frameborder="0"
allowfullscreen
style="border: none;"></iframe>



<div style=";font-size: 25px; text-align: center; font-family: 'American Typewriter'; font-weight: 800; ">  Acknowledgements  </div>
<div style="text-align: justify">This work was supported by the InnoHK of the Government of the Hong Kong Special Administrative Region via the Hong Kong Centre for Logistics Robotics.
</div>
