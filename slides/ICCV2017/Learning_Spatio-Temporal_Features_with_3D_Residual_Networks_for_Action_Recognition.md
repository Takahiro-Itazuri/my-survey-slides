#### Learning Spatio-Temporal Features with 3D Residual Networks for Action Recognition
###### Kensho Hara, Hirokatsu Kataoka, Yutaka Satoh

@div[left]

__概要__<br>
大規模動画データベースにより、パラメータ数が多い3D CNNも学習可能となり、非常に高い精度を実現している一方で、3D CNNは2D CNNと比べて浅いネットワークである。本論文では、2D CNNにおける深いネットワークであるResNetを3D CNNに適用した3D ResNetを提案した。データセットはActivityNetとKineticsを用いて実験し、データ数が多いKineticsデータセット上でC3DやI3D（浅い3D CNN）より高い精度を実現した。<br>
<br>
__手法・新規性__<br>
通常のResNetと同様に、3D ResNetはResidual Blockを重ねていく。入力は16フレーム分のRGB画像である。18層の3D ResNetと34層の3D ResNetを提案した。ActivityNetはデータ量が少ないため、Sports-1Mで事前学習したC3Dは良い精度を出した一方で、提案したネットワークのうち浅い方である18層の3D ResNetでも過学習を起こした。その一方で、Kineticsのような大規模データセットを使用すると、34層の3D ResNetでも過学習を起こすことなく、非常に良い精度を出した。<br>

@divend

@div[right]

![3D ResNet](assets/img/3D_ResNet.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_ICCV_2017_workshops/papers/w44/Hara_Learning_Spatio-Temporal_Features_ICCV_2017_paper.pdf)<br>
・[GitHub](https://github.com/kenshohara/3D-ResNets)<br>

@divend