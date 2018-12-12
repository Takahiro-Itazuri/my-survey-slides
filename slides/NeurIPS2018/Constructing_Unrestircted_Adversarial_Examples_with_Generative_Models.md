#### Constructing Unrestricted Adversarial Examples with Generative Models
###### Yang Song, Rui Shu, Nake Kushman, Stefano Ermon

@div[left]

__概要__<br>
従来の入力画像に微小な摂動を加えるタイプのperturbation-based adversarial examplesとは異なり、conditional generative modelsを用いてスクラッチからadversarial examples (unrestricted adversarial examples) を合成した。元のクラスとしての見た目を保持していることを保証するために、人間による評価を行った。またperturbation-based adversarial examplesと同様にtransfersabilityがあることを確認した。<br>
<br>
__手法・新規性__<br>
perturbation-based adversarial examples `$\mathcal{A}_p$`は以下のように定義できる。<br>
`\begin{align} \mathcal{A}_p =: \left\{ x \in \mathcal{O} | \exists x' \in \mathcal{T}, \|x - x'\| \leq \epsilon \land f(x') = o(x') = o(x) \neq f(x) \right\} \end{align}`
これに対して、提案するunrestricted adversarial examplesは広義である。<br>
`\begin{align} \mathcal{A}_u =: \left\{ x \in \mathcal{O} | o(x) \neq f(x) \right\} \end{align}`
unrestricted adversarial examplesを生成するため、まずauxiliary classifier付きのconditional WGANを学習させる。このGANのgeneratorを`$g_{\theta}$`、criticを`$d_{\phi}$`、auxiliary classifierを`$c_{\psi}$`、ターゲットとするclassifierを`$f$`とするとき、以下の損失関数を最小化する。<br>
`\begin{align} \mathcal{L} &=: \mathcal{L}_0 + \lambda_1 \mathcal{L}_1 + \lambda_2 \mathcal{L}_2 \\ \mathcal{L}_0 &=: - \log f(y_{\rm target} | g_{\theta} (z, y_{\rm source})) \\ \mathcal{L}_1 &=: \frac{1}{m} \sum_{i=1}^{m} \max \left\{ |z_i - z_i^0| - \epsilon, 0 \right\} \\ \mathcal{L}_2 &=: - \log c_{\phi} (y_{\rm source}|g_{\theta} (z, y_{\rm source})) \end{align}`

@divend

@div[right]

![](assets/img/Constructing_Unrestircted_Adversarial_Examples_with_Generative_Models.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1805.07894.pdf)<br>
・[GitHub](https://github.com/ermongroup/generative_adversary)<br>

@divend