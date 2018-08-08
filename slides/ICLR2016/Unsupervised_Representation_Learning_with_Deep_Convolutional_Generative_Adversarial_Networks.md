#### Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks
###### Alec Radford, Luke Metz, Soumith Chintala

@div[left]

__概要__<br>
教師ありCNNに比べて、教師なしCNNは注目されてこなかったが、ラベルの付いていないデータから再利用可能な特徴量表現を得ることは非常に重要である。教師なし学習の手法としてGANで学習したDiscriminatorを特徴量抽出器として他のタスクに利用することが注目されているが、GANは学習が安定しないことが知られている。本論文はGANを安定的に学習させることが可能な構造を持つネットワーク（DCGAN：Deep Convolutional GANs）を提案した。また学習したGANのDiscriminatorを画像分類タスクに使用し、教師なし学習の手法においてSoTAを実現し、またGANで学習されたフィルタの可視化を行った。<br>
<br>
__手法・新規性__<br>
安定的な学習が可能なDCGANの構造のガイドラインは以下の通り。<br>
・プーリング層の代わりにストライドを大きくした畳み込み層を使う。<br>
・Batch Nomalizationを使う。<br>
・全結合層を排除する。<br>
・Generatorの出力層以外の活性化関数にはReLU、出力層にはTanhを使う。<br>
・DiscriminatorにはLeakyReLUを使う。<br>


@divend

@div[right]

![DCGAN](assets/img/Unsupervised_Representation_Learning_with_Deep_Convolutional_Generative_Adversarial_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1511.06434.pdf)<br>

@divend