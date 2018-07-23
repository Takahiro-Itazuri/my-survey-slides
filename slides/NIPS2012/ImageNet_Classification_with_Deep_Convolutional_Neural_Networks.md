#### ImageNet Classification with Deep Convolutional Neural Networks
###### Alex Krizhevsky, Ilya Sutskever, Geoffrey E. Hinton

@div[left]

__概要__<br>
本論文では、1000クラスのカテゴリに分類する画像分類タスクにおいて、1,200万枚の画像を用いて学習した深いニューラルネット（AlexNet）を用いて精度を飛躍的に向上させた。CNNは高解像度の画像に対して適用するには非常にコストが大きいため、2次元の畳み込み演算を複数のGPU上で最適化したCNNのC++コードを公開した。<br>
<br>
__手法・新規性__<br>
ネットワーク構成は5層の畳み込み層と3層の全結合層からなる。学習の進みを早くするために活性化関数にReLUを採用し、正規化には同じ位置の複数のカーネルの出力に対して正規化を行うLocal Response Normalizationを用いた。また従来プーリングには重複を持たせていなかったが、ある程度の重複を持たせることで過学習をしにくくできることがわかった。過学習を防ぐため、データ拡張とDropoutを適用した。<br>


@divend

@div[right]

![AlexNet](assets/img/AlexNet.png =full)<br>
<br>

__リンク__<br>
・[論文](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf)<br>
・[code](https://code.google.com/archive/p/cuda-convnet/)<br>

@divend