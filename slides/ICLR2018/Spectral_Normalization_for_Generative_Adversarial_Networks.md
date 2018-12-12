#### Spectral Normalization for Generative Adversarial Networks
###### Takeru Miyato, Toshiki Kataoka, Masanori Koyama, Yuichi Yoshida

@div[left]

__概要__<br>
GANの学習の安定化するため、discriminatorの重みの正規化方法としてspectral normalizationを用いた。spectral normalizationは計算量も軽く、既存の実装に容易に組み込むことが可能である。spectral normalizationを用いたGAN（SNGAN）を用いて、CIFAR10、STL-10、ILSVRC2012のデータセットにおいて画像生成を行った結果、既存の正規化や正則化の手法より高いInception Scoreと低いFIDを実現した。<br>
<br>
__手法・新規性__<br>
従来からdiscriminatorのLipschitz連続性に基づく有界性がGANの学習の安定化に重要であることが提案されてきた。本論文においても、識別器がLipschitz連続な関数にするための正規化方法としてspectral normalizationを導入する。discriminatorを関数`$f$`とし、`$l$`番目の層を`$g_l(h)=W^l h_{l-1}$`とするとき、`$g_l$`のLipschitzノルム`$\|g_l\|_{Lip}$`は`${\rm sup}_h \sigma (\nabla g_l (h))$`と等しい（`$\sigma(A)$`は行列`$A$`のスペクトルノルム）。また活性化関数はReLUのLipschitzノルムは1であることから、関数`$f$`のLipschitzノルム`$\|f\|_{Lip}$`は以下の式のように上からおさえることができる。<br>
`\begin{align} \|f\|_{Lip} \leq \prod_{l=1}^{L+1} \sigma(W^l) \end{align}`
したがって、以下のようにスペクトルノルムで各重み行列を正規化すると、Lipschitz定数が1になるようにすることができる。<br>
`\begin{align} \overline{W}_{SN} = W / \sigma(W) \end{align}`
spectral normalizationをするためには、重み行列`$W$`の最大特異値を計算する必要があるが、べき乗法を用いて高速に近似解を得ることができる。またspectral normalizationを用いた際の勾配を計算すると、特定の方向への敏感な学習を押さえるように正則化項を加えたことに等しいくなる。以上のことから、discriminatorの学習をより安定化することが可能になる。

@divend

@div[right]

![](assets/img/Spectral_Normalization_for_Generative_Adversarial_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1802.05957.pdf)<br>
・[GitHub](https://github.com/pfnet-research/sngan_projection)<br>

@divend