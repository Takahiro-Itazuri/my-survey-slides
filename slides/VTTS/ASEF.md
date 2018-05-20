#### Average of Synthetic Exact Filters (ASEF)

@div[left]

__概要__<br>
SDFは学習画像サンプルごとに１つのレスポンス値を設定するが、ASEFは学習画像サンプルごとに１つのレスポンス画像を設定することができる。このレスポンス画像では各位置で任意のレスポンス値を設定する。その結果、１つの学習画像サンプルに設定するレスポンス値の数とフィルタの自由度が同じであるため、１つの学習サンプルのみからフィルタを作ることができる。またオーバーフィッティングを避けるため、複数枚の学習サンプルに対して平均を取る。<br>
`\begin{align} g(x, y) &= (f \otimes h) (x, y) = \mathcal{F}^{-1} \left( F(\omega, \nu) H(\omega, \nu) \right) \\ G(\omega, \nu) &= F(\omega, \nu) H^{\ast}(\omega, \nu) \\ H_i^{\ast}(\omega) &= \frac{G_i (\omega, \nu)}{F_i (\omega, \nu)} \end{align}`

@divend

@div[right]

![ASEF](assets/img/ASEF.png)

@divend