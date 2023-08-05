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



<h1 style="font-size: 50px; font-family: 'Sama Devanagari';"> Learnable Cost Metric Based Multi-View Stereo for Point Cloud Reconstruction
</h1>

## Authors

 <a href="https://orcid.org/0000" target="_blank">
        <img src="https://orcid.org/sites/default/files/images/orcid_16x16(1).gif" alt="ORCID logo">
        Guidong Yang
</a>
 , Xunkuai Zhou, Chuanxiang Gao,  <a href="https://orcid.org/0009-0003-2940-8499" target="_blank">
        <img src="https://orcid.org/sites/default/files/images/orcid_16x16(1).gif" alt="ORCID logo">
        
</a> <a href="https://orcid.org/0000-0003-2168-9057" target="_blank">
        <img src="https://orcid.org/sites/default/files/images/orcid_16x16(1).gif" alt="ORCID logo">
        Xi Chen
</a>, and Ben M. Chen, Fellow, IEEE

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

<p>For the math enthusiasts out there, let's dive into the formulas. Our network, for level \( l \), uniformly samples \( M_l \)-layer depth hypotheses in 3D space from the depth range \( [d_{min,l}, d_{max, l}] \) for the reference camera frustum. The depth calculation is given by:</p>

$$
d_l = d_{min,l} + m\frac{d_{max,l} - d_{min,l}}{M_l-1}
$$

<p>Where \( d_{min,l} \) and \( d_{max,l} \) represent the minimum and maximum depth at level \( l \), respectively. The homography matrix \( \textbf{H}_{i}(d_l) \) between the \( i_{th} \) source-view feature map and reference feature map at depth \( d_l \) is defined as:</p>

$$
\textbf{H}_{i}(d_l) = \textbf{K}_{i}\textbf{R}_{i}(\textbf{I}-\frac{(\textbf{C}_{0} - \textbf{C}_i)\textbf{n}_{0}^T}{d_l})\textbf{R}_{0}^{T}(\textbf{K}_{0})^{-1}
$$

<p>... and so on with more math content as needed.</p>

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

<h3><strong>Efficient LCM</strong></h3>
<p>The <i>efficient LCM</i> at network level \( l \) is defined as follows:</p>

\[
\begin{aligned}
\textbf{C}_l &= \mathcal{M}(\textbf{V}_{l,0}, \cdots, \textbf{V}_{l,N})\\
&= \mathcal{M}(\textbf{B}_{l,0}, \cdots, \textbf{B}_{l,N})\\
&= AvgPool \left( \alpha_l \textbf{B}_{l,0} \odot \sum\limits_{i=1}^{N}\frac{S_i}{\sum\limits_{i=1}^{N} S_i}\textbf{B}_{l,i} \right)
\end{aligned}
\]

<p>Where \( \textbf{B}_{l,i} \) stands for the batched volumes after evenly separating the original volumes \( \textbf{V}_{l,i} \) into \( K \) batches along the channel dimension. ...</p>

<!-- Continue with the rest of the provided content, converting LaTeX to KaTeX notation -->

<h3>Cost Volume Regularization and Depth Estimation</h3>
<p>Following recent learning-based MVS methods, a four-scale 3D CNN is adopted ...</p>

\[
\textbf{D}_l = \underset{d_l \in [d_{min,l}, d_{max,l}]}{\argmax} \ \textbf{P}_{l,est}(d_l) + \frac{(d_{max,l} - d_{min,l})}{M_l-1} \max \textbf{P}_{l,est}(d_l)
\]

<!-- Continue with the rest of the provided content -->

<h3>Loss Function</h3>
<p>Most recent learning-based MVS approaches use \( L1 \) loss to minimize ...</p>

\[
\begin{aligned}
\mathcal{L}_l = \sum\limits_{\textbf{x} \in \{\textbf{x}_{valid}\}} - \beta_l |\textbf{P}_{l,gt}(\textbf{x}) - \textbf{P}_{l,est}(\textbf{x})|^{\gamma_l} \cdot \\
((1-\textbf{P}_{l,gt}(\textbf{x}))\log(1-\textbf{P}_{l,est}(\textbf{x})) + \textbf{P}_{l,gt}(\textbf{x})\log(\textbf{P}_{l,est}(\textbf{x})))
\end{aligned}
\]

<h3>🔍 <strong>Depth Maps Filtering and Fusion</strong></h3>
<hr>
<p>Depth maps filtering and fusion form a critical juncture in our methodology. These processes are pivotal for coalescing the estimated multi-view depth maps \( \{\textbf{D}_i\}_{i=0}^{N} \) into the ultimate 3D point cloud. Here's how we achieve precision:</p>

<div style="background-color: #f9f9f9; padding: 15px; margin: 20px 0; border-left: 5px solid #3498db;">
  <strong>For Depth Map Filtering:</strong> We harness both photometric and geometric constraints to ensure impeccable accuracy:
  <ul>
    <li>We set a probability threshold \( \tau \) to systematically discard depth outliers, ensuring only the most accurate depth maps remain.</li>
    <li>We also introduce the number of consistent views \( N_{c} \) to drastically minimize depth inconsistency.</li>
    <li>The photometric constraint gauges the multi-view matching quality, while the geometric constraint underscores multi-view depth consistency.</li>
  </ul>
</div>

<p>After this rigorous filtering process, we then fuse the meticulously estimated depth maps into the final 3D point cloud, using techniques inspired by previous works.</p>

<p><a href="#next-section" style="color: #3498db; text-decoration: none;">On to the next phase ➡️</a></p>

---
<h2>📊 Experiments on the Benchmark Datasets</h2>
<hr>
<p>In this section, we showcase the effectiveness and superiority of our LCM-MVSNet across multiple MVS benchmarks. The datasets, evaluation metrics, training & evaluation specifics, and all reconstruction visualizations can be found in the <strong>Appendix</strong> due to page constraints.</p>

<div class="image-container">
    <img src="image/dtu_depth-2.pdf" alt="DTU depth comparison" width="85%">
    <p>Qualitative comparison of the depth map estimations on <em>Scan13</em> (1st row) and <em>Scan33</em> (2nd row) of the <em>DTU evaluation set</em>.</p>
</div>

<div class="image-container">
    <img src="image/dtu_points-5.pdf" alt="DTU points comparison" width="85%">
    <p>Qualitative comparison of the point cloud reconstruction of <em>Scan12</em> (1st row), <em>Scan13</em> (2nd row) and <em>Scan77</em> (3rd row) on the <em>DTU evaluation set</em>.</p>
</div>

<h3>Benchmark Performance</h3>
<p><strong>Benchmark on DTU Dataset:</strong> We benchmark our method on the <em>DTU evaluation set</em> and conduct a comprehensive comparison with traditional (geometric) and cutting-edge learning-based MVS strategies. We follow the standard evaluation procedure for quantitative benchmarking and summarize the <em>mean error distance</em> metrics (in mm, lower is better) including reconstruction <em>accuracy</em>, <em>completeness</em>, and <em>overall score</em>.</p>

<!-- The table content would go here. Due to the extensive nature of the table, I'll provide a basic structure as an example. -->

<table class="benchmark-table">
    <caption>Quantitative Benchmarking Results on <em>DTU Evaluation Set</em></caption>
    <thead>
        <tr>
            <th>Type</th>
            <th>Methods</th>
            <th>ACC. ↓ (mm)</th>
            <th>Comp. ↓ (mm)</th>
            <th>Overall ↓ (mm)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan="5">Geometric</td>
            <td>Furu</td>
            <td>0.613</td>
            <td>0.941</td>
            <td>0.777</td>
        </tr>
        <tr>
            <td>Tola</td>
            <td>0.342</td>
            <td>1.190</td>
            <td>0.766</td>
        </tr>
        <tr>
            <td>Camp</td>
            <td>0.835</td>
            <td>0.554</td>
            <td>0.695</td>
        </tr>
        <tr>
            <td>Gipuma</td>
            <td>0.283</td>
            <td>0.873</td>
            <td>0.578</td>
        </tr>
        <tr>
            <td>Colmap</td>
            <td>0.400</td>
            <td>0.664</td>
            <td>0.532</td>
        </tr>

        <!-- Learning Methods -->
        <tr>
            <td rowspan="24">Learning</td>
            <td>SurfaceNet</td>
            <td>0.450</td>
            <td>1.040</td>
            <td>0.745</td>
        </tr>
        <tr>
            <td>MVSNet</td>
            <td>0.396</td>
            <td>0.527</td>
            <td>0.462</td>
        </tr>
        <!-- ... following the same pattern for other learning methods ... -->
        <tr>
            <td>TransMVSNet<sup>†</sup></td>
            <td>0.360</td>
            <td>0.271</td>
            <td>0.316</td>
        </tr>

        <!-- Ours -->
        <tr>
            <td rowspan="5"><strong>Ours</strong></td>
            <td>Ours (N=5, N<sub>c</sub>=6)</td>
            <td><strong>0.263</strong></td>
            <td>0.539</td>
            <td>0.401</td>
        </tr>
        <tr>
            <td>Ours (N=5, N<sub>c</sub>=5)</td>
            <td>0.285</td>
            <td>0.427</td>
            <td>0.356</td>
        </tr>
        <tr>
            <td>Ours (N=7, N<sub>c</sub>=4)</td>
            <td>0.317</td>
            <td>0.323</td>
            <td>0.320</td>
        </tr>
        <tr>
            <td>Ours (N=5, N<sub>c</sub>=3)</td>
            <td>0.368</td>
            <td>0.263</td>
            <td>0.315</td>
        </tr>
        <tr>
            <td>Ours (N=7, N<sub>c</sub>=3)</td>
            <td>0.364</td>
            <td><strong>0.262</strong></td>
            <td><strong>0.313</strong></td>
        </tr>
    </tbody>
</table>

<style>
.benchmark-table {
    width: 100%;
    border-collapse: collapse;
    margin: 25px 0;
    font-size: 16px;
    text-align: left;
}

.benchmark-table th, .benchmark-table td {
padding: 8px 12px;
border-bottom: 1px solid #ddd;
}

.benchmark-table tbody tr:hover {
background-color: #f5f5f5;
}

.benchmark-table th {
background-color: #f2f2f2;
}

</style>
<!-- And so on for the other datasets and tables -->

<p><strong>Benchmark on Tanks and Temples Dataset:</strong> We benchmark our method on both the <em>intermediate set</em> and the <em>advanced set</em> of the <em>Tanks and Temples</em> benchmark...</p>

<!-- The corresponding table content and other datasets would follow -->


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