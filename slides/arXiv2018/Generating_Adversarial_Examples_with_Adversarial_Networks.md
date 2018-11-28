#### Generating Adversarial Examples with Adversarial Networks
###### Chaowei Xiao, Bo Li, Jun-Yan Zhu, Warren He, Mingyan Liu, Dawn Song

@div[left]

__概要__<br>
知覚的によりリアルなadversarial examplesを生成するため、GANを利用したadversarial examplesを生成するネットワーク（AdvGAN）を提案した。提案手法はsemi-whitebox attack（一度学習した後はターゲットのモデルへのアクセスを必要としない）とblackbox attack（モデルへの一切のアクセスを必要としない）を実現した。AdvGANは１回のfeedforwardでadversarial examplesが生成できるため高速である。<br>
<br>
__手法・新規性__<br>
AdvGANは生成器`$G$`と識別器`$D$`と攻撃対象の分類器`$f$`からなる。`$G$`はpix2pixと同様の構造をしており、入力データ`$x$`に対して摂動`$G(x)$`を出力する。`$D$`は入力がadversarial examplesかどうかを識別する。提案手法のsemi-whitebox attackの損失関数は以下の通りである。<br>
`\begin{align} \mathcal{L} $= \mathcal{L}_{adv}^{f} + \alpha \mathcal{L}_{GAN} + \beta \mathcal{L}_{hinge} \\ \mathcal{L}_{adv}^{f} $= \mathbb{E}_x \left[ l_f (x + G(x), t) \right] \\ \mathcal{L}_{GAN} &= \mathbb{E} \left[ \log D(x) + \log \left( 1 - D(x + G(x)) \right) \right] \\ \mathcal{L}_{hinge} &= \mathbb{E}_x \max \left( 0, \|G(x)\|_2 - c \right) \end{align}`
ただし、`$t$`はターゲットラベルであり、`$c$`は摂動の大きさの制約パラメータであり、`$\alpha, \beta$`は損失の重要度をコントロールするパラメータである。これをblackbox attackにするために、blackboxな分類器`$f$`に対して、knowledge distillationによって学習した`$b$`に対して同様の学習を行う。

@divend

@div[right]

![](assets/img/Generating_Adversarial_Examples_with_Adversarial_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1801.02610.pdf)<br>

@divend