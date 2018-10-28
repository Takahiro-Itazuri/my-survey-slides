#### Spectral Normalization for Generative Adversarial Networks
###### Takeru Miyato, Toshiki Kataoka, Masanori Koyama, Yuichi Yoshida

@div[left]

__概要__<br>
GANの学習の安定化するため、Discriminatorの重みの正規化方法としてSpectral Normalizationを提案した。Spectral Normalizationは計算量も軽く、既存の実装に容易に組み込むことが可能である。実験では、Spectral Normalizationを用いたGAN（SNGAN）で、CIFAR10、STL-10、ILSVRC2012のデータセットで画像生成を行った結果、既存手法より高いInception Scoreと低いFIDを実現した。<br>
<br>
__手法・新規性__<br>
Discriminatorを関数`$f$`とし、`$l$`番目の層を`$g_l(h)=W^l h_{l-1}$`とする。Spectral Normalizationは関数`$f$`のリプシッツ定数をコントロールする手法である。`$g_l$`のリプシッツノルム`$\|g_l\|_{Lip}$`は`${\rm sup}_h \simga (\nabla g_l (h))$`と等しい（`$\sigma(A)$`は行列`$A$`のスペクトルノルム）。活性化関数はReLUを考えると、リプシッツノルムは1であることがわかる。これにより、関数`$f$`のリプシッツノルム`$\|f\|_{Lip}$`は以下の式のように上からおさえることができる。<br>
`\begin{align} \|f\|_{Lip} = \prod_{l=1}^{L+1} \sigma(W^l) \end{align}`
以下のようにスペクトルノルムで各重み行列を正規化すると、リプシッツ定数が1になるようにすることができる。<br>
`\begin{align} \overline{W}_{SN} = W / \sigma(W) \end{align}`
Spectral Normalizationをするためには、重み行列`$W$`の最大特異値を計算する必要があるが、べき乗法を用いて高速に近似解を得ることができる。またSpectral Normalizationを用いた際の勾配を計算すると、特定の方向への敏感な学習を押さえるように正則化項を加えたことに等しいことを導くことができる。以上のことから、Discriminatorの学習をより安定化することが可能になる。

@divend

@div[right]

![](assets/img/Spectral_Normalization_for_Generative_Adversarial_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1802.05957.pdf)<br>
・[GitHub](https://github.com/pfnet-research/sngan_projection)<br>

@divend