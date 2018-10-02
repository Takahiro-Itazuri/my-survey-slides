#### Efficient Semantic Image Segmentation with Superpixel Pooling
###### Mathijs Schuurmans, Maxim Berman, Matthew B. Blaschko

@div[left]

__概要__<br>
Superpixel Pooling層を提案した。Superpixelを用いる利点として、情報をグルーピングできる点とエッジ情報を維持できる点が挙げられる。しかし、これらの利点は、Superpixelの大きさに応じてトレードオフの関係にある。VoxResNetとENet上で実験を行い、有効性を示した。<br>
<br>
__手法・新規性__<br>
Superpixel Pooling層の役割は、通常のPooling層と同様に局所領域の情報を集約することである。`$C$`チャンネルの`$P$`ピクセルからなる入力画像`$I \in \mathbb{R}^{C \times P}$`について、１チャンネルのSuperpixel画像`$S \in L^{P} (L = \left[ 1, K \right])$`が与えられたとき、Superpixel Pooling層は`$c$`番目のチャンネルの`$i$`番目のピクセルに対して、以下の`$P \in \mathbb{R}^{C \times K}$`を出力する。<br>
`\begin{align} P_{c,k} = reduce \left\{ I_{c,i} | i:S_i=k \right\} \end{align}`
`$reduce$`はmax関数もしくはaverage関数である。同様にSupervoxel Pooling層も定義することができる。単純に通常のPooling層を用いたネットワークから得た特徴量にSupervoxel Pooling層を適用するV1（本質的には既存と同じ）、通常のPooling層の変わりにSuperpixel Pooling層を用いたV2、通常のPooling層を用いて得た特徴量とSuperpixel Poolingを用いた後にUnpoolingを行った特徴量を統合したV3において実験し、V3が最も良い精度を示した。

@divend

@div[right]

![](assets/img/Efficient_Semantic_Image_Segmentation_with_Superpixel_Pooling.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1806.02705.pdf)<br>
・[GitHub](https://github.com/bermanmaxim/superpixPool)<br>

@divend