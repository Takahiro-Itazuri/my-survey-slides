#### A3T: Adversarially Augmented Adversarial Training
###### Akram Erraqabi, Aristide Baratin, Yoshua Bengio, Simon Lacoste-Julien

@div[left]

__概要__<br>
Adversarial Examplesに頑健なクラス分類器を学習するために、クラス分類器の中間層に、本物の画像の特徴量かAdversarial Examplesの特徴量かを識別する識別器を持たせ、これを騙すような特徴量を抽出するようにクラス分類器を学習させる手法（A3T）を提案した。proof-of-conceptではあるが、通常の識別器よりもAdversarial Examplesに頑健であることを確認し、Ablation Studyも行った。<br>
<br>
__手法・新規性__<br>
クラス分類器`$C_{\theta}$`に対する入力`$x$`のAdversarial Examples `$x^{adv}$`を以下の式で生成する。<br>
`\begin{align} x^{adv} = x + \epsilon {\rm sign} (\Delta_x \mathcal{L}_{\theta} (x, y)) \end{align}`
またクラス分類器`$C_{\theta}$`を、特徴量抽出をするエンコーダ`$E$`と残りのクラス分類器`$R$`に分ける。エンコーダ`$E$`から得た入力`$x$`の特徴量`$E(x)$`と`$E(x^{adv})$`を識別する識別器`$D$`をつけて、以下の損失関数の元で最適化を行う。<br>
Classification Loss<br>
`\begin{align} \mathcal{L}_{\theta} (x, x^{adv}, y) = - \alpha \log P_{\theta} (y|x) - (1 - \alpha) \log P_{\theta} (y|x^{adv}) \end{align}`
Discriminator Loss<br>
`\begin{align} \mathcal{L}_{\theta_{disc}} (z, t) = - \log P_{\theta_{disc}} (t|z) \end{align}`
Encoder Adversarial Loss<br>
`\begin{align} \mathcal{L}^{adj}_{\theta_{enc}} (x^{adv}) = - \beta \log D(E(x^{adv})) \end{align}`
これによりAdversarial Examplesに頑健な特徴量抽出が可能となる。

@divend

@div[right]

![](assets/img/A3T_Adversarially_Augmented_Adversarial_Training.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1801.04055.pdf)<br>

@divend