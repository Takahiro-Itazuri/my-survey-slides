#### Minimum-Variance Synthetic Discriminant Functions (MVSDF)

@div[left]

最後にsuboptimally factor `$F$`を導入する。<br>
`\begin{align} F &= \frac{\boldsymbol{u}^{T} (\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X})^{-1} \boldsymbol{u}}{\boldsymbol{u}^T (\boldsymbol{X}^T \boldsymbol{X})^{-1} (\boldsymbol{X}^T \boldsymbol{CX}) (\boldsymbol{X}^T \boldsymbol{X})^{-1} \boldsymbol{u}} \\ &= \frac{\boldsymbol{u}^{T} (\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X})^{-1} \boldsymbol{u}}{\boldsymbol{u}^{T} (\boldsymbol{X}^{+} \boldsymbol{C}^{-1} {\boldsymbol{X}^{+}}^{T}) \boldsymbol{u}} \end{align}`
ただし`$ \boldsymbol{X}^{+} $`は一般逆行列である。<br>
`\begin{align} \boldsymbol{X}^{+} = (\boldsymbol{X}^T \boldsymbol{X})^{-1} \boldsymbol{X}^T \end{align}`
`$\boldsymbol{h}_{opt}$`は出力の分散を最小化するため、`$\sigma_{SDF}^{2} \geq \sigma_{opt}^{2} $`である。またノイズが白色ノイズであった場合に、`$F$`は1となり、<br>
ここで学習サンプルが1枚の場合を考える。
`\begin{align} F = \frac{(\boldsymbol{x}^T \boldsymbol{x})^2}{(\boldsymbol{x}^T \boldsymbol{Cx})(\boldsymbol{x}^T \boldsymbol{C}^{-1} \boldsymbol{x})} \end{align}`
ノイズの共分散行列`$\boldsymbol{C}$`の最大固有値と最小固有値によって最悪のケースのsuboptimalityが与えられる。<br>
また学習サンプルがすべて直行する場合を考える。これらのベクトルの大きさは1であり、Gram-Schmidtの直交化法を用いることで得ることができる。<br>
`\begin{align} F = \frac{\boldsymbol{u}^{T} (\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X})^{-1} \boldsymbol{u}}{\boldsymbol{u}^{T} (\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X}) \boldsymbol{u}} \end{align}`
以上から、より簡単な表現を得ることができる。

@divend

@div[right]

学習サンプルが固有ベクトルである場合、上述の学習サンプルが直行する場合の議論は一般性を失わない。また`$\boldsymbol{C}$`はすべての要素が正かつ対称であるため、正の固有値`$\alpha_i$`とそれに対応する固有ベクトル`$\boldsymbol{e}_i$`が存在する。このとき以下が成り立つ。<br>
`\begin{align} \boldsymbol{X}^{T} \boldsymbol{CX} &= {\rm diag} (\alpha_{j_1}, \cdots, \alpha_{j_N}) \\ ( \boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X} )^{-1} &= {\rm diag} (\alpha_{j_1}, \cdots, \alpha_{j_N}) \end{align}`
以上より、どんな制約下でも`$F=1$`とする学習サンプルが存在することがわかる。またMVSDFの最適解とSDFの解が一致する学習サンプルが存在する。

@divend
