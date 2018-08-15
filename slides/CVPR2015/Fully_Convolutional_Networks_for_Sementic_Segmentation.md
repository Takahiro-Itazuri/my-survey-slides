#### Fully Convolutional Networks for Semantic Segmentation
###### Jonathan Long, Evan Shelhamer, Trevor Darrell

@div[left]

__概要__<br>
本論文は、全畳み込み層ネットワーク（FCN：Fully Covolutional Network）を用いたセマンティックセグメンテーションの手法を提案した。既存のクラス分類ネットワーク（AlexNet、VGG net、GoogLeNet）の全結合層を畳み込み層と捉えなおすことでFCNを実現した。FCNにすることで入力画像サイズに制約がなくなり、従来のパッチごとに切り出して行う方法より効率よく任意のサイズの画像を扱うことできる。またセマンティックセグメンテーションのようなピクセルレベルの出力を行うため、入力層に近い層の情報を持ちいるスキップ構造を持たせることでSoTAを実現した。<br>
<br>
__手法・新規性__<br>
通常のクラス分類ネットワークのニューロン数`$n$`の全結合層を`$n \times 1 \times 1$`の畳み込み層として捉えなおすことで、従来のクラス分類ネットワークを容易にFCNに変換することが可能である。<br>

@divend

@div[right]

![](assets/img/Fully_Convolutional_Networks_for_Sementic_Segmentation.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2015/papers/Long_Fully_Convolutional_Networks_2015_CVPR_paper.pdf)<br>

@divend