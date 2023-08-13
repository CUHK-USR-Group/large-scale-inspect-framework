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
</h2>加上标
<div style=" text-align: center; font-size: 17px;">
Guidong Yang, Xunkuai Zhou, Chuanxiang Gao,  Xi Chen
, and <a href="http://www.mae.cuhk.edu.hk/~bmchen/">Ben M. Chen</a>, Fellow, IEEE
</div>
<div  style="text-align: center; font-size: 17px;" >
1. CUHK 2.TJ

</div>
<span style="display: flex; flex-direction: row; margin: 10px auto; justify-content: center"> 

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px;border: none; border-radius: 5px;"><a href="https://www.overleaf.com/project/64acc26ed265fde278ed8fb4" style="color: white; text-decoration: none;">Paper</a></button>

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px; border: none; border-radius: 5px;"><a href="/dataset" style="color: white; text-decoration: none;">Dataset</a></button>

<button style="background-color: #000000; color: white;margin-right: 15px; padding: 10px 15px; border: none; border-radius: 5px;"><a href="#detailed-section" style="color: white; text-decoration: none;">Supplementary</a></button>

</span>

<div style="text-align: center; font-family: 'American Typewriter'; font-weight: 400; "> 
<h2>Abstract</h2>
</div>
<div>

3D reconstruction is essential to defect localization. This paper proposes LCM-MVSNet, a novel multiview stereo (MVS) network with learnable cost metric (LCM) for more accurate and complete dense point cloud reconstruction. To adapt to the scene variation and improve the reconstruction quality in non-Lambertian low-textured scenes, we propose LCM to adaptively aggregate multiview matching similarity into the 3D cost volume by leveraging sparse point hints. The proposed LCM benefits the MVS approaches in four folds, including depth estimation enhancement, reconstruction quality improvement, memory footprint reduction, and computational burden alleviation, allowing the depth inference for high-resolution images to achieve more accurate and complete reconstruction. Additionally, we improve the depth estimation by enhancing the shallow feature propagation via a bottomup pathway and strengthen the end-to-end supervision by adapting the focal loss to reduce ambiguity caused by sample imbalance. Extensive experiments are carefully conducted on three benchmark datasets to validate that our method achieves state-of-the-art performance on the DTU and BlendedMVS dataset, and exhibits strong generalization ability with a competitive performance on the Tanks and Temples benchmark. Furthermore, we deploy our LCMMVSNet into our UAV-based infrastructure defect inspection system for reconstruction-based defect localization, demonstrating the effectiveness, efficiency, and scalability of our method. More experiment results can be found in the <a href="http://shorturl.at/xFRSU">Appendix</a>

</div>

---

<div style="font-size: 25px; text-align: center; font-family: 'American Typewriter'; font-weight: 800; ">    Comparison with the state of the arts
</div>
<h3>
Depth estimation performance on the <i>DTU</i> dataset</h3>
<div class="image-container" style="margin: 20px auto; text-align: center;">
        <img src="images/dtu_depth-2.pdf" alt="DTU depth comparison" width="85%">
        <p>Qualitative comparison of the depth map estimations on <em>Scan13</em> (1st row) and <em>Scan33</em> (2nd row) of the <em>DTU evaluation set</em>.</p>
</div>

----
<h3>
Reconstruction performance on the<i> DTU </i> dataset </h3>

<div class="image-container" style="margin: 20px auto;text-align: center;">
    <img src="images/dtu_points-5.pdf" alt="DTU depth comparison" width="85%">
    <p> The visualization of the reconstruction errors of the four scenes including <em> Family</em>, <em>Francis</em>, <em>Auditorium</em>, and <em>Courtroom </em> on the Tanks and Temples benchmark. ( \tau \) is the per-scene point distance threshold defined by the benchmark and darker color indicates a larger reconstruction error with respect to ( \tau \).</p>  
</div>
---

<h3>
Reconstruction performance on the<i> Tanks and Temples</i> dataset </h3>

<div class="image-container"  style="margin: 20px auto; text-align: center;">
    <img src="images/TNT-Compare-2.pdf" alt="DTU depth comparison" width="85%">
    <p> The visualization of the reconstruction errors of the four scenes including <em> Family</em>, <em>Francis</em>, <em>Auditorium</em>, and <em>Courtroom </em> on the Tanks and Temples benchmark. ( \tau \) is the per-scene point distance threshold defined by the benchmark and darker color indicates a larger reconstruction error with respect to ( \tau \).</p>  
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

<button style="background-color: #3498db; color: white; padding: 10px 15px; border: none; border-radius: 5px;"><a href="#detailed-section" style="color: white; text-decoration: none;">Explore Furth</h3>er</a></button>

<img src="/images/image/Framework.pdf"/>

---

<h2>📐 Methodology of Multi-View Stereo (MVS)</h2>
<hr>
<p>Discover the intricacies of our innovative two-stage MVS method, the <strong>LCM-MVSNet</strong>. Delving deep into automated point cloud reconstruction, this section unveils the techniques and strategies behind our state-of-the-art system.</p>

<figure>
  <img src="/images/network.pdf" alt="Overview of LCM-MVSNet" style="width:100%; border: 1px solid #ddd; border-radius: 4px; padding: 5px;">
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
d_l = d_{min,l} + m\frac{d_{max,l} d_{min,l}}{M_l-1}
$$

<p>Where \( d_{min,l} \) and \( d_{max,l} \) represent the minimum and maximum depth at level \( l \), respectively. The homography matrix \( \textbf{H}_{i}(d_l) \) between the \( i_{th} \) source-view feature map and reference feature map at depth \( d_l \) is defined as:</p>

$$
\textbf{H}_{i}(d_l) = \textbf{K}_{i}\textbf{R}_{i}(\textbf{I}-\frac{(\textbf{C}_{0} \textbf{C}_i)\textbf{n}_{0}^T}{d_l})\textbf{R}_{0}^{T}(\textbf{K}_{0})^{-1}
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
$$
d_l = d_{\text{min},l} + m\frac{d_{\text{max},l} d_{\text{min},l}}{M_l-1}
$$
<!-... Rest of the content ... -->

<h3><strong>Efficient LCM</strong></h3>
<p>The <i>efficient LCM</i> at network level \( l \) is defined as follows:</p>

$$
\begin{aligned}
\textbf{C}_l &= \mathcal{M}(\textbf{V}_{l,0}, \cdots, \textbf{V}_{l,N})\\
&= \mathcal{M}(\textbf{B}_{l,0}, \cdots, \textbf{B}_{l,N})\\
&= AvgPool \left( \alpha_l \textbf{B}_{l,0} \odot \sum\limits_{i=1}^{N}\frac{S_i}{\sum\limits_{i=1}^{N} S_i}\textbf{B}_{l,i} \right)
\end{aligned}
$$

<p>Where \( \textbf{B}_{l,i} \) stands for the batched volumes after evenly separating the original volumes \( \textbf{V}_{l,i} \) into \( K \) batches along the channel dimension. ...</p>

<!-Continue with the rest of the provided content, converting LaTeX to KaTeX notation -->

<h3>Cost Volume Regularization and Depth Estimation</h3>
<p>Following recent learning-based MVS methods, a four-scale 3D CNN is adopted ...</p>

$$
\textbf{D}_l = \underset{d_l \in [d_{min,l}, d_{max,l}]}{\argmax} \ \textbf{P}_{l,est}(d_l) + \frac{(d_{max,l} d_{min,l})}{M_l-1} \max \textbf{P}_{l,est}(d_l)
$$

<!-Continue with the rest of the provided content -->

<h3>Loss Function</h3>
<p>Most recent learning-based MVS approaches use \( L1 \) loss to minimize ...</p>

$$
\begin{aligned}
\mathcal{L}_l = \sum\limits_{\textbf{x} \in \{\textbf{x}_{valid}\}} \beta_l |\textbf{P}_{l,gt}(\textbf{x}) \textbf{P}_{l,est}(\textbf{x})|^{\gamma_l} \cdot \\
((1-\textbf{P}_{l,gt}(\textbf{x}))\log(1-\textbf{P}_{l,est}(\textbf{x})) + \textbf{P}_{l,gt}(\textbf{x})\log(\textbf{P}_{l,est}(\textbf{x})))
\end{aligned}
$$

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
    <img src="images/dtu_depth-2.pdf" alt="DTU depth comparison" width="85%">
    <p>Qualitative comparison of the depth map estimations on <em>Scan13</em> (1st row) and <em>Scan33</em> (2nd row) of the <em>DTU evaluation set</em>.</p>
</div>

<div class="image-container">
    <img src="images/dtu_points-5.pdf" alt="DTU points comparison" width="85%">
    <p>Qualitative comparison of the point cloud reconstruction of <em>Scan12</em> (1st row), <em>Scan13</em> (2nd row) and <em>Scan77</em> (3rd row) on the <em>DTU evaluation set</em>.</p>
</div>
<div style="margin: 30px auto; text-align: center;">
<div class="sketchfab-embed-wrapper"> <iframe style=" height: 600px;" title="(Not GOODMAN) Procedural Hong Kong building" frameborder="0" allowfullscreen mozallowfullscreen="true" webkitallowfullscreen="true" allow="autoplay; fullscreen; xr-spatial-tracking" xr-spatial-tracking execution-while-out-of-viewport execution-while-not-rendered web-share src="https://sketchfab.com/models/528a732e84c44fd49c4726f341014a23/embed"> </iframe> <p style="font-size: 17px; font-weight: normal; margin: 5px; color: #4A4A4A;"> <a href="https://sketchfab.com/3d-models/procedural-hong-kong-building-528a732e84c44fd49c4726f341014a23?utm_medium=embed&utm_campaign=share-popup&utm_content=528a732e84c44fd49c4726f341014a23" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;"> Procedural Hong Kong building </a> by <a href="https://sketchfab.com/udayjeet?utm_medium=embed&utm_campaign=share-popup&utm_content=528a732e84c44fd49c4726f341014a23" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;"> uday </a> on <a href="https://sketchfab.com?utm_medium=embed&utm_campaign=share-popup&utm_content=528a732e84c44fd49c4726f341014a23" target="_blank" rel="nofollow" style="font-weight: bold; color: #1CAAD9;">Sketchfab</a></p></div>
</div>
<h3>Benchmark Performance</h3>
<p><strong>Benchmark on DTU Dataset:</strong> We benchmark our method on the <em>DTU evaluation set</em> and conduct a comprehensive comparison with traditional (geometric) and cutting-edge learning-based MVS strategies. We follow the standard evaluation procedure for quantitative benchmarking and summarize the <em>mean error distance</em> metrics (in mm, lower is better) including reconstruction <em>accuracy</em>, <em>completeness</em>, and <em>overall score</em>.</p>

<!-The table content would go here. Due to the extensive nature of the table, I'll provide a basic structure as an example. -->

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
        <!-Geometric Methods -->
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

        <!-Learning Methods -->
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
        <!-... following the same pattern for other learning methods ... -->
        <tr>
            <td>TransMVSNet<sup>†</sup></td>
            <td>0.360</td>
            <td>0.271</td>
            <td>0.316</td>
        </tr>

        <!-Ours -->
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
<!-And so on for the other datasets and tables -->

<p><strong>Benchmark on Tanks and Temples Dataset:</strong> We benchmark our method on both the <em>intermediate set</em> and the <em>advanced set</em> of the <em>Tanks and Temples</em> benchmark...</p>

<!-The corresponding table content and other datasets would follow -->

<h2>Ablation Study</h2>
<p id="subsec: ablation">
In this section, we conduct systematic ablation experiments to analyze the effectiveness and efficiency of each component of our method. All the ablation experiments are conducted on the <em>DTU evaluation set</em>. Please see more ablation studies (BPA, experimental settings, memory, and runtime) in the <strong>Appendix</strong>.
</p>

<h3>Bottom-up Path Augmentation</h3>
<p>
As aforementioned, we introduce the BPA to augment the propagation of low-level features and incorporate more context information for robust feature matching and continuous depth estimation. As shown in the table below, the <em>Baseline</em> model references <a href="#CasMVSNet">[CasMVSNet]</a> and applies FPN for feature extraction, the heuristic variance-based scheme for cost volume aggregation, and \(L1\) loss for optimization. Benefiting from BPA, <em>Model A</em> addresses the over-smoothing depth estimation around the object boundary and achieves significant improvement on the reconstruction <em>completeness</em> (0.370 → 0.344) and <em>overall score</em> (0.367 → 0.354).
</p>

<figure>
    <img src="images/depth_curve.pdf" alt="Comparison of mean absolute depth error" width="85%">
    <figcaption>Comparison of <em>mean absolute depth error</em> by proposed LCM modules for cost volume aggregation (a) during training on the <em>DTU training set</em>; (b) during validation on the <em>DTU validation set</em>.</figcaption>
</figure>

<h3>LCM Modules and Adapted Focal Loss</h3>
<p>
Based on <em>Model A</em>, we adopt the proposed <em>coarse-to-fine LCM</em> (<em>Model B</em>), <em>efficient LCM</em> (<em>Model C</em>) to adaptively fuse multi-view feature volumes into the cost volume. The above figure (a) and (b) show the descent curve of the mean absolute depth error by different cost volume aggregation modules on the <em>DTU training</em> and <em>validation set</em>, respectively, demonstrating that the models with LCM modules produce more accurate depth estimations. The quantitative ablation results on the <em>DTU evaluation set</em> shown in the table below further verify that both  LCM modules effectively improve the reconstruction <em>accuracy</em>, <em>completeness</em>, and <em>overall score</em> by a large margin. Notably, the adapted focal loss significantly boosts the reconstruction quality in terms of <em>completeness</em> and <em>overall score</em> to the state-of-the-art performance (<em>Model D</em> and <em>Model E</em>).
</p>

<table class="benchmark-table" style=" width:80%; margin:auto; border-collapse: collapse;">
    <caption>Ablation Experiments on Different Components of Proposed Method (\(N=5\), \(W\times H=1152\times864\), \(\tau=0.3\), and \(N_c=3\))</caption>
    <thead>
        <tr>
            <th rowspan="2">Models</th>
            <th colspan="2">Feature Extraction</th>
            <th colspan="4">Cost Volume Aggregation</th>
            <th colspan="2">Loss Function</th>
            <th colspan="3">Mean Error Distance \(\downarrow\) (mm)</th>
        </tr>
        <tr>
            <th>FPN</th>
            <th>FPN+BPA</th>
            <th>Variance</th>
            <th>AA</th>
            <th>C-LCM</th>
            <th>E-LCM</th>
            <th>L1</th>
            <th>Focal</th>
            <th>Acc.</th>
            <th>Comp.</th>
            <th>Overall</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Baseline</td>
            <td>✓</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td>0.364</td>
            <td>0.370</td>
            <td>0.367</td>
        </tr>
        <tr>
            <td>Model A</td>
            <td></td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td>0.364</td>
            <td>0.344</td>
            <td>0.354</td>
        </tr>
        <tr>
            <td>Model B</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td>0.355</td>
            <td>0.335</td>
            <td>0.345</td>
        </tr>
        <tr>
            <td>Model C</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td>✓</td>
            <td></td>
            <td><strong>0.348</strong></td>
            <td>0.331</td>
            <td>0.340</td>
        </tr>
        <tr>
            <td>Model D</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td>0.358</td>
            <td>0.275</td>
            <td><strong>0.317</strong></td>
        </tr>
        <tr>
            <td>Model E</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td>✓</td>
            <td>0.362</td>
            <td><strong>0.274</strong></td>
            <td>0.318</td>
        </tr>
        <tr>
            <td>Model G</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td>0.356</td>
            <td>0.334</td>
            <td>0.345</td>
        </tr>
        <tr>
            <td>Model H</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td>✓</td>
            <td></td>
            <td></td>
            <td></td>
            <td>✓</td>
            <td>0.364</td>
            <td>0.279</td>
            <td>0.321</td>
        </tr>
    </tbody>
</table>

<h3>Comparison with Adaptive Aggregation Module</h3>
<p>
We compare the proposed LCM modules with adaptive aggregation (AA) module references <a href="#AA-RMVSNet">[AA-RMVSNet]</a>, <a href="#Uni-MVSNet">[Uni-MVSNet]</a> (<em>Model G</em> and <em>Model H</em> as shown in the table below) adopting an additional re-weight network to compute the weight for each feature volume. The results show that our <em>coarse-to-fine LCM</em> (<em>Model B, D</em>) and <em>efficient LCM</em> (<em>Model C, E</em>) outperforms AA in terms of reconstruction <em>accuracy</em>, <em>completeness</em>, and <em>overall score</em>.
</p>

<h2>Real-World Application for UAV-Based Infrastructure Defect Inspection and Localization</h2>
<p id="sec: uav">
As demonstrated in the figure below, we deploy our MVS method into our UAV-based infrastructure defect inspection system for reconstruction-based defect localization, with crack as our target defect.
</p>

<!-The rest of the content, including figures and tables, will follow in a similar format. -->

<!-Conclusion Section -->
<section>
    <h2>Conclusion</h2>
    <p>
        We have presented the LCM-MVSNet for accurate and complete multi-view depth estimation and dense point cloud reconstruction, proposed the LCM scheme for adaptive cost volume aggregation, enhanced the shallow feature information flow to smooth depth estimation, and adapted the focal loss into the end-to-end MVS supervision to reduce ambiguity. The proposed MVS method has been extensively evaluated on three benchmark datasets and deployed into our UAV-based infrastructure defect inspection system for reconstruction-based defect localization, demonstrating the effectiveness, efficiency, and scalability of our method.
    </p>
</section>

<!-References (Not included in LaTeX snippet, placeholder for now) -->
<section>
    <h2>References</h2>
<ol>
    <li>Y. Yao, Z. Luo, S. Li, T. Fang, and L. Quan, “Mvsnet: Depth inference for unstructured multi-view stereo,” in <i>Proceedings of the European Conference on Computer Vision (ECCV)</i>, Sep. 2018.</li>
    <li>Y.Yao, Z.Luo, S.Li, T.Shen, T.Fang, and L.Quan, “Recurrentmvsnet for high-resolution multi-view stereo depth inference,” in <i>Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)</i>, Jun. 2019.</li>
    <li>X. Gu, Z. Fan, S. Zhu, Z. Dai, F. Tan, and P. Tan, “Cascade cost volume for high-resolution multi-view stereo and stereo matching,” in <i>Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition</i>, pp. 2495–2504, 2020.</li>
    <li>J. Zhang, S. Li, Z. Luo, T. Fang, and Y. Yao, “Vis-mvsnet: Visibility-aware multi-view stereo network,” <i>International Journal of Computer Vision</i>, pp. 1–16, 2022.</li>
    <li>Z. Wei, Q. Zhu, C. Min, Y. Chen, and G. Wang, “Aa-rmvsnet: Adaptive aggregation recurrent multi-view stereo network,” in <i>Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)</i>, pp. 6187–6196, Oct. 2021.</li>
    <li>X. Ma, Y. Gong, Q. Wang, J. Huang, L. Chen, and F. Yu, “Epp-mvsnet: Epipolar-assembling based depth prediction for multi-view stereo,” in <i>Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)</i>, pp. 5732–5740, Oct. 2021.</li>
    <li>K. T. Giang, S. Song, and S. Jo, “Curvature-guided dynamic scale networks for multi-view stereo,” <i>arXiv preprint arXiv:2112.05999</i>, 2021.</li>
        <li>R. Peng, R. Wang, Z. Wang, Y. Lai, and R. Wang, “Rethinking depth estimation for multi-view stereo: A unified representation,” in <i>Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)</i>, pp. 8645–8654, Jun. 2022.</li>
    <li>Y. Ding, W. Yuan, Q. Zhu, H. Zhang, X. Liu, Y. Wang, and X. Liu, “Transmvsnet: Global context-aware multi-view stereo network with transformers,” in <i>Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)</i>, pp. 8585–8594, Jun. 2022.</li>
    <li>H. Aanæs, R. R. Jensen, G. Vogiatzis, E. Tola, and A. B. Dahl, “Large-scale data for multiple-view stereopsis,” <i>International Journal of Computer Vision</i>, vol. 120, no. 2, pp. 153–168, 2016.</li>
    <li>H. Yi, Z. Wei, M. Ding, R. Zhang, Y. Chen, G. Wang, and Y.-W. Tai, “Pyramid multi-view stereo net with self-adaptive view aggregation,” in <i>European Conference on Computer Vision</i>, pp. 766–782. Springer, 2020.</li>
    <li>J. Yan, Z. Wei, H. Yi, M. Ding, R. Zhang, Y. Chen, G. Wang, and Y.-W. Tai, “Dense hybrid recurrent multi-view stereo net with dynamic consistency checking,” in <i>European conference on computer vision</i>, pp. 674–689. Springer, 2020.</li>
    <li>Z. Wei, Q. Zhu, C. Min, Y. Chen, and G. Wang, “Bidirectional hybrid lstm based recurrent neural network for multi-view stereo,” <i>IEEE Transactions on Visualization and Computer Graphics</i>, DOI 10.1109/TVCG.2022.3165860, pp. 1–1, 2022.</li>
    <li>T.-Y. Lin, P. Goyal, R. Girshick, K. He, and P. Dolla ́r, “Focal loss for dense object detection,” in <i>Proceedings of the IEEE international conference on computer vision</i>, pp. 2980–2988, 2017.</li>
    <li>X. Li, W. Wang, L. Wu, S. Chen, X. Hu, J. Li, J. Tang, and J. Yang, “Generalized focal loss: Learning qualified and distributed bounding boxes for dense object detection,” <i>Advances in Neural Information Processing Systems</i>, vol. 33, pp. 21 002–21 012, 2020.</li>
    <li>Y. Chen, S. Lai, J. Cui, B. Wang, and B. M. Chen, “Gpu-accelerated incremental euclidean distance transform for online motion planning of mobile robots,” <i>IEEE Robotics and Automation Letters</i>, vol. 7, DOI 10.1109/LRA.2022.3177852, no. 3, pp. 6894–6901, 2022.</li>
    <li>K. Liu and B. M. Chen, “Industrial uav-based unsupervised domain adaptive crack recognitions: From database towards real-site infrastructural inspections,” <i>IEEE Transactions on Industrial Electronics</i>, vol. 70, DOI 10.1109/TIE.2022.3204953, no. 9, pp. 9410–9420, 2023.</li>
    <li>S. Liu, L. Qi, H. Qin, J. Shi, and J. Jia, “Path aggregation network for instance segmentation,” in <i>Proceedings of the IEEE conference on computer vision and pattern recognition</i>, pp. 8759–8768, 2018.</li>
    <li>S. R. Bulo, L. Porzi, and P. Kontschieder, “In-place activated batchnorm for memory-optimized training of dnns,” in <i>Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition</i>, pp. 5639–5647, 2018.</li>
    <li>Y.Furukawa and J.Ponce, “Accurate, dense, and robust multi-view stereopsis,” <i>IEEE Transactions on Pattern Analysis and Machine Intelligence</i>, vol. 32, DOI 10.1109/TPAMI.2009.161, no. 8, pp. 1362–1376, 2010.</li>
    <li>E. Tola, C. Strecha, and P. Fua, “Efficient large-scale multi-view stereo for ultra high-resolution image sets,” <i>Machine Vision and Applications</i>, vol. 23, no. 5, pp. 903–920, 2012.</li>
    <li>N. D. Campbell, G. Vogiatzis, C. Herna ́ndez, and R. Cipolla, “Using multiple hypotheses to improve depth-maps for multi-view stereo,” in <i>European Conference on Computer Vision</i>, pp. 766–779. Springer, 2008.</li>
    <li>S.Galliani, K.Lasinger, and K.Schindler, “Massively parallel multi-view stereopsis by surface normal diffusion,” in <i>2015 IEEE International Conference on Computer Vision (ICCV)</i>, DOI 10.1109/ICCV.2015.106, pp. 873–881, 2015.</li>
    <li>J.L.Schö ̈nberger and J.-M.Frahm, “Structure-from-motion revisited,” in <i>2016 IEEE Conference on Computer Vision and Pattern Recognition (CVPR)</i>, DOI 10.1109/CVPR.2016.445, pp. 4104–4113, 2016.</li>
    <li>J. L. Schönberger, E. Zheng, M. Pollefeys, and J.-M. Frahm, “Pixel-wise view selection for unstructured multi-view stereo,” in <i>European Conference on Computer Vision (ECCV)</i>, 2016.</li>
    <li>M.Ji, J.Gall, H.Zheng, Y.Liu, and L.Fang, “Surfacenet: An end-to-end 3d neural network for multiview stereopsis,” in <i>2017 IEEE International Conference on Computer Vision (ICCV)</i>, DOI 10.1109/ICCV.2017.253, pp. 2326–2334, 2017.</li>
    <li>R. Chen, S. Han, J. Xu, and H. Su, “Point-based multi-view stereo network,” in <i>Proceedings of the IEEE/CVF international conference on computer vision</i>, pp. 1538–1547, 2019.</li>
    <li>Z. Yu and S. Gao, “Fast-mvsnet: Sparse-to-dense multi-view stereo with learned propagation and gauss-newton refinement,” in <i>Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)</i>, Jun. 2020.</li>
    <li>F. Wang, S. Galliani, C. Vogel, P. Speciale, and M. Pollefeys, “Patch-matchnet: Learned multi-view patchmatch stereo,” in <i>Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)</i>, pp. 14,194–14,203, Jun. 2021.</li>
    <li>J. Yang, W. Mao, J. M. Alvarez, and M. Liu, “Cost volume pyramid based depth inference for multi-view stereo,” in <i>Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition</i>, pp. 4877–4886, 2020.</li>
    <li>F. Wang, S. Galliani, C. Vogel, and M. Pollefeys, “Itermvs: Iterative probability estimation for efficient multi-view stereo,” in <i>Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition</i>, pp. 8606–8615, 2022.</li>
    <li>G. Yang, K. Liu, J. Zhang, B. Zhao, Z. Zhao, X. Chen, and B. M. Chen, “Datasets and processing methods for boosting visual inspection of civil infrastructure: A comprehensive review and algorithm comparison for crack classification, segmentation, and detection,” <i>Construction and Building Materials</i>, vol. 356, DOI <a href="https://doi.org/10.1016/j.conbuildmat.2022.129226">https://doi.org/10.1016/j.conbuildmat.2022.129226</a>, p. 129226, 2022. <a href="https://www.sciencedirect.com/science/article/pii/S0950061822028823">Online Available</a></li>
</ol>


</section>

<!-Author Biographies -->
<section>
    <h2>Author Biographies</h2>

    <figure>
        <img src="Authors_pic/Guidong.jpg" alt="Guidong Yang" width="100" height="125">
        <figcaption>
            <strong>Guidong Yang</strong> received the B.Eng. degree from Shanghai Jiao Tong University (SJTU), Shanghai, China, in 2018, the M.Eng. degree from SJTU and M.Sc. degree from Polytecnic University of Milan, Milan, Italy, in 2021. He is currently pursuing his Ph.D. degree in mechanical and automation engineering, The Chinese University of Hong Kong, Hong Kong, China. His current research interests include object detection and 3D reconstruction.
        </figcaption>
    </figure>

    <figure>
        <img src="Authors_pic/xunkuai.jpg" alt="Xunkuai Zhou" width="100" height="125">
        <figcaption>
            <strong>Xunkuai Zhou</strong> is currently pursuing his Ph.D. degree in control science and engineering, Tongji University, Shanghai, China. He is currently involved in research works as a visiting Ph.D. student with the Department of Mechanical and Automation, The Chinese University of Hong Kong, Hong Kong, China. His current research interests include model compression, object detection, object tracking and 3D reconstruction.
        </figcaption>
    </figure>

    <figure>
        <img src="Authors_pic/chuanxiang.jpeg" alt="Chuanxiang Gao" width="100" height="125">
        <figcaption>
            <strong>Chuanxiang Gao</strong> received the B.Eng. degree from Northwestern Polytechnical University (NWPU), Xian, China, in 2020. He is currently pursing his Ph.D. degree in mechanical and automation engineering, The Chinese University of Hong Kong, Hong Kong, China. His current research interests include task planning and motion planning.
        </figcaption>
    </figure>

    <figure>
        <img src="Authors_pic/Prof. Patrick.jpeg" alt="Xi Chen" width="100" height="125">
        <figcaption>
            <strong>Xi Chen</strong> is now a Research Assistant Professor in the Chinese University of Hong Kong. He has over 10-year experience in sustainable building technology related to the urban energy systems, renewable application in buildings and built environment modelling, and has led or managed multiple research projects including ARC, MOST, RGC and consultancy projects with the local government and industry. He has published over 40 papers in peer-reviewed international journals and coauthored a book in green building and renewable application areas.

            Dr. Chen has been awarded the DECRA Fellow in the Australian Research Council and Fulbright Scholar in the Lawrence Berkeley National Laboratory. In addition, he services as the editorial board member of Buildings, Energies and Advances in Applied Energy.
        </figcaption>
    </figure>

    <figure>
        <img src="Authors_pic/Prof.chen" alt="Ben M. Chen" width="100" height="125">
        <figcaption>
            <strong>Ben M. Chen</strong> (Fellow, IEEE) is currently a Professor of mechanical and automation engineering with the Chinese University of Hong Kong (CUHK), Hong Kong. He was a Provost's Chair Professor with the Department of Electrical and Computer Engineering, National University of Singapore (NUS), before joining CUHK, in 2018. He was an Assistant Professor with the Department of Electrical Engineering, State University of New York at Stony Brook, NY, USA, from 1992 to 1993. He has authored/co-authored hundreds of journal and conference articles, and a dozen research monographs in control theory and applications, unmanned systems and financial market modeling. His current research interests are in unmanned systems and their applications.

            Dr. Chen is a Fellow of IEEE and Fellow of Academy of Engineering, Singapore. He had served on the editorial boards of a dozen international journals including Automatica and IEEE TRANSACTIONS ON AUTOMATIC CONTROL. He is currently serving as an Editor-in-Chief of Unmanned Systems, and Editor of International Journal of Robust and Nonlinear Control.
        </figcaption>
    </figure>
</section>


## Acknowledgements

This work was supported in part by the InnoHK of 1056 the Government of the Hong Kong Special Administrative 1057 Region via the Hong Kong Centre for Logistics Robotics 1058 and in part by the Research Grants Council of Hong Kong 1059 SAR (Grant No: 14209020 and Grant No: 14206821).