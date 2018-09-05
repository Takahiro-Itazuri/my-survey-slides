#### Recovering Realistic Texture in Image Super-Resolution by Deep Spatial Feature Transform
###### Xintao Wang, Ke Yu, Chao Dong, Chen Change Loy

@div[left]

__概要__<br>
高解像度化タスクはill-posed problemであるため取りうる解が複数あり、GANを用いてもリアルなテクスチャを生成できていないが、特定のカテゴリに特化して学習させたネットワークを用いればリアルなテクスチャが生成できるという事実から、セマンティックセグメンテーションを利用した高解像度化に着目した。しかし、すべてのカテゴリごとに学習したネットワークを用意することは非現実的であるため、Spatial Feature Transform（SFT）層を導入することで、単一のネットワークでカテゴリ情報を考慮した高解像度化を行った。<br>
<br>
__手法・新規性__<br>
SFT層は特徴量をアフィン変換をする層である。そのアフィン変換はスケールとシフトのパラメータで定義され、これらは各カテゴリごとの確率マップから与えられる。SFT層は従来のネットワークに導入することが可能であり、さらにセマンティックセグメンテーションに限らず、あらゆる事前知識（デプス情報など）に対しても適用可能である。<br>


@divend

@div[right]

![SFT-GAN](assets/img/Recovering_Realistic_Texture_in_Image_Super-Resolution_by_Deep_Spatial_Feature_Transform.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Recovering_Realistic_Texture_CVPR_2018_paper.pdf)<br>

@divend