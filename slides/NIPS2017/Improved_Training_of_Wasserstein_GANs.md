#### Improved Training of Wasserstein GANs
###### Ishaan Gulrajani, Faruk Ahmed, Martin Arjovsky, Vincent Dumoulin, Aaron Courville

@div[left]

__概要__<br>
WGANではLipschitz制約を満たすためにweight clippingを行っていたが、いくつか問題点があり、critic `$D$`の最適解が持つ性質をもとにweight penaltyを用いた手法（WGAN-GP）を提案した。<br>
<br>
__手法・新規性__<br>
weight clippingには高次のモーメントが無視され、最適解からかなり単純化された近似をモデル化してしまう点とweight clippingの閾値`$c$`の大きさによって勾配が消失したり爆発してしまう点が問題であった。<br>
そこで最適なcriticの勾配のノルムがデータ分布`$\mathbb{P}_r$`と生成器の分布`$\mathbb{P}_g$`上のほとんどの場所で`$1$`になることを証明し、これに基づいて、次式のようにcriticの勾配のノルムに関するsoft constraintとしてgradient penaltyを導入した。
`\begin{align} L = \mathbb{E}_{\hat{x} \sim \mathbb{P}_g} \left[ D (\hat{x}) \right] - \mathbb_{x \sim \mathbb{P}_r} \left[ D(x) \right] + \lambda \mathbb{E}_{\hat{x} \sim \mathbb{P}_{\hat{x}}} \left[ \left( \|\nabla_{\hat{x}} D(\hat{x}) \|_2 - 1 \right)^2 \right] \end{align}`
`$\mathbb{P}_{\hat{x}}$`は`$\mathbb{P}_r$`と`\mathbb{P}_g`からサンプリングされたペアの間を結んだ直線上から一様にサンプリングする。またgradient penaltyは入力ごとに独立にかかるものであるため、critic `$D$`からバッチに依存する処理であるbatch normalizationは除去する（代わりにlayer normalizationは利用することができる）。


@divend

@div[right]

![](assets/img/Improved_Training_of_Wasserstein_GAN.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1704.00028.pdf)<br>
・[GitHub](https://github.com/igul222/improved_wgan_training)<br>

@divend