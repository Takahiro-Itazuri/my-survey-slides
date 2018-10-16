#### Least Squares Generative Adversarial Networks
###### Xudong Mao, Qing Li, Haoran Xie, Raymond Y.K. Lau, Zhen Wang, Stephen Paul Smolley

@div[left]

__概要__<br>
通常のGANのDiscriminatorはSigmoid Cross Entropy Lossを損失関数として用いるが、これは学習過程において勾配消失問題は発生される原因となっていることを指摘し、代わりにLeast Squares Lossを用いたGAN（LSGAN：Least Squares Generative Adversarial Networks）を提案し、安定的なGANの学習を可能にした。学習の安定性の評価に加えて、3740クラスの中国語文字の画像生成にも成功している。<br>
<br>
__手法・新規性__<br>
Sigmoid Cross Entropy Lossを用いると、Discriminatorによって正しく分類された生成画像が本物の画像の分布とかけ離れていても、損失はほぼなくなってしまう。一方で、Least Squares Lossを用いると、決定境界からの距離に応じて損失が生じるため、正しく分類された生成画像に対しても損失が生まれる。通常のGANがJensen-Shannon Divergenceを最小化する問題を解いているのに対して、LSGANはPearson `$\chi^2$` Divergenceを最小化する問題を解いていることに相当する。LSGANの解く問題は以下の式で表される。<br>
`\begin{align} \mathop{\rm min}\limits_{D} V_{LSGAN} (D) &= \frac{1}{2} \mathbb{E}_{x \sim p_{data}} \left[ \left( D(x) - 1 \right)^2 \right] + \frac{1}{2} \mathbb{E}_{z \sim p_z} \left[ \left( D(G(z)) \right)^2 \right] \\ \mathop{\rm min}\limits_{G} V_{LSGAN} (G) &= \frac{1}{2} \mathbb{E}_{z \sim p_z} \left[ \left( D(G(z)) - 1 \right)^2 \right] \end{align}`

@divend

@div[right]

![](assets/img/Least_Squares_Generative_Adversarial_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1611.04076v3.pdf)<br>
・[GitHub](https://github.com/xudonmao/LSGAN)<br>

@divend