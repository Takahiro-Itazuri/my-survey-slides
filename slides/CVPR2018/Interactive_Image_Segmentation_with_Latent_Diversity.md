#### Interactive Image Segmentation with Latent Diversity
###### Zhuwen Li, Qifeng Chen, Vladlen Koltun

@div[left]

__概要__<br>
より少ないインタラクションで高精度なInteractive Image Segmentationを行う論文。インタラクションが少ない場合に発生する曖昧さ（multimodality）の問題に取り組んだ。また従来の手法と同様のインターフェースと互換性のあるシステムとなるような設計を行った。実験では、従来手法より少ないクリック回数で良い精度のセグメンテーションを得ることができるようになった。<br>
<br>
__手法・新規性__<br>
ネットワーク構造はユーザの入力を考慮した複数の異なるセグメンテーション結果を出力するネットワークとそれらから１つのセグメンテーション結果を選択するネットワークで構成される。複数のセグメンテーション結果をランク付けし、それに伴った重み付けを行った損失関数を用いる。<br>


@divend

@div[right]

![](assets/img/Interative_Image_Segmentation_with_Latent_Diversity.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Li_Interactive_Image_Segmentation_CVPR_2018_paper.pdf)<br>

@divend