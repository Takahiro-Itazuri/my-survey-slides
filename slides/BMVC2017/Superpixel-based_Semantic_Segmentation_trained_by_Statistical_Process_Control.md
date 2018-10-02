#### Superpixel-based Semantic Segmentation trained by Statistical Process Control
###### Hyojin Park, Jisoo Jeong, Youngjoon Yoo and Nojun Kwak

@div[left]

__概要__<br>
従来のCNNは最終的にピクセルごとにクラス分類問題を解いており、隣接するピクセル間の持つ依存性を考慮していないため、非常に冗長であることを指摘した。この問題を避けるために、Superpixelに基づいたサンプリングによるSemantic Segmentation手法（HP-SPS: Hypercolumns for Pyramid module with SuperPixel-based Sampling）を提案した。これによりCNNのアップサンプリングの計算量を大幅に削減することが可能になった。また、これによりサンプリング数が著しく減ったことによって学習が進みにくくなる問題をStatistical Process Control（SPC）により解決した。<br>
<br>
__手法・新規性__<br>
提案手法はまず通常のCNNと同様に特徴量を抽出し、次にSuperpixelごとにランダムにピクセルを抽出し、そのピクセルに対応するCNN特徴量をHypercolumnで取り出し、そのHypercolumnに対してクラス分類のタスクを解く。しかし、Superpixelが１サンプルとなるため、本来のピクセルごとのサンプリングに比べて、サンプリング数は0.374%まで減ってしまう。これによる学習の不安定さを避けるため、学習率をSPCによって調整する手法を提案した。<br>


@divend

@div[right]

![](assets/img/Superpixel-based_Semantic_Segmentation_trained_by_Statistical_Process_Control.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1706.10071.pdf)<br>

@divend