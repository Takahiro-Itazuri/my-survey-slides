#### Minimum-Variance Synthetic Discriminant Functions (MVSDF)

@div[left]

最後にsuboptimally factor `$F$`を導入する。<br>
`\begin{align} F &= \frac{\boldsymbol{u}^{T} (\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X})^{-1} \boldsymbol{u}}{\boldsymbol{u}^T (\boldsymbol{X}^T \boldsymbol{X})^{-1} (\boldsymbol{X}^T \boldsymbol{CX}) (\boldsymbol{X}^T \boldsymbol{X})^{-1} \boldsymbol{u}} \\ &= \frac{\boldsymbol{u}^{T} (\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X})^{-1} \boldsymbol{u}}{\boldsymbol{u}^{T} (\boldsymbol{X}^{+} \boldsymbol{C}^{-1} {\boldsymbol{X}^{+}}^{T}) \boldsymbol{u}} \end{align}`
ただし`$ \boldsymbol{X}^{+} $`は一般逆行列である。<br>
`\begin{align} \boldsymbol{X}^{+} = (\boldsymbol{X}^T \boldsymbol{X})^{-1} \boldsymbol{X}^T \end{align}`
ここで学習サンプルが1枚の場合を考える。
`\begin{align} F = \frac{(\boldsymbol{x}^T \boldsymbol{x})^2}{(\boldsymbol{x}^T \boldsymbol{Cx})(\boldsymbol{x}^T \boldsymbol{C}^{-1} \boldsymbol{x})} \end{align}`
ノイズの共分散行列`$\boldsymbol{C}$`の最大固有値と最小固有値によって最悪のケースのsuboptimalityが与えられる。<br>

@divend

@div[right]


@divend
