#### Wasserstein Generative Adversarial Networks
###### Martin Arjovsky, Soumith Chintala, Léon Bottou

@div[left]

__概要__<br>
データ分布と生成器の分布の距離尺度としてEarth-Mover (EM) distanceを用いたGAN（WGAN：Wasserstein GAN）を提案した。WGANはGANの勾配消失問題を解消し、学習の安定性を向上させた。<br>
<br>
__手法・新規性__<br>
Total Variation (TV) distance、Kullback-Leibler (KL) divergence、Jensen-Shannon (JS) divergenceと異なり、EM distanceは生成器`$g_{\theta}$`の最適解以外の領域においても勾配が連続であり、学習において適切である。EM distanceはデータ分布`$\mathbb{P}_r$`と生成器の分布`$\mathbb{P}_{\theta}$`を用いて、以下の式で表される。<br>
`\begin{align} W(\mathbb{P}_r, \mathbb{P}_{\theta}) &= \inf_{\gamma \in \Pi (\mathbb{P}_r, \mathbb{P}_{\theta})} \int_{\mathcal{X} \times \mathcal{X}} \|x - y\| d \gamma (x,y) \\ &= \inf_{\gamma \in \Pi (\mathbb{P}_r, \mathbb{P}_{\theta})} \mathbb{E}_{(x,y) \sim \gamma} \left[ \|x-y\| \right] \end{align}`
しかし、このままでは下限を取る操作が扱いにくい。そこでKantorovich-Rubinstein双対性を用いると以下のようにできる。<br>
`\begin{align} W(\mathbb{P}_r, \mathbb{P}_{\theta}) = \sup_{|f|_L \leq 1} \mathbb{E}_{x \sim \mathbb{P}_r} \left[ f (x) \right] - \mathbb{E}_{x \sim \mathbb{P}_{\theta}} \left[ f (x) \right] \end{align}`
以上から識別器`$f$`は以下の式を最適化する。<br>
`\begin{align} \max_{\|f\|_L \leq 1} \mathbb{E}_{x \sim \mathbb{P}_r} \left[ f(x) \right] - \mathbb{E}_{x \sim \mathbb{P}_{\theta}} \left[ f(x) \right] \end{align}`
また生成器`$g_{\theta}$`は以下の勾配を用いて重みを更新する。<br>
`\begin{align} \nabla_{\theta} W(\mathbb{P}_r, \mathbb{P}_{\theta}) = - \mathbb{E}_{z \sim p(z)} \left[ \nabla_{\theta} f(g_{\theta} (z)) \right] \end{align}`
Lipschitz制約をニューラルネットが満たすためにはコンパクト空間に存在する必要があるため、シンプルな方法としては重みの更新後に重みを固定値でクリッピングする方法が挙げられる。適切な損失のメトリックを取ることで(1)生成器が収束するようになり、サンプルの質が向上し、(2)最適化のプロセスが安定するようになった。しかし、論文中ではweight clippingは非常にterribleであり、さらなる改良が必要であると述べている。

@divend

@div[right]

![](assets/img/Wasserstein_Generative_Adversarial_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](http://proceedings.mlr.press/v70/arjovsky17a/arjovsky17a.pdf)<br>

@divend