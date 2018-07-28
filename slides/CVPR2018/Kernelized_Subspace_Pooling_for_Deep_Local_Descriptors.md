#### Kernelized Subspace Pooling for Deep Local Descriptors
###### Xing Wei, Yue Zhang, Yihong Gong, Nanning Zheng

@div[left]

__概要__<br>
CNNの特徴量表現の識別性能を向上させるため、幾何学的変形に不変なプーリング手法であるSubspace Poolingを提案した論文。さらに精度を向上させるため、Marginal Triplet Lossにカーネル法を適用し、Bilinear Poolingより良い精度を少ないメモリ容量で実現した。<br>
<br>
__手法・新規性__<br>
Subspace Poolingは特徴量マップを列成分に並べた行列に対してSVDによって次元圧縮を行う。この方法は、行列の行成分の順列（位置に関する入れ替え）に対して不変である。Patch Matchingのような2点距離を測るようなタスクに対しては、Subspace Poolingで得られた特徴量をガウシアンカーネルを用いたカーネル法を適用することができ、これによりさらに精度を向上させた。<br>


@divend

@div[right]

![](assets/img/Kernelized_Subspace_Pooling_for_Deep_Local_Descriptors.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wei_Kernelized_Subspace_Pooling_CVPR_2018_paper.pdf)<br>

@divend