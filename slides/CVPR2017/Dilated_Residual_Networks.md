#### Dilated Residual Networks
###### Fisher Yu, Vladlen Koltun, Thomas Funkhouser

@div[left]

__概要__<br>
Dialted ConvolutionとResidual Networkを組み合わせたDilated Residual Networks（DRN）を提案した。従来手法のように出力層に近づくにあたって解像度を下げるより、Dilated Convolutionを使って解像度を出力層まで保つことで、画像クラス分類の精度を向上させることができることを示した。またDRNは出力層まで解像度を落とさないため、Semantic SegmentationのようなDense Predictionが必要となるタスクにも適用させることができる。またDilated Convolutionによって生じるグリッド状のartifactを除去するDegriddingのテクニックも提案した。実験の結果、42層のDRNがResNet-101よりも良い精度を出した。<br>
<br>
__手法・新規性__<br>
従来のResNetは５つのResidual Blockで構成され、ResNetの最後の２つのResidual Blockの１層目にあるstrideを除去し、Dialted Convolutionを適用する。これにより入力画像が`$224 \times 224$`だった場合、ResNetの出力は`$7 \times 7$`であるが、DRNの出力は`$28 \times 28$`となる。DRNで`$1/8$`のダウンスケールを行うのは、ハードウェアに制約がある点と`$28 \times 28$`の大きさであれば人間が空間構造を認識できる事実があるからである。Gridding Artifactを除去するために、(1) Max Pooling層を畳み込み層に変更し、(2) 出力層側にDilated Convolutionのdilationを小さくしたBlockを追加し、(3) 出力層側に追加したBlockではResidual Connectionを除去した。<br>


@divend

@div[right]

![](assets/img/Dilated_Residual_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2017/papers/Yu_Dilated_Residual_Networks_CVPR_2017_paper.pdf)<br>
・[GitHub](https://github.com/fyu/drn)<br>

@divend