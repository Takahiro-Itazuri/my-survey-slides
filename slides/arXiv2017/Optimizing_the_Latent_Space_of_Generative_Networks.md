#### Optimizing the Latent Space of Generative Networks
###### Piotr Bojanowski, Armand Joulin, David Lopez-Paz, Arthur Szlam

@div[left]

__概要__<br>
GANはなぜ成功するのかを紐解き、それに基づいてDiscriminatorを用いずにGeneratorを学習させることが可能なフレームワーク（GLO: Generative Latent Optimization）を提案した。GLOは、Discriminatorを持たないGAN、Encoderを持たないAutoencoderと捉えることが可能である。GANの強みである潜在変数空間上での補間や潜在変数に対する線形演算が可能であることを実験で示した（個人的にはあまり上手くいっていないように見える）。<br>
<br>
__手法・新規性__<br>
GLOはまず大規模の画像データセット`$\left\{ x_1, \cdots, x_N \right\}$`に対して、初期化した`$d$`次元ベクトル`$\left\{ z_1, \cdots, z_N \right\}$`をそれぞれ割り当て、データセット`$\left\{ (z_1, x_1), \cdots, (z_N, x_N) \right\}$`を作成する。これに対して、以下の最適化問題を解くことで、生成モデル`$g_{\theta}$`を得る。<br>
`\begin{align} \mathop{\rm min}\limits_{\theta \in \Theta} \frac{1}{N} \sum_i^N \left[ \mathop{\rm min}\limits_{z_i \in \mathcal{Z}} l (g_{\theta}(z_i), x_i) \right] \end{align}`
GLOは生成モデルのパラメータ`$\theta$`と各画像に割り当たられた入力ベクトル`$z_i$`を同時最適化する。Autoencoderは入力画像から中間表現となる`$z$`をEncoderにより推定していたが、GLOでは`$z$`は完全に自由なパラメータである。また損失にはLaplacian pyramid `$Lap_1$` lossを用いる。<br>
`\begin{align} Lap_1 (x, x') = \sum_j 2^{-2j} | L^j (x) - L^j (x') |_1 \end{align}`
`$z$`を更新した後、表現空間として選んだ`$\mathcal{Z}$`（`$d$`次元単位球）から外れたものを強制的に戻す操作を行う。


@divend

@div[right]

![](assets/img/Optimizing_the_Latent_Space_of_Generative_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/abs/1707.05776)<br>
・[GitHub](https://github.com/gitlimlab/Generative-Latent-Optimization-Tensorflow)<br>

@divend