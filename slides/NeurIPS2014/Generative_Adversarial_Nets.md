#### Generative Adversarial Nets
###### Ian J. Goodfellow, Jean Pouget-Abadie, Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozairm Aaron Courville, Yoshua Bengio

@div[left]

__概要__<br>
敵対的プロセスを通して生成モデルを学習する新しいフレームワーク（GAN：Generative Adversarial Nets）を提案した。GANはデータの分布を真似る生成モデル`$G$`と、入力画像が`$G$`が生成したサンプル（fake sample）か本物のデータサンプル（real sample）かの確率を出力する識別モデル`$D$`を同時に学習させる。提案された定式化では`$D$`と`$G$`によるminimax gameとなっており、従来のようにマルコフ連鎖やあらゆる近似を仮定する必要がない。<br>
<br>
__手法・新規性__<br>
生成モデル`$G(z;\theta_G)$`はパラメータ`$\theta_G$`を持ち、ノイズ`$z \sim p_z(z)$`をデータ空間に射影する写像であり、データ分布`$p_{data}$`と`$z \sim p_z$`を射影することで得たデータ分布`$p_g$`を一致させるように学習する。識別モデル`$D(x;\theta_d)$`はパラメータ`$\theta_d$`を持ち、データ`$x$`が真のデータ分布`$p_{data}$`に属する確率を出力する写像であり、`$p_g$`と`$p_{data}$`を識別するように学習する。このことは以下の式で定式化される。<br>
`\begin{align} \mathop{\rm min}\limits_{G} \mathop{\rm max}\limits_{D} V(D,G)= & \mathbb{E}_{x \sim p_{data}} \left[ \log D(x) \right] \\ & + \mathbb{E}_{z \sim p_z} \left[ \log (1 - D(G(z))) \right] \end{align}`
`$D$`の目的は条件付き確率`$P(Y=y|x)$`の尤度を最大化することに相当する。`$G$`が固定されているとき、最適な識別モデル`$D^{\ast}$`は`$D^{\ast}=p_{data}/(p_{data}+p_g)$`で与えられる。`$D^{\ast}$`が与えられたときの`$G$`の目的関数は真のデータ分布`$p_{data}$`と生成モデル`$G$`のデータ分布`$p_g$`のJensen-Shannon divergenceに等しくなることから、`$G$`の最適解は`$p_{data}=p_g$`となる。また`$G$`と`$D$`に十分なキャパシティが与えられたとき、`$D$`は与えられた`$G$`に対する最適解に到達することが可能であり、その上で`$p_g$`は尺度`$V$`を向上させ`$p_{data}$`に収束可能であることを証明した。

@divend

@div[right]

![](assets/img/Generative_Adversarial_Nets.png =full)<br>
<br>

__リンク__<br>
・[論文](https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf)<br>
・[GitHub](https://github.com/goodfeli/adversarial)<br>

@divend
