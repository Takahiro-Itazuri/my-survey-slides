#### Generative Adversarial Nets
###### Ian J. Goodfellow, Jean Pouget-Abadie, Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozairm Aaron Courville, Yoshua Bengio

@div[left]

__概要__<br>
敵対的プロセスを通して生成モデルを学習する新しいフレームワーク（GAN：Generative Adversarial Nets）を提案した。GANはデータの分布を真似る生成モデル`$G$`と、入力画像が`$G$`が生成したサンプル（fake sample）か本物のデータサンプル（real sample）かの確率を出力する識別モデル`$D$`を同時に学習させる。このフレームワークは２人のプレイヤーによるminimax gameとなっており、従来のようにマルコフ連鎖やあらゆる近似を仮定する必要がない。<br>
<br>
__手法・新規性__<br>
生成モデル`$G(z;\theta_G)$`はパラメータ`theta_G$`を持ち、ノイズ`$z \sim p_z(z)$`をデータ空間に射影する写像であり、データ分布`$p_{data}$`と自身の分布`$p_g$`を一致させるように学習する。識別モデル`$D(x;\theta_d)$`はパラメータ`$\theta_d$`を持ち、データ`$x$`が真のデータ分布`$p_{data}$`に属する確率を出力する写像であり、`$p_g$`と`$p_{data}$`を識別するように学習する。このことは以下の式で定式化される。<br>
`\begin{align} \mathop{\rm min}\limits_{G} \mathop{\rm max}\limits_{D} V(D,G)= \mathbb_{x \sim p_{data}} \left[ \log D(x) \right] + \mathbb{E}_{z \sim p_z} \left[ \log (1 - D(G(z))) \right] \end{align}`
したがって、`$D$`は対数尤度`$V$`を最大化するように学習し、`$G$`は`$V$`の第二項にあたる`$G$`に関する対数尤度`$\log(D(G(z)))$`）を最大化するように学習する。

@divend

@div[right]

![](assets/img/Generative_Adversarial_Nets.png =full)<br>
<br>

__リンク__<br>
・[論文](https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf)<br>
・[GitHub](https://github.com/goodfeli/adversarial)<br>

@divend
