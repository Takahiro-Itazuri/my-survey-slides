#### Learning to Detect Fake Images in the Wild
###### Chih-Chung Hsu, Chia-Yen Lee, Yi-Xiu Zhuang

@div[left]

__概要__<br>
画像生成技術の悪用を防ぐ目的で、様々なGANを用いた手法で生成された画像と本物が画像を見分ける識別器（DeepFD: Deep Forgery Discriminator）を提案した。Contrastive Lossを用いることによって、学習データに特定のGAN手法による生成画像を含まない場合でも、テスト時に良い精度を出すことに成功した。<br>
<br>
__手法・新規性__<br>
DeepFDは大きく2つのネットワークに分かれており、1つは識別可能な特徴量を学習する特徴量抽出器（`$D_1$`）ともう1つは`$D_1$`から得た特徴量を用いた識別器（`$D_2$`）である。まず始めの数epochで、`$D_1$`を学習する。損失関数は、CelebAの顔画像（real）とGANで生成された画像（fake）に対して、以下のようなContrastive Lossを取る。<br>
`\begin{align} L(W, (P, x_1, x_2)) &= \frac{1}{2} \left( \left( 1 - p_{ij} \right) (E_W)^2 + p_{ij} \left( {\rm max} (0, m - E_W)^2 \right) \right) \\ E_W (x_1, x_2) &= \| D_1 (x_1) - D_1 (x_2) \| \\ p_{ij} &= \begin{cases} 1 & {\rm fake-fake~or~real-real} \\ 0 & {\rm otherwise} \end{cases} \end{align}`
その後は、`$D_2$`をCross Entropy Lossで学習する。Contrastive Lossを用いて学習するのは、最初の数epochであるが`$D_2$`を学習した後でも、Contrastive Lossは低いままとなる。

@divend

@div[right]

![](assets/img/Learning_to_Detect_Fake_Face_Images_in_the_Wild.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/ftp/arxiv/papers/1809/1809.08754.pdf)<br>

@divend