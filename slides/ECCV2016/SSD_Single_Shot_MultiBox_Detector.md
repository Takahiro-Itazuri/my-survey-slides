#### SSD: Single Shot MultiBox Detector
###### Wei Liu, Dragomir Anguelov, Dumitru Erhan, Christian Szegedy, Scott Reed, Cheng-Yang Fu, Alexandar C. Berg

@div[left]

__概要__<br>
Faster R-CNNはBounding Box Proposalの生成やそれに伴う特徴量やピクセルのリサンプリングがあるために高速性が損なわれている。本論文では、Bounding Box Proposalの生成をしない物体検出手法（SSD：Single Shot MultiBox Detector）を提案した。Faster R-CNNは7fpsでmAP 73.2%、YOLOは45fpsでmAP 63.4%であるのに対して、SSDは59fpsでmAP 74.3%を実現した。<br>
<br>
__手法・新規性__<br>
SSDは複数の特徴量マップ上の各位置で異なるアスペクト比を持つ複数のdefault boxを持ち、そのdefault boxごとにboxの形のoffsetと物体のカテゴリの確率を出力する。損失は位置についてはSmooth L1 Lossを用い、カテゴリについてはSoftmax Lossを適用する。<br>
`$\begin{align} L(x,c,l,g) = \frac{1}{N} \left(L_{conf}(x,c) + \alpha L_{loc}(x,l,g) \right) \end{align}$`

@divend

@div[right]

![SSD](assets/img/SSD_Single_Shot_MultiBox_Detector.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1512.02325.pdf)<br>
・[GitHub](https://github.com/weiliu89/caffe/tree/ssd)<br>

@divend