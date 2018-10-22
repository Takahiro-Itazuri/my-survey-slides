#### Improved Techniques for Training GANs
###### Tim Salimans, Ian Goodfellow, Wojciech Zaremba, Vicki Cheung, Alec Radford, Xi Chen

@div[left]

__概要__<br>
本論文ではGANの収束性を高めるためのいくつかのテクニックを提案した。提案手法はMNIST、CIFAR-10、SVHNにおける半教師ありクラス分類においてSoTAを実現した。また生成した画像はTuring Testにおいて非常に良い数字を出した。<br>
<br>
__手法・新規性__<br>
GANにおけるDiscriminator `$D$`とGenerator `$G$`の学習を収束させるためのテクニックは以下の通りである。Feature Matchingは`$G$`が現在の`$D$`に過学習するのを避けるため、本物の画像と統計量（実際には`$D$`の中間層の特徴量の期待値）を一致させるよう`$G$`を学習させる。Minibatch Discriminationは`$G$`がmode collapseを起こすのを避けるため、`$D$`の中間層においてミニバッチ内のお互いのサンプルの情報（side information）を考慮させることにより、`$D$`はサンプルごとに独立に識別していたが、複数のデータを組み合わせて識別するように学習する。これら２つのテクニックに加えて、Historial Averaging、One-side Label Smoothing、Virtual Batch Normalizationのテクニックを提案した。またAMTにおける評価に加えて、GANで生成した画像の質を評価するための指標としてInception Score（IS）を提案した。ISは意味の画像を生成できていれば、Inception Networkによる推定クラスラベル分布`$p(y|x)$`のエントロピーは大きくなり、多様性のある画像を生成できていれば周辺化確率`$\int p(y|x=G(z)) dz$`のエントロピーは小さくなるはずである。以上から、これら２つのKLダイバージェンスを評価尺度として用いる。<br>
`\begin{align} IS(G) = \exp \left( \mathbb{E}_{x \sim p_g} \left[ D_KL (p(y|x) || p(y)) \right] \right) \end{align}`
また半教師ありクラス分類のために`$D$`をクラス数`$K$`に生成した画像用クラスを加えた`$K+1$`クラス分類を行うように`$D$`を学習した。

@divend

@div[right]

![](assets/img/Improved_Techniques_for_Training_GANs.png =full)<br>
<br>

__リンク__<br>
・[論文](https://papers.nips.cc/paper/6125-improved-techniques-for-training-gans.pdf)<br>
・[GitHub](https://papers.nips.cc/paper/6125-improved-techniques-for-training-gans.pdf)<br>

@divend