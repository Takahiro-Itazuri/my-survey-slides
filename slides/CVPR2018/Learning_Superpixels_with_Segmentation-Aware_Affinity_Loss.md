#### Learning Superpixels with Segmentation-Aware Affinity Loss
###### Wei-Chih Tu, Ming-Yu Liu, Varun Jampani, Deqing Sun, Shao-Yi Chien, Ming-Hsuan Yang, Jan Kautz

@div[left]

__概要__<br>
Groundtruthがないことや、Superpixelのインデックスは可換であること、既存手法は微分不可能であることから、SuperpixelをDNNで学習する手法は提案されていなかった。本論文では、隣接するピクセルが同一物体に属するかどうかの尤度を表すPixel Affinityを推定するネットワーク（PAN：Pixel Affinity Net）を既存のセグメンテーションデータセットを用いて学習させた。<br>
<br>
__手法・新規性__<br>
提案手法は、PANによって推定したPixel Affinityを、グラフベースの手法であるERS（Entropy Rate Superpixel Segmentation）へ入力し、Superpixelを計算する。得られたSuperpixel `$S_k$`、セグメンテーションのGroudtruth `$G_j$`とその境界`$B_j$`を用いて、SEAL（SEgmenta-Aware Loss）を以下のように定義する。<br>
`\begin{align} L_{SEAL} (\theta) &= - \sum_i \left( 1 + \gamma_i \right) \left( t_i \log \left( a_i \right) + \left( 1 - t_i \right) \log \left( 1 - a_i \right) \right) \\ \gamma_i &= \begin{cases} |S_k \setminus \left\{ S_k \cap G_j \right\} | & \left( i \in S_k \cap B_j \right) \\ 0 & \left( {\rm otherwise} \right) \end{cases} \end{align}`

@divend

@div[right]

![](assets/img/Learning_Superpixels_with_Segmentation-Aware_Affinity_Loss.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Tu_Learning_Superpixels_With_CVPR_2018_paper.pdf)<br>
・[プロジェクト](https://sites.google.com/site/wctu1009/cvpr18_superpixel)<br>

@divend