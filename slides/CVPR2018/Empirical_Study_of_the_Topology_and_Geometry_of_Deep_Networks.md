#### Empirical Study of the Topology and Geometry of Deep Networks
###### Alhussein Fawzi, Seyed-Mohsen Moosavi-Dezfooli, Pascal Frossard

@div[left]

__概要__<br>
本研究は、DNNを用いた画像クラス分類器の入力画像空間中おける幾何学的性質を解析する論文である。特に「各分類領域の位相空間として連結性」と「曲率に基づく識別境界の形状の考察」について経験的研究を行った。<br>
<br>
__手法・新規性__<br>
分類領域`$\mathcal{R}_i$`の任意の２つのデータ`$x_1, x_2 \in \mathcal{R}_i$`に対して、`$\gamma(0)=x_1, \gamma(1)=x_2$`を満たす連続な曲線`$\gamma: \left[0, 1\right] \to \mathcal{R}_i$`が存在するとき、連結であると定義する。この経路`$\mathcal{P}$`を有限なアンカーポイントの集合`$\left( p_0=x_1, p_1, \cdots, p_n, p_{n+1}=x_2 \right)$`で表現する。様々なサンプルのペアに対して経路探索を行った結果、「同一の分類領域に含まれる任意の２点が連結性を満たすこと」と「その経路はほぼ直線的な経路であること」がわかった（ただし分類領域は凸であるとは限らないことに注意）。<br>
次に任意のデータ`$x$`の近傍に存在する識別境界上の点`$z=x+r(x)$`に対して、主曲率を計算するとほとんどの方向で0であることと非常に大きな負の曲率を含むことがわかった。これから境界面をほとんどの方向で平坦であり、特定の方向に対して大きく曲がっていることがわかる。そして、あらゆるデータ点に対して主曲率を計算し、大きな主曲率を持つ方向は異なるデータ同士で共有されていることがわかった。共有している大きな主曲率を持つ方向を可視化すると局所的なGaborフィルタのようなものであることがわかった。また大きな主曲率を持つ方向のノイズにCNNは非常に弱いこともわかった。<br>
自然画像の主曲率の平均は正になるが、adversarial examplesの主曲率の平均は負になるという曲率の非対称性を用いて、非常に高い精度でadversarial examplesを検出し、また正しいラベルを推定することが可能である。

@divend

@div[right]

![](assets/img/Empirical_Study_of_the_Topology_and_Geometry_of_Deep_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Fawzi_Empirical_Study_of_CVPR_2018_paper.pdf)<br>

@divend