#### Towards Principled Methods for Training Generative Adversarial Networks
###### Martin Arjovsky, Léon Bottou

@div[left]

__概要__<br>
GANの最も大きい問題点である不安定さに関する理論的説明を行った。<br>
<br>
__手法・新規性__<br>
真のデータ分布`$\mathbb{P}_r$`と生成器`$g_{\theta}$`のデータ分布`$\mathbb{P}_g$`が与えられたとき、従来の尤度最大化による手法ではKullback-Leibler (KL) divergence `$KL(\mathbb{P}_r||\mathbb{P}_g)$`の最小化を行っていたが、非対称性に基づく不安定性がある。GANではKL divergenceの代わりに、対称性を持つ以下のJenson-Shannon (JS) divergence `$JS (\mathbb{P}_r || \mathbb{P}_g)$`に置き換えており、GANの成功はこの変更によるものが大きいとされている。<br>
`\begin{align} JS(\mathbb{P}_r || \mathbb{P}_g) = \frac{1}{2} KL (\mathbb{P}_r || \mathbb{P}_A) + \frac{1}{2} (\mathbb{P}_g || \mathbb{P}_A) \end{align}`
`$\mathbb{P}_A$`は密度関数`$(P_r+P_g)/2$`を持つ平均分布である。しかし、GANの学習はclosedからほど遠い。GANの学習は２つのステップからなり、まず以下のcriterion `$L$`を最大化するように識別器`$D$`を学習した後、生成器`$g_{\theta}$`を学習する。
`\begin{align} L(D, g_{\theta}) = \mathbb{E}_{x \sim \mathbb{P}_r} \left[ \log D(x) \right] + \mathbb{E}_{x \sim \mathbb{P}_g} \left[ \log (1 - D(x)) \right] \end{align}`
しかし、実際の学習はsaturationが原因で安定しないため、生成器`$g_{\theta}$`は`$\mathbb{E}_{x \sim \mathbb{P}_g} \left[ - \log (D(x)) \right]$`を最小化するように学習すると良いと記述されているが、これを用いても実際には学習は安定しない。このような既に報告されている不安定性について理論的説明を行った。<br>

@divend

@div[right]

（以降、数学的証明は論文を参照）<br>
一度学習させたDCGANの生成器に対して、識別器`$D$`をスクラッチで学習させると、早い段階でerrorが`$0$`になり、これはJSDが最大化されていることを意味し、またこれが発生するのは`$\mathbb{P}_r$`と`$\mathbb{P}_g$`の台がdisjointになっていることを意味する。論文中では、２つの確率分布`$\mathbb{P}_r$`と`$\mathbb{P}_g$`の台を含む多様体`$\mathcal{M}$`と`$\mathcal{P}$`が与えられたとき、`$\mathcal{M}$`もしくは`$\mathcal{P}$`上のほとんどの`$x$`に対して精度が`$1$`となる（完全に分離）最適な識別器`$D^{\ast}$`が存在することを数学的に証明した。このような識別器はKL divergenceを無限大にし、JS divergenceを最大にする。したがって、学習を安定化するには、多様体上の分布の距離を測るためのよりソフトな尺度が必要である。さらに、GANの最初の論文で提案された生成器に関する２つの損失関数はどちらを使っても学習が安定しないことを示した。<br>
このような問題の解決策の一つとして、識別器の入力にノイズを加える方法が有効であり、この操作は確率質量の分布を滑らかにする効果がある。実際にノイズを加えた確率分布`$\mathbb{P}_{X+\epsilon}$`の密度`$P_{X+\epsilon}(x)$`は`$\mathbb{P}_X$`の台上の点群までの距離を各点の発生確率で重み付けた平均に反比例する（データ分布までの距離を導入できている）。ノイズを加えたときの識別器の最適解を用いると、生成器`$g_{\theta}(z)$`で生成したサンプルは真のデータの多様体に向かうようになる。非常に近い２つの分布`$\mathbb{P}_r$`と`$\mathbb{P}_g$`はノイズを載せたnoisyな分布`$\mathbb{P}_{r+\epsilon}$`と`$\mathbb{P}_{g+\epsilon}$`になると、ほとんどの領域で重複しており小さなDS divergenceが小さくなる。しかし、実際にはノイズの種類や大きさに依存するため、データ間の距離を陽に考えたWasserstein metricを用いるとよい。Wasserstein metricを用いたGAN（WGAN）を実際に適用したものは別の論文にて提案されている。<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1701.04862.pdf)<br>

@divend