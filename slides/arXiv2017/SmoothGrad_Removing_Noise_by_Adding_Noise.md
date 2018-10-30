#### SmoothGrad: Removing Noise by Adding Noise
###### Daniel Smikov, Nikhil Thorat, Been Kim, Fernanda Viegas, Martin Wattenberg

@div[left]

__概要__<br>
画像クラス識別問題における勾配情報を利用した手法で生成したsensitivity mapはノイズが大きく、どのピクセルが本当に識別問題に寄与しているのかを判断するのは困難である。そこで、入力画像に対して微小なノイズを加えて入力画像に類似した画像を大量に生成し、それらすべてに対して計算した勾配情報で平均化を行うと、sansitivity mapのノイズが除去できるSmoothGradを提案した。<br>
<br>
__手法・新規性__<br>
`$C$`クラス分類問題において、各クラスの活性化関数を`$S_c$`とすると、最終的な識別結果は以下のように計算される。<br>
`\begin{align} class(x) = \mathop{\rm arg~max}_{c \in C} S_c(x) \end{align}`
既存手法は偏微分情報を使って、以下のようにsensitivity mapを構築する。<br>
`\begin{align} M_c(x) = \frac{\partial S_c (x)}{\partial x} \end{align}`
これは入力画像のそれぞれのピクセル微小な変動が、出力にどれだけ影響を与えるかを表している。しかし、ReLU関数のような微分が不連続な関数を導入している時点でこの偏微分は連続であることを保証していない。実際に、特定のピクセルに微小な変動を加えると偏微分は大きく変動する。したがって、入力画像に対する近傍に対する変微分の平均を取る方がより重要な部分のみが出てくると考え、以下のようにしてsensitivity mapを構築する。<br>
`\begin{align} \hat{M}_c (x) = \frac{1}{n} \sum M_c (x + \mathcal{N} (0, \sigma^2) ) \end{align}`

@divend

@div[right]

![](assets/img/SmoothGrad_Removing_Noise_by_Adding_Noise.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1706.03825.pdf)<br>
・[プロジェクト](https://pair-code.github.io/saliency/)<br>
・[GitHub](https://github.com/pair-code/saliency)

@divend