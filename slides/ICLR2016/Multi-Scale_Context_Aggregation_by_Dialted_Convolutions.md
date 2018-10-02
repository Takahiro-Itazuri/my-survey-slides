#### Multi-Scale Context Aggregation by Dialted Convolutions
###### Fisher Yu, Vladlen Koltun

@div[left]

__概要__<br>
既存のSemantic Segmentationの手法は画像クラス分類におけるCNNをそのまま適用しているが、Semantic SegmentationのようなDense Predictionタスクは画像クラス分類タスクとは構造的に異なる。本論文では、解像度を下げることなく、指数的に受容野を広くすることができるモジュール（Dialted Convolution）を提案した。<br>
<br>
__手法・新規性__<br>
離散関数`$F:\mathbb{Z} \to \mathbb{R}$`、領域`$\Omega_r = \left[ -r, r \right]^2 \cap \mathbb{Z}^2$`、フィルタサイズ`$(2r+1)^2$`の離散フィルタ`$k: \Omega_r \to \mathbb{R}$`が与えられたとき、離散畳み込み演算子`$\ast$`は以下のように定義される。<br>
`\begin{align} (F \ast k) (p) = \sum_{s+t=p} F(s)k(t) \end{align}`
これにdilation factor `$l$`を導入すると、以下のようになる。<br>
`\begin{align} (F \ast_{l} k) (p) = \sum_{s+lt=p} F(s)k(t) \end{align}`
このような畳み込みをDialted Convolutionと呼ぶ。層が深くなるにつれて、Dilation Factorを徐々に大きくするようにネットワークを設計すると、受容野を指数的に大きくすることができる。<br>

@divend

@div[right]

![](assets/img/Multi-Scale_Context_Aggregation_by_Dialted_Convolutions.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1511.07122.pdf)<br>
・[GitHub](https://github.com/fyu/dilation)<br>
・[著者ページ](http://www.yf.io/)<br>

@divend