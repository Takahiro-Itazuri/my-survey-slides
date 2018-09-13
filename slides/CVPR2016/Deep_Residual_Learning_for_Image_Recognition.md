#### Deep Residual Learning for Image Recognition
###### Kaiming He, Xiangyu Zhang, Shaoqing Ren, Jian Sun

@div[left]

__概要__<br>
本論文は、より深いニューラルネットワークを学習することを可能にするため、入力に関する残差を学習するResidual Learningを提案した。VGGの8倍以上の深さになる182層からなるネットワーク（Residual Network）を提案し、ILSVRC 2015で優勝した。<br>
<br>
__手法・新規性__<br>
Deep Residual Learning Frameworkは、従来のDNNで学習していた写像関数`$\mathcal{H}(x)$`から入力を引いた残差関数`$\mathcal{F}(x) = \mathcal{H}(x)-x$`を学習する。もし恒等関数が最適解であった場合、恒等写像を学習させるより、残差が0になるように学習する方が容易であるからである。また提案手法のshortcut connectionは従来手法とは異なり、入力をそのまま伝搬するため追加のパラメータや計算の複雑さがない。実験の結果からも入力をそのまま伝搬するのがよいことを確認した。<br>


@divend

@div[right]

![ResNet](assets/img/Deep_Residual_Learning_for_Image_Recognition.png =full)<br>
<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf)<br>
・[GitHub](https://github.com/KaimingHe/deep-residual-networks)<br>

@divend