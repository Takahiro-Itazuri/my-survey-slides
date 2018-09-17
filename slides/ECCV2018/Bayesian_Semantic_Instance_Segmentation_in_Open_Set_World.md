#### Bayesian Semantic Instance Segmentation in Open Set World
###### Trung Pham, Vijay Kumar B G, Thanh-Toan Do, Gustavo Carneiro, Ian Reid

@div[left]

__概要__<br>
既存のSemantic Segmentationは学習時にすべての物体のマスクアノテーションが必要になるため、現実世界のアプリケーションとしては現実的ではなかった。本論文は、このようなOpen-Set ConditionにおけるSemantic Instance SegmentationのためのBayesianに基づくフレームワークを提案した。提案手法は既知のクラスに対してSoTAに近い精度を出し、さらに未知のクラスに対して教師なし学習手法より良い精度を達成した。<br>
<br>
__手法・新規性__<br>
提案手法は画像入力`$I$`に対するセグメンテーション`$S$`の事後確率`$p(S|I)\propto p(I|S)p(S)$`を最大化するMAP推定を解く。セグメンテーションされた各領域は互いに独立であるため、尤度`$$p(I|S)`は以下のようにできる。<br>
`\begin{align} p(I|S) = \prod_{i=1}^{k} p(I_{R_i} | t_i, \theta_i) \end{align}`
`$t$`はモデルタイプを表し、`$\theta$`はそのモデルのパラメータを意味する。モデルタイプはBoundary / Contour Model（`$\mathcal{C}$`）、Bounding Box Model（`$\mathcal{B}$`）、Mask Model（`$\mathcal{M}$`）があり、`$\mathcal{C}$`は未知の物体領域のためのモデルであり、`$\mathcal{B}$`と`$\mathcal{M}$`は既知の物体領域のためのモデルである。上述のMAP推定を解くためにSimulated Annealingを用いて、大域最適解の近似解を得る。また新しいセグメンテーションを生成するために、Region Hierarchyに基づいたPartition Sampling法を提案した。sample-and-pasteの操作を行うだけで、split、merge、split-and-mergeのプロセスを確率的に行うことができる。

@divend

@div[right]

![](assets/img/Bayesian_Semantic_Instance_Segmentation_in_Open_Set_World.png =full)<br>
<br>

__リンク__<br>
・[論文](https://eccv2018.org/openaccess/content_ECCV_2018/papers/Trung_Pham_Bayesian_Instance_Segmentation_ECCV_2018_paper.pdf)<br>

@divend