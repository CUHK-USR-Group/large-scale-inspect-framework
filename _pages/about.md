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
Guidong Yang, Benyun Zhao, Jihan Zhang, Yijun Huang, Xi Chen, and <a href="http://www.mae.cuhk.edu.hk/~bmchen/">Ben M. Chen</a>, Fellow, IEEE
</div>
<div  style="text-align: center; font-size: 17px;" >
The Chinese University of Hong Kong, Hong Kong &nbsp; &nbsp; &nbsp;

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
Visual inspection plays a predominant role in surface defect inspection. However, the generalization of existing visual inspection systems to large-scale real-world scenes remains challenging. In this paper, we introduce a novel and practical inspection framework based on advanced unmanned aerial vehicles and learning-based techniques as a significant step towards automating the inspection of large-scale infrastructure. Our framework separates the complex inspection procedure into three stages: <em>Detect</em>, <em>Reconstruct</em>, and <em>Register</em>. For defect detection (<em>Detect</em>), we present an open-source defect dataset tailored for large-scale defect detection. Based on the dataset, we evaluate the most effective real-time object detection algorithms and push the boundary by proposing CUBIT-Net for real-world defect inspection. For infrastructure reconstruction (<em>Reconstruct</em>), we propose a learning-based multi-view stereo (MVS) network to adapt to large-scale scenes, taking as input the multi-view images and outputting the point cloud reconstruction, where its performance has been validated via comparative experiments on the standard MVS datasets, including BlendedMVS, DTU, and Tanks and Temples dataset. For defect localization (<em>Register</em>), we develop a WebGIS platform that incorporates the detected defects and registers them onto the reconstruction model based on geographic information, thereby establishing a reliable reference for maintenance measures. Finally, extensive on-site experiments further demonstrate the effectiveness, efficiency, and scalability of the proposed inspection framework. Dataset and <a href=""> Appendix </a> are available in our project page

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


<div style=";font-size: 25px; text-align: center; font-family: 'American Typewriter'; font-weight: 800; ">  Acknowledgements  </div>
<div style="text-align: justify">This work was supported by the InnoHK of the Government of the Hong Kong Special Administrative Region via the Hong Kong Centre for Logistics Robotics.
</div>
