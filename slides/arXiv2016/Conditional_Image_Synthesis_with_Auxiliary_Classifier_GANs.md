#### Conditional Image Synthesis with Auxiliary Classifier with GANs
###### Augustus Odena, Christopher Olah, Jonathon Shlens

@div[left]

__概要__<br>
GANのDiscriminatorの通常のタスクに加えてクラス分類タスクを同時に解かせるネットワーク（AC-GAN：auxiliary classifier GAN）を提案した。ImageNet（1000クラス）のデータセットに対して、global coherenceを保った`$128 \times 128$`の画像の生成に成功し、またCIFAR-10のInception scoreでSoTAを達成した。またdiscriminabilityとdiversityの観点からclass-conditional GANで生成した画像の分析を行った。<br>
<br>
__手法・新規性__<br>
生成器`$G$`はノイズ`$z$`に加えてクラスラベル`$c \sim p_c$`を入力として画像`$X_{fake}=G(c,z)$`を出力する。識別器`$D$`は入力画像が従う分布を推定するタスクに加えて、どのクラスに属するものかを推定するタスクを解く（`$P(S|X), P(C|X) = D(X)$`）。以上を用いて、目的関数は以下の２つの対数尤度からなる。<br>
`\begin{align} L_S &= \mathbb{E} \left[ \log P(S=real|X_{real}) \right] + \mathbb{E} \left[ \log P(S=fake|X_{fake}) \right] \\ L_C &= \mathbb{E} \left[ \log P(C=c|X_{real}) \right] + \mathbb{E} \left[ \log P(C=c|X_{fake}) \right] \end{align}`
`$D$`は`$L_S+L_C$`を最大化するように学習し、`$G$`は`$L_C-L_S$`を最大化するように学習する。ImageNetの画像を生成する際は1000クラスを10クラスごとの100グループに分けて、各グループに対してAC-GANを学習させた。<br>
生成した画像のdiscriminabilityとdiversityの分析の結果、mode collapseしてdiversityがないときに、低品質でdiscriminabilityが低くなることがわかり、従来研究の見解とは異なる結果が得られた。

@divend

@div[right]

![](path/to/img =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1610.09585.pdf)<br>

@divend