#### Universal Adversarial Perturbations
###### Seyed-Mohsen Moosavi Dezfooli, Alhussein Fawzi, Omar Fawzi, Pascal Frossard

@div[left]

__概要__<br>
入力画像に依存しないadversarial perturbation（universal adversarial perturbation）を提案した。universal adversarial perturbationが存在することを通して、高次元空間上の識別境界の幾何的な相関性を明らかにした。universal adversarial perturbationは入力画像に依存しないだけでなく、ネットワーク構造にも依存しない。<br>
<br>
__手法・新規性__<br>
入力画像（`$\mathbb{R}^{d}$`）の分布を`$\mu$`、識別器を`$\hat{k}$`とするとき、画像`$x \in \mathbb{R}^d$`の識別結果は`$\hat{k}(x)$`で与えられる。このとき、universal adversarial perturbationは以下のように定義される。<br>
`\begin{align} \hat{k}(x+v) \neq \hat{k}(x)  {\rm \; for \; most \;} x \sim \mu \end{align}`
提案手法は、分布`$\mu$`からサンプリングされた画像集合`$X = \left\{ x_1, \cdots, x_m \right\}$`に対して反復的なアプローチをとる。`$i$`番目のイテレーションにおいて、摂動がのったデータ`$x_i + v$`に対する摂動`$\Delta v_i$`を以下のように求める。<br>
`\begin{align} \Delta v_i \gets \mathop{\rm arg~min}\limits_{r} \|r\|_2 {\rm \; s.t. \;} \hat{k}(x_i + v + r) \neq \hat{k}(x_i) \end{align}`
ただし、摂動の大きさの制約（`$\|v\|_p \leq \xi$`）を満たすために、中心`$0$`で半径`$\xi$`の`$l_p$`球に射影する。<br>
このようなuniversal adversarial perturbationが存在する事実を元に、識別境界までの垂線の方向ベクトルを並べた行列の特異値を計算すると、非常に大きな特異値がいくつか存在していることがわかり、これはどんな入力画像に対しても識別結果が変化しやすい共通の方向が存在することを意味する。<br>

@divend

@div[right]

![](assets/img/Universal_Adversarial_Perturbations.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1610.08401.pdf)<br>
・[GitHub](https://github.com/LTS4/universal)<br>

@divend