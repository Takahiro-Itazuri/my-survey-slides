#### Occlusion Aware Unsupervised Learning of Optical Flow
###### Yang Wang, Yi Yang, Zhenheng Yang, Liang Zhao, Peng Wang, Wei Xu

@div[left]

__概要__<br>
オプティカルフローのアノテーションが困難であることから、教師なし学習ベースのオプティカルフロー推定手法が提案されているが、十分な精度が出ていない。そこで問題とされている遮蔽と大きな動きに対応したネットワークを提案。<br>
<br>
__手法・新規性__<br>
２枚の画像に対して、１枚目から２枚目へのオプティカルフロー`$F_{12}$`と、２枚目から１枚目のオプティカルフロー`$F_{21}$`を推定する。２枚目の画像と前者のオプティカルフロー`$F_{12}$`を用いて、１枚目の画像を復元する。復元した１枚目の画像のうち遮蔽が発生していない部分に対して、本物の１枚目の画像との差を損失として用いる。<br>

@divend

@div[right]

![](assets/img/Occlusion_Aware_Unsupervised_Learning_of_Optical_Flow.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1711.05890.pdf)<br>

@divend