#### Autoencoding Beyond Pixels using a Learned Similarity Metric
###### 	Anders Boesen Lindbo Larsen, 	Søren Kaae Sønderby, 	Hugo Larochelle, 	Ole Winther

@div[left]

__概要__<br>
VAEのような学習モデルを学習する場合、再構成誤差を測るための類似度尺度の選択が重要である。最も単純な手法では二乗誤差を用いるが、二乗誤差は画像を対象とするには適していない。そこで本論文では、VAEの再構成誤差を測る尺度としてGANを用いることで、抽象的な類似度を考えることが可能なVAE/GANを提案した。<br>
<br>
__手法・新規性__<br>
通常のVAEの損失関数は以下の通り。<br>
`\begin{align} \mathcal{L}_{VAE} &= - \mathbb{E}_{q(z|x)} \left[ \frac{p(x|z)p(z)}{q(z|x)} \right] = \mathcal{L}_{like}^{pixel} + \mathcal{L}_{prior} \\ \mathcal{L}_{like}^{pixel} &= - \mathbb{E}_{q(z|x)} \left[ \log p(x|z) \right] \\ \mathcal{L}_{prior} &= D_{KL} (q(z|x) || p(z)) \end{align}`
また通常のGANの損失関数は以下の通り。<br>
`\begin{align} \mathcal{L}_{GAN} = \log (D(x)) + \log (1 - D(G(z))) \end{align}`
VAE/GANは`$\mathcal{L}_{like}^{pixel}$`の代わりに、Discriminatorのより抽象的な情報を含む層`$l$`に対して、以下のような損失関数を用いる。<br>
`\begin{alingn} \mathcal{L} &= \mathcal{L}_{prior} + \mathcal{L}_{like}^{Dis_l} + \mathcal{L}_{GAN} \\ \mathcal{L}_{like}^{Dis_l} &= - \mathbb{E}_{q(z|x)} \left[ \log p(Dis_l (x)|z) \right] \end{align}`

@divend

@div[right]

![VAE/GAN](assets/img/Autoencoding_Beyond_Pixels_using_a_Learned_Similarity_Metric.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1512.09300.pdf)<br>
・[GitHub](https://github.com/andersbll/autoencoding_beyond_pixels)<br>

@divend