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

---

## Introduction
\IEEEPARstart{M}{ulti-View} stereo (MVS) aims to recover the dense 3D representation of the scene leveraging stereo correspondences as the main cue given calibrated 2D images from multiple views (more than two views), essentially equivalent to solving the pixel correspondences across multi-view images. Recently, learning-based MVS approaches~\cite{MVSNet, R-MVSNet, CasMVSNet, Vis-MVSNet, AA-RMVSNet, EPP-MVSNet, CDS-MVSNet, Uni-MVSNet, TransMVSNet} have significantly outperformed the traditional counterparts in MVS benchmarks~\cite{DTU_dataset, Tanks_dataset, ETH3D, BlendedMVS}. Deep MVS approaches decouple the MVS into a two-stage process: \textit{learning-based depth map estimation} and \textit{depth map filtering \& fusion}. Compared to the hand-crafted photometric measures in traditional approaches, deep MVS approaches encode scene cues such as reflective priors and illumination changes into the network by adopting powerful feature extraction and cost volume representation to achieve superior reconstruction accuracy and completeness. Despite the superiority of the learning-based MVS approaches, the following improvements can be made to further boost the overall reconstruction quality: Most recent learning-based methods~\cite{CasMVSNet, UCS-Net, Uni-MVSNet} use feature pyramid network (FPN) to extract multi-scale features for constructing cost volume pyramid. The depth estimation and subsequent reconstruction may suffer from over-smoothing around the object boundaries due to the lack of shallow feature information containing low-level features such as local textures and edges.
<img src="/images/image/Framework.pdf"/>

---

## Feature Pyramid Extraction
\label{subsec: deep_feature_extraction} Most recent learning-based methods~\cite{CasMVSNet, UCS-Net, Uni-MVSNet, TransMVSNet} adopts the coarse-to-fine depth estimation strategy and utilizes FPN to extract multi-scale image features for constructing cost volumes at different resolutions. As the depth estimation and subsequent reconstruction may suffer from over-smoothing around the object boundaries due to the lack of shallow feature information containing low-level features such as local textures and edges~\cite{MVSNet}, we enhance the shallow feature information flow by introducing a bottom-up pathway to augment the propagation of low-level features and enlarge the receptive field to incorporate global context information for more accurate and robust feature matching under low-textured regions~\cite{PANet}. We integrate in-place activated batch normalization (ABN) to reduce memory footprint in a computationally efficient way~\cite{InPlace-ABN}. Our feature pyramid extraction network takes as input multi-view images $\{\textbf{I}_{i} \}_{i=0}^{N}$ and output ($L+1$)-level feature pyramids $\{\textbf{f}_{l,i} \in \mathbb{R}^{F_l \times H/2^{l} \times W/2^{l}} \}_{l=0}^{L}$ for each image $\textbf{I}_{i}$, where $l$ represents the level ordinal, $l=L$ is the coarsest level, $l=0$ is the finest level, $F_l$ is the channel number of the feature map at level $l$, $H/{2^l}$ and $W/{2^l}$ is the height and width of the $l$-th level feature map downsampled to $1/2^l$ of the original input image resolution, respectively. Specifically, the...


---

## Benchmark Performance
\label{subsec: benchmark} \textbf{Benchmark on DTU Dataset} We benchmark our method on the \textit{DTU evaluation set} and conduct a comprehensive comparison with traditional (geometric) and state-of-the-art learning-based MVS approaches. We follow the standard evaluation procedure~\cite{DTU_dataset} for quantitative benchmark and summarize the \textit{mean error distance} metrics (in $mm$, lower the better) including reconstruction \textit{accuracy}, \textit{completeness}, and \textit{overall score} as shown in Table~. With different settings, including the changes of $N$ and $N_c$ (detailed in the Appendix), our method performs an excellent trade-off between the reconstruction \textit{accuracy} and \textit{completeness}. It achieves the best performance in terms of the \textit{accuracy}, \textit{completeness} and \textit{overall score} compared with the existing traditional and learning-based methods, indicating the state-of-the-art performance of our method. We qualitatively compare the depth estimation and reconstruction results of several reflective and low-textured scenes with illumination changes on \textit{DTU evaluation set} in Fig.~ and Fig.~ respectively, where our method achieves more complete depth estimation and dense point cloud reconstruction with fine-grained details preserved benefiting from the proposed LCM scheme, qualitatively verifying the quantitative comparison results. \vspace{-1mm} \begin{table}[htbp!] \renewcommand{\arraystretch}{1.3} \caption{Quantitative Benchmarking Results on \textit{DTU Evaluation Set}} \label{dtu_benchmark} \begin{center} \resizebox{0.8\columnwidth}{!}{ \begin{threeparttable} \begin{tabular}{l l c c c} \hline\hline \\[-3mm] \multirow{2}{*}{Type} & \multirow{2}{*}{Methods} & \multicolumn{3}{c}}
<img src="/images/image/TNT-Compare-2.pdf"/>

---

## Real-World Application for UAV-Based Infrastructure Defect Inspection and Localization
\label{sec: uav} As demonstrated in Fig.~, we deploy our MVS method into our UAV-based infrastructure defect inspection system for reconstruction-based defect localization, with crack as our target defect. \textbf{Unmanned Aerial System} As shown in Fig.~ (a), three UAVs are used to speed up the image collection for defect detection and reconstruction of the target warehouse. Each UAV will reach the best region according to the task assignment method. After reaching the best region, viewpoints can be generated based on the building morphology. Furthermore, these viewpoints are regarded as the nodes of a traveling salesman problem to determine the shortest path that travels through all these viewpoints. Finally, the generated path will be executed by each UAV to collect the images for inspection and reconstruction. The multi-UAV-based data collection can speed up the overall image collection process by more than 3 times. \begin{figure}[htbp!]% \centering \includegraphics[width=0.85\columnwidth]{image/defects.pdf} \caption{Experiments for (a) multi-UAV-based data collection; (b) defect detection results.} \label{figure: depth_curve} \vspace{-4mm} \end{figure} \textbf{Defect Detection} Based on our \textit{UAS} system, we collect $923$ images with crack defect from different directions of the target warehouse for defect detection. We train and compare the performance of the state-of-the-art object detection methods on our established defect...
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