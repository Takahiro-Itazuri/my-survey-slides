#### MoNet: Moments Embedding Network
###### Mengran Gou, Fei Xiong, Octavia Camps, Mario Sznaier

@div[left]

__概要__<br>
Bilinear Poolingは2次の統計量を用いているため非常に良い精度を出す一方で、出力の特徴量の次元数が膨大になるといった問題点がある。本論文はBilinear Poolingの次元数をコンパクトにしたネットワークMoNetを提案した。MoNetはSoTAと同等の精度を保ちながら、特徴量の次元を4%にまで落とすことに成功した。<br>
<br>
__手法・新規性__<br>
Bilinear Poolingの次元数を減らすためCompact Poolingが提案されたが、通常のBilinear Poolingをさらに拡張したiBCNNやG2DeNetに対しては、Gaussian EmbeddingとBlinear Poolingが絡んでいること点と行列の正規化が必要な点から適用することができない。そこでMoment Matrixを用いてGaussian EmbeddingとBilinear Poolingを別にし、sub-matrix square root layerを追加してBilinear Poolingの前に正規化を行うことでCompact Poolingを適用可能にした。<br>


@divend

@div[right]

![](assets/img/MoNet.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Gou_MoNet_Moments_Embedding_CVPR_2018_paper.pdf)<br>

@divend