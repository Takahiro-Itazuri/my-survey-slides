#### Dual Attention Matching Network for Context-Aware Feature Sequence based Person Re-Identification
###### Jianlou Si, Honggang Zhang, Chun-Guang Li, Jason Kuen, Xiangfei Kong, Alex C. Kot, Gang Wang

@div[left]

__概要__<br>
Person Re-Identification（ReID）をするためのEnd-to-Endなネットワーク（Dual ATtention Matching network: DuATM）を提案した論文。DuATMのコアとなる要素はdual attention mechanismであり、映像内と映像間のattentionを特徴量の補正とペアリングに用いる。また実験では、いくつかのベンチマークでSoTAを達成した。<br>
<br>
__手法・新規性__<br>
DuATMは大きく２つの構成要素からなる。１つは動画内から特徴量を抽出する要素であり、もう１つはそれらの特徴量のマッチングを行う要素である。後者にdual attention mechanismが導入されており、１つはコンテキストに応じて映像内の特徴量を補正するものでありもう１つは映像間の割り当てを行うものである。DuATMの損失関数はtriplet lossに加えて、de-correlatoin lossとcross-entropy lossを用いており、これに対してsiamese networkを学習する。<br>


@divend

@div[right]

![DuATM](assets/img/DuATM.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Si_Dual_Attention_Matching_CVPR_2018_paper.pdf)<br>

@divend