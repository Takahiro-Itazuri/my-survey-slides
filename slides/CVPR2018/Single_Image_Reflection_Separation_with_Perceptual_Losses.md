#### Single Image Reflection Separation with Perceptual Losses
###### Xuaner Zhang, Ren Ng, Qifeng Chen

@div[left]

__概要__<br>
本論文では、DNNで単一画像から反射成分と透過成分を分離するタスクを解いている。入力画像Iを反射成分Rと透過成分Tに分離する問題は本来ill-posedな問題であり、従来は様々な前提知識を利用してこの問題を解いていた。近年ではDNNが利用され始めているが、最新の手法であるCEILNetでは低レベルなセマンティクスのみを考慮しているため、十分な精度が出ていなかった。そこで提案手法は高レベルなセマンティクスを考慮することで非常に高品質な分離が可能となった。DNNを学習するにあたって、データセットを構築し、またSoTAの精度を実現した。<br>
<br>
__手法・新規性__<br>
提案手法におけるネットワークの損失はFeature Loss、Adversarial Loss、Exclusion Lossの３つからなる。Feature Lossは提案ネットワークによって分離した画像と正解画像を深い部分における特徴量の差であり、Adversarial LossはCGANを適用しておいリアルな分離を実現するように学習し、Exclusion Lossは基本的に透過部と反射部は１つのエッジを共有しないという観察を元に勾配空間で透過部と反射部をよりはっきりと分けるように学習する。これらの損失を組み合わせたEnd-to-Endのネットワークを用いることでSoTAを実現した。<br>

@divend

@div[right]

![img](assets/img/Single_Image_Reflection_Separation_with_Perceptual_Losses.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Zhang_Single_Image_Reflection_CVPR_2018_paper.pdf)<br>

@divend