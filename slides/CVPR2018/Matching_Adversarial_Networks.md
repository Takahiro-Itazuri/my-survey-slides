#### Matching Adversarial Networks
###### Geller Mattyus, Raquel Urtasun

@div[left]

__概要__<br>
GANで教師あり学習をするタスクにおいて、DiscriminatorにSiamese Networkを適用することで直接教師データを損失関数に導入することが可能なMatching Adversarial Network（MatAN）を提案した。MatANは様々なGANで行う教師あり学習のタスクに適用することが可能であり、実験においてはsemantic segmentation、road network centerline extraction、instance segmentationのタスクに適用し、良い精度を出した。<br>
<br>
__手法・新規性__<br>
DiscriminatorをSiamese Networkにする。2枚の画像ペアのうち、1枚はground truthであり、もう1枚はnegative sampleはGeneratorによって生成された画像もしくはground truthに摂動を加えた画像である。学習の方法自体は、通常のGANと同様に、Discriminatorはrealかfakeかを識別できるように学習し、GeneratorはDiscriminatorの識別率を下げるように学習する。<br>


@divend

@div[right]

![](assets/img/MatAN.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Mattyus_Matching_Adversarial_Networks_CVPR_2018_paper.pdf)<br>

@divend