#### Learning to Compare Image Patches via Convolutional Neural Networks
###### Sergey Zagoruyko, Nikos Komodakis

@div[left]

__概要__<br>
本論文は画像パッチのペアの類似度を計算するCNNとして最適な構造はどんな構造であるかを実験した。実際には、Siamese Network、Pseudo-siamese Network、Two-channel Networkのネットワーク構造に対して、それぞれShallow Network、Deep Network、Central-Surround Two-stream Network、Spatial Pyramid Pooling (SPP) Networkのバリエーションを加えたもので実験を行った。<br>
<br>
__手法・新規性__<br>
目的関数は以下の通り。<br>
`\begin{align} \mathop{\rm min}\limits_{\omega} \frac{\lambda}{2} \| \omega \| + \sum_{i=1}^{N} {\rm max} \left( 0, 1 - y_i o_i^{net} \right) \end{align}`
結果として、Two-channel Networkが最も良い結果を出した。

@divend

@div[right]

![](assets/img/Learning_to_Compare_Image_Patches_via_Convolutional_Nerual_Networks.png =full)<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Zagoruyko_Learning_to_Compare_2015_CVPR_paper.pdf)<br>
・[プロジェクト](http://imagine.enpc.fr/~zagoruys/publication/deepcompare/)<br>
・[GitHub](https://github.com/szagoruyko/cvpr15deepcompare)

@divend