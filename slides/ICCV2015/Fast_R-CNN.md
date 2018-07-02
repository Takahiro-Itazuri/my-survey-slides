#### Fast R-CNN
###### Ross Girshick

@div[left]

__概要__<br>
R-CNNが各ProposalごとにCNNを順伝搬するため低速であった。そこでSPPnetはCNN特徴量を共有することで計算速度を向上させた。しかし、SPPnetは依然として学習過程がmulti-stageで構成されていることや、fine-tuning時にCNNを更新できないことが、精度を低くする原因となっている。本論文では、single-stageでProposalの分類と位置の更新が可能な構造を持つ高速かつ高精度な物体検出ネットワーク（Fast R-CNN）を提案した。<br>
<br>
__手法・新規性__<br>
Fast R-CNNでは1つネットワークの中で大きく3つの役割を持つ部分に分解できる（全体の処理はsingle-stageに行える）。
1. 画像全体を入力し、CNN特徴量を抽出する。<br>
2. 各ProposalごとにRoI Pooling層を用いて固定長の特徴量を抽出する。<br>
3. クラス分類用の全結合層とBounding Boxの位置を回帰する全結合層に分かれる。<br>
Multi-task Lossを導入することでsingle-stageにすることが可能となった。Multi-task Lossは各クラスごとの確率の正解`$u$`と推定値`$p$`、Bounding Boxの位置の正解`$v$`と推定値`$t$`を用いて、以下の式で与えられる。<br>
`\begin{align} L(p,u,t^u,v) = L_{cls} (p,u) + \lambda \left[ u \geq 1 \right] L_{loc} (t^u, v) \end{align}`

@divend

@div[right]

![Fast R-CNN](assets/img/Fast_R-CNN.png =full)<br>
<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Girshick_Fast_R-CNN_ICCV_2015_paper.pdf)<br>
・[GitHub](https://github.com/rbgirshick/fast-rcnn)<br>

@divend