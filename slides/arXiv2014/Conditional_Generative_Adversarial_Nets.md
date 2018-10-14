#### Conditional Generative Adversarial Nets
###### Mehdi Mirza, Simon Osindero

@div[left]

__概要__<br>
通常のGANに追加の情報で条件付けたConditional GANを提案した。実験では、MNISTに対してクラスラベルで条件付けて画像を生成し、YMCC 100Mに対して画像で条件付けてタグを生成し、Conditional GANを評価した。<br>
<br>
__手法・新規性__<br>
通常のGANは、以下のように定式化される。<br>
`\begin{align} \mathop{\rm min}\limits_{G} \mathop{\rm max}\limits_{D} V(D,G) = \mathbb{E}_{x \sim p_{data} (x)} \left[ \log D(x) \right] + \mathbb{E}_{z \sim p_z (z)} \left[ \log (1 - D(G(z))) \right] \end{align}`
通常のGANに対して、追加で情報`$y$`で条件付けると、以下のように定式化される。<br>
`\begin{align} \mathop{\rm min}\limits_{G} \mathop{\rm max}\limits_{D} V(D,G) = \mathbb{E}_{x \sim p_{data} (x)} \left[ \log D(x|y) \right] + \mathbb{E}_{z \sim p_z (z)} \left[ \log (1 - D(G(z|y))) \right] \end{align}`

@divend

@div[right]

![](assets/img/Conditional_Generative_Adversarial_Nets.png =full)<br>
<br>

__リンク__<br>
・[](https://arxiv.org/pdf/1411.1784.pdf)<br>

@divend