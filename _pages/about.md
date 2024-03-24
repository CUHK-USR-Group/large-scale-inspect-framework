---
permalink: /
title: ""
excerpt: "About the paper"
author_profile: false
redirect_from:
    /about/
    /about.html
---



<h1 style="text-align: center; font-size: 36px; font-family: 'system-ui';"> Det-Recon-Reg: An Intelligent Framework Towards Automated Large-Scale Infrastructure Inspection  </h1>
<h2  style="text-align: center; font-size: 18px; font-family: 'Sama Devanagari';">
    Submitted to 2024 IEEE International Conference on Intelligent Robots and Systems
</h2>
<div style=" text-align: center; font-size: 17px;">
Guidong Yang, Jihan Zhang, Benyun Zhao, Chuanxiang Gao, Yijun Huang, <br> Junjie Wen, Qingxiang Li, Xi Chen, and Ben M. Chen, Fellow, IEEE
</div>
<div  style="text-align: center; font-size: 17px;" >
The Chinese University of Hong Kong, Hong Kong SAR, China

</div>
<div style="display: flex; flex-direction: row; margin: 10px auto; justify-content: center"> 

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px;border: none; border-radius: 5px;">
<a href="pdfs/IROS_2024_paper.pdf" style="color: white; text-decoration: none;">Paper</a>
</button>

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px; border: none; border-radius: 5px;">
<a href="https://github.com/CUHK-USR-Group/Defect-Dataset" style="color: white; text-decoration: none;">Dataset and Code</a>
</button>

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px; border: none; border-radius: 5px;">
<a href="pdfs/IROS_2024_Appendix.pdf" style="color: white; text-decoration: none;">Appendix</a>
</button>

</div>

<div style="text-align: center; font-family: 'American Typewriter'; font-weight: 400; "> 
<h2>Abstract</h2>
</div>
<div style="text-align: justify; text-justify:inter-ideograph;">

Visual inspection plays a predominant role in inspecting infrastructure surface. However, the generalization of existing visual inspection systems to large-scale real-world scenes remains challenging. In this paper, we introduce <strong> Det-Recon-Reg</strong>, an intelligent framework separating the complex inspection procedure into three stages: <strong>Detect</strong>, <strong>Reconstruct</strong>, and <strong>Register</strong>. For defect detection (<strong>Detect</strong>), we present the first high-resolution defect dataset tailored for large-scale defect detection. Based on the dataset, we evaluate the most effective real-time object detection algorithms and push the boundary by proposing CUBIT-Net for real-world defect inspection. For infrastructure reconstruction (<strong>Reconstruct</strong>), we propose a learning-based multi-view stereo (MVS) network to adapt to large-scale scenes, taking as input the multi-view images and outputting the point cloud reconstruction, where its performance has been validated on the standard MVS datasets, including BlendedMVS, DTU, and Tanks and Temples datasets. For defect localization (<strong>Register</strong>), we propose an effective registration method based on the geographic information system that registers the detected defects onto the reconstructed infrastructure model to establish a global reference for maintenance measures. The real-world experiments verify the effectiveness and efficiency of our proposed framework.

</div>

<div style="text-align: center; font-family: 'American Typewriter'; font-weight: 400; "> 

<h2>Demo Video</h2>

</div>

<div style="margin: 10px auto; padding: 3px auto;">

<video controls style="margin: 10px auto; width: 100%;">
  <source src="images/Video_IROS.mp4" type="video/mp4">
  your browser does not support video tag.
</video>

</div>

<div style="text-align: center; font-family: 'American Typewriter'; font-weight: 400; "> 
<h2>Inspection Framework</h2>

</div>


<div class="image-container"  style="margin: 40px auto; text-align: center; font-weight: 400;">
    <img src="images/workflow.png" alt="" width="100%">
<div style="text-align: justify; font-size: 14px;  text-justify:inter-ideograph;">
<p style="text-align: justify; font-size: 14px;  text-justify:inter-ideograph;">
The structure of the proposed <strong><em>Det-Recon-Reg</em></strong> framework for large-scale infrastructure inspection. We adopt multi-UAV coverage path planning to collect multi-view images for reconstruction and close-range facade images for surface defect detection. <strong><em>Detect</em></strong>: We deploy the proposed CUBIT-Net trained on the established CUBIT-Det dataset to detect surface flaws. <strong><em>Reconstruct</em></strong>: We leverage the proposed MVS network to predict multi-view depth maps and fuse them to reconstruct the infrastructure. <strong><em>Register</em></strong>: We identify the global position of the detected defects based on GIS.</p>

</div>
</div>



<div style="text-align: center; font-family: 'American Typewriter'; font-weight: 400; "> 
<h2>Acknowledgements</h2>
</div>

<div style="text-align: justify">This work was supported by the InnoHK of the Government of the Hong Kong Special Administrative Region via the Hong Kong Centre for Logistics Robotics.
<br> <br>
We sincerely appreciate the time and efforts paid by all the IROS reviewers.
</div>
