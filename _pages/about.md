---
permalink: /
title: ""
excerpt: "About the paper"
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---
<img src="/images/image/network.pdf"/>

<p>This is an inline equation \( a = b \) and this is a block equation:</p>
$$ c = d $$

<h1 style="font-size: 50px; font-family: 'Sama Devanagari';"> Learnable Cost Metric Based Multi-View Stereo for Point Cloud Reconstruction
</h1>

## Authors

 <a href="https://orcid.org/0009-0003-2940-8499" target="_blank">
        <img src="https://orcid.org/sites/default/files/images/orcid_16x16(1).gif" alt="ORCID logo">
        Guidong Yang
</a>
 , Xunkuai Zhou, Chuanxiang Gao, Xi Chen, and Ben M. Chen, Fellow, IEEE

<img src="/images/Classification_Sample_Images.png"/>

<div style="font-family: 'American Typewriter'; font-weight: 400; "> 
<h2>🔍 Abstract</h2>
<hr>
<p>Welcome to the evolution of <strong><span style="color: #3498db;">3D reconstruction</span></strong> with the <mark>LCM-MVSNet</mark>. This state-of-the-art system ushers in a new era for multi-view stereo (MVS) reconstructions, offering depth and detail previously unattained.</p>

<blockquote>
  "Redefining the depth of 3D imaging by merging technology and innovation."
</blockquote>

<p>Challenging terrains like low-textured or reflective scenes? No problem. Our <em><span style="color: #e74c3c;">Learnable Cost Metric (LCM)</span></em> intelligently fuses images, refining depth intricacies, and delivering unparalleled reconstructions—efficiently and effectively.</p>

<img src="/images/Mawan_Sample_Images.png" alt="LCM-MVSNet Technology" width="500" style="display: block; margin: 0 auto;">

<p>Our rigorous benchmarks highlight the system's unmatched prowess, particularly on esteemed datasets like <a href="#DTU-dataset">DTU</a> and <a href="#BlendedMVS-dataset">BlendedMVS</a>. But it's not just about numbers. We've seamlessly blended our technology into a <span style="color: #2ecc71;">UAV-based platform</span> for aerial inspections, revealing a unique synergy between academic advancement and real-world application.</p>

<button style="background-color: #3498db; color: white; padding: 10px 15px; border: none; border-radius: 5px;"><a href="#full-paper" style="color: white; text-decoration: none;">Dive Deeper</a></button>

</div>

---


<h2>🌐 Introduction to LCM-MVSNet</h2>
<hr>
<p>Welcome to the next generation of <strong><span style="color: #3498db;">3D imaging</span></strong>. Dive deep with our transformative system, the <mark>LCM-MVSNet</mark>, offering a paradigm shift in multi-view stereo (MVS) reconstructions.</p>

<blockquote>
  "Pushing the boundaries of depth and detail in 3D reconstructions using multi-angle images."
</blockquote>

<p>Traditional techniques have their merits, but the realm of learning-based MVS is where the future lies. Our innovative approach addresses inherent challenges, such as over-smoothing and computational intensity. The cornerstone? Our <em><span style="color: #e74c3c;">Learnable Cost Metric (LCM)</span></em>—a tool that adapts gracefully to multi-view scenes, optimizing both performance and efficiency.</p>

<img src="/images/innovation-imperative.png" alt="Innovation in 3D Imaging" width="500" style="display: block; margin: 0 auto;">

<p>Our work isn’t confined to theory. Rigorous tests have spotlighted the prowess of LCM-MVSNet, with standout results on elite datasets like <a href="#DTU-dataset">DTU</a> and <a href="#BlendedMVS-dataset">BlendedMVS</a>. And for the real-world enthusiasts? We’ve integrated our system into a <span style="color: #2ecc71;">UAV-based platform</span>, dramatically transforming aerial infrastructure inspections. Our system, showcased in <a href="#fig1">Fig. 1</a>, melds high-resolution imagery with pinpoint 3D defect localization.</p>

<button style="background-color: #3498db; color: white; padding: 10px 15px; border: none; border-radius: 5px;"><a href="#detailed-section" style="color: white; text-decoration: none;">Explore Further</a></button>

<img src="/images/image/Framework.pdf"/>

---

<h2>📐 Methodology of Multi-View Stereo (MVS)</h2>
<hr>
<p>Discover the intricacies of our innovative two-stage MVS method, the <strong>LCM-MVSNet</strong>. Delving deep into automated point cloud reconstruction, this section unveils the techniques and strategies behind our state-of-the-art system.</p>

<figure>
  <img src="/images/lcm_mvsnet_overview.png" alt="Overview of LCM-MVSNet" style="width:100%; border: 1px solid #ddd; border-radius: 4px; padding: 5px;">
  <figcaption><i>Fig. 2: A bird's-eye view of the LCM-MVSNet architecture.</i></figcaption>
</figure>

<h3>A. Feature Pyramid Extraction</h3>
<p>Recent methodologies, including references [3], [8], [9], and [14], have leaned on the coarse-to-fine depth estimation approach. This is where our method stands out:</p>
<ul>
  <li>We've enhanced shallow feature information, crucial for preserving details like local textures and edges.</li>
  <li>Through a bottom-up pathway, we've improved the propagation of these low-level features, ensuring accurate feature matching even in challenging, low-textured regions.</li>
  <li>Our network seamlessly integrates in-place activated batch normalization (ABN), optimizing computational efficiency without compromising on memory.</li>
</ul>
<p>The result? A feature pyramid extraction network that efficiently processes multi-view images, capturing depth and detail at varying resolutions.</p>

<div style="background-color: #f9f9f9; padding: 15px; margin: 20px 0; border-left: 5px solid #3498db;">
  <strong>Note:</strong> Our feature pyramid extraction is comprehensive, consisting of 20 convolutional layers. For the enthusiasts, the details are consistent with [3], and an in-depth look at the structure can be found in Fig. 2. The systematic experiments in Subsection III-B further showcase the efficiency and accuracy of our approach.
</div>

<p><a href="#next-section" style="color: #3498db; text-decoration: none;">Continue to the next section ➡️</a></p>


---

<h2>🧪 Adaptive Cost Volume Pyramid Aggregation</h2>
<p>
Delve into the depths of encoding image features for multi-view feature volumes construction and cost volume aggregation.
</p>

<h3>Depth Hypotheses</h3>
<p>
We focus on encoding the extracted image features and the corresponding parameters into our network. A crucial part of this process is depth hypotheses sampling in 3D space:
</p>
\[
d_l = d_{\text{min},l} + m\frac{d_{\text{max},l} - d_{\text{min},l}}{M_l-1}
\]
<!-- ... Rest of the content ... -->

<h3>Efficient LCM</h3>
<p>
Efficiency is paramount, and our LCM also incorporates an efficient version:
</p>
\[
\mathbf{C}_l = \mathcal{M}(\mathbf{V}_{l,0}, \cdots, \mathbf{V}_{l,N}) = \text{AvgPool} ( \alpha_l \mathbf{B}_{l,0} \odot \sum\limits_{i=1}^{N}\frac{S_i}{\sum\limits_{i=1}^{N} S_i}\mathbf{B}_{l,i} )
\]

## Benchmark Performance
We benchmark our method on the DTU evaluation set and conduct a comprehensive comparison with traditional (geometric) and state-of-the-art learning-based MVS approaches. We follow the standard evaluation procedure~ for quantitative benchmark and summarize the mean error distance metrics (in $mm$, lower the better) including reconstruction accuracy, completeness, and overall score as shown in Table~. With different settings, including the changes of $N$ and $N_c$ (detailed in the Appendix), our method performs an excellent trade-off between the reconstruction accuracy and completeness. It achieves the best performance in terms of the accuracy, completeness and overall score compared with the existing traditional and learning-based methods, indicating the state-of-the-art performance of our method. We qualitatively compare the depth estimation and reconstruction results of several reflective and low-textured scenes with illumination changes on DTU evaluation set in Fig.~ and Fig.~ respectively, where our method achieves more complete depth estimation and dense point cloud reconstruction with fine-grained details preserved benefiting from the proposed LCM scheme, qualitatively verifying the quantitative comparison results.  [htbp!]  }   {!}{  {l l c c c}  \\[-3mm] {*}{Type} & {*}{Methods} & {c}{Mean Error...
<img src="/images/image/TNT-Compare-2.pdf"/>

---

## Real-World Application for UAV-Based Infrastructure Defect Inspection and Localization
As demonstrated in Fig.~, we deploy our MVS method into our UAV-based infrastructure defect inspection system for reconstruction-based defect localization, with crack as our target defect.  As shown in Fig.~ (a), three UAVs are used to speed up the image collection for defect detection and reconstruction of the target warehouse. Each UAV will reach the best region according to the task assignment method. After reaching the best region, viewpoints can be generated based on the building morphology. Furthermore, these viewpoints are regarded as the nodes of a traveling salesman problem to determine the shortest path that travels through all these viewpoints. Finally, the generated path will be executed by each UAV to collect the images for inspection and reconstruction. The multi-UAV-based data collection can speed up the overall image collection process by more than 3 times. [htbp!]%  [width=0.85]{image/defects.pdf}      Based on our UAS system, we collect $923$ images with crack defect from different directions of the target warehouse for defect detection. We train and compare the performance of the state-of-the-art object detection methods on our established defect...
<img src="/images/image/defects.pdf"/>


---

## Conclusion
We have presented the LCM-MVSNet for accurate and complete multi-view depth estimation and dense point cloud reconstruction, proposed the LCM scheme for adaptive cost volume aggregation, enhanced the shallow feature information flow to smooth depth estimation, and adapted the focal loss into the end-to-end MVS supervision to reduce ambiguity. The proposed MVS method has been extensively evaluated on three benchmark datasets and deployed into our UAV-based in- frastructure defect inspection system for reconstruction-based defect localization, demonstrating the effectiveness, efficiency, and scalability of our method.

<a href="https://youtube.com/watch?v=UJ3akL3gH68" target="_blank">
        <img src="https://s.ytimg.com/yts/img/favicon-vfl8qSV2F.ico" alt="YouTube logo" width="16" height="16">
        YouTube
    </a>
<iframe width="420" height="315"
src="https://www.youtube.com/embed/UJ3akL3gH68?autoplay=1&mute=1">
</iframe>

---

## Acknowledgements