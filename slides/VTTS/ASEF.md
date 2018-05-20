#### Average of Synthetic Exact Filters (ASEF)

@div[left]

__概要__<br>
SDFは学習画像サンプルごとに１つのレスポンス値を設定するが、ASEFは学習画像サンプルごとに１つのレスポンス画像を設定することができる。このレスポンス画像では各位置で任意のレスポンス値を設定する。その結果、１つの学習画像サンプルに設定するレスポンス値の数とフィルタの自由度が同じであるため、１つの学習サンプルのみからフィルタを作ることができる。またオーバーフィッティングを避けるため、複数枚の学習サンプルに対して平均を取る。<br>
<br>
__手法__<br>
畳み込み定理より、空間領域のCross-Correlationは、フーリエ領域の要素ごとの積に変換することができる。<br>
`\begin{align} g(x, y) &= (f \star h) (x, y) = \mathcal{F}^{-1} \left( F(\omega, \nu) H^{\ast}(\omega, \nu) \right) \\ G(\omega, \nu) &= F(\omega, \nu) H^{\ast}(\omega, \nu) \end{align}`
各学習画像サンプル`$i$`ごとにフィルタを計算するができる（除算は要素ごと）。<br>
`\begin{align} H_i^{\ast}(\omega) &= \frac{G_i (\omega, \nu)}{F_i (\omega, \nu)} \end{align}`
左図のように、各学習サンプルごとに得られるフィルタは十分な特徴を含まないが、複数枚のフィルタの平均を取ることで学習サンプルに普遍的な特徴を得られる（バギングと同様）。<br>
`\begin{align} H_{\mu}^{\ast}(\omega, \nu) &= \frac{1}{N} \sum_{i=1}^{N} H_i^{\ast}(\omega, \nu) \\ h_{\mu} (x, y) &= \frac{1}{N} \sum_{i=1}^{N} h_i (x, y) \end{align}`

@divend

@div[right]

![ASEF](assets/img/ASEF.png)

@divend