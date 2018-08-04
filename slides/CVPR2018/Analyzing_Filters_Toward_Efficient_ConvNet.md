#### Analyzing Filters Toward Efficient ConvNet
###### Takumi Kobayashi

@div[left]

__概要__<br>
CNNの振る舞いに関する分析は、従来手法のほとんどが入力に対する活性化に対して行っていたのに対して、本論文はフィルタ自体に着目して分析を行った。畳み込み層と全結合層に対して分析を行い、それぞれに対して基底となるフィルタを作ることで、学習に必要なパラメータ数を減らし、また提案手法を適用することでImageNetで学習させたVGG-vd-16の精度を向上させることに成功した。<br>
<br>
__手法・新規性__<br>
VGG-vd-16の畳み込み層のフィルタに対してSVDを行い主成分を抽出すると、Orthonormal Steerable Filtersと呼ばれる既存の直交するフィルタと非常に類似したフィルタとなっていることがわかった。同様にVGG-Mの全結合層に対してSVDを行い主成分を抽出すると、離散コサイン変換の基底関数と類似していることがわかった。したがって、これらの基底関数の線形和で畳み込み層のフィルタや全結合層の重みが決定できるとすると、従来のおよそ半分の学習パラメータ数に抑えることができる。<br>


@divend

@div[right]

![](assets/img/Analyzing_Filters_Toward_Efficient_ConvNet.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Kobayashi_Analyzing_Filters_Toward_CVPR_2018_paper.pdf)<br>
・[Supplemental Materials](http://openaccess.thecvf.com/content_cvpr_2018/Supplemental/3073-supp.pdf)<br>

@divend