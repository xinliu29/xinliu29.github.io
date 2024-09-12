---
title: "Progressive Neighbor Consistency Mining for Correspondence Pruning"
collection: publications
permalink: /publication/NCMNet_CVPR23
date: 2023-02-28
venue: 'IEEE Conference on Computer Vision and Pattern Recognition (CVPR)'
# paperurl: 'https://academicpages.github.io/files/paper1.pdf'
# citation: '~~~'
---

<a href="papers/NCMNet/Liu_Progressive_Neighbor_Consistency_Mining_for_Correspondence_Pruning_CVPR_2023_paper.pdf"><img src='https://img.shields.io/badge/PDF-NCMNet-red' alt='Paper PDF'></a>
    <a href='https://github.com/xinliu29/NCMNet'><img src='https://img.shields.io/badge/Project Page-NCMNet-yellow' alt='Project Page'></a>	

The goal of correspondence pruning is to recognize correct correspondences (inliers) from initial ones, with applications to various feature matching based tasks. Seeking neighbors in the coordinate and feature spaces is a common strategy in many previous methods. However, it is difficult to ensure that these neighbors are always consistent, since the distribution of false correspondences is extremely irregular. For addressing this problem, we propose a novel global-graph space to search for consistent neighbors based on a weighted global graph that can explicitly explore long-range dependencies among correspondences. On top of that, we progressively construct three neighbor embeddings according to different neighbor search spaces, and design a Neighbor Consistency block to extract neigh- bor context and explore their interactions sequentially. In the end, we develop a Neighbor Consistency Mining Network (NCMNet) for accurately recovering camera poses and identifying inliers. Experimental results indicate that our NCMNet achieves a significant performance advantage over state-of-the-art competitors on challenging outdoor and indoor matching scenes.
<!-- Abstract: Coming soon... -->


# NCMNet Pipeline
Framework of our NCMNet. $N\times 4$ initial correspondences are established as inputs, then, the parametric model and $N\times 1$ inlier probabilities are estimated. The iterative pruning strategy containing two pruning modules is adopted as the core architecture to distill more reliable candidates for model estimation. Each pruning module includes several existing network structures and the proposed Neighbor Consistency (NC) block. NC block mainly consists of three key parts: the construction of three neighbor embeddings ($\mathcal{G}^S, \mathcal{G}^F, \mathcal{G}^G$), Self-Context Extraction (SCE) layer to capture and aggregate intra-neighbor context ($C^S, C^F, C^G$), and Cross-Context Interaction (CCI) layer to fuse and modulate inter-neighbor information ($I^S, I^F, I^G$). CS: the coordinate space, FS: the feature space, GS: the global-graph space.
<p align="center">
  <img width="95%" src="papers/NCMNet/images/pipeline.png">
</p>
 <br/>


**Recommended citation:**

~~~
@inproceedings{liu2023ncmnet,
  author    = {Liu, Xin and Yang, Jufeng},
  title     = {Progressive Neighbor Consistency Mining for Correspondence Pruning},
  booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
  month     = {June},
  year      = {2023},
  pages     = {9527-9537}
}
~~~