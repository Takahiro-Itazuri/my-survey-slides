#### Unconstrained Minimum Average Correlation Energy (UMACE)

@div[left]

以上より、負のサンプルを含めた基準は以下のようになる。<br>
`\begin{align} J' (\boldsymbol{h}) = \frac{ \boldsymbol{h}^{+} \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} \boldsymbol{h} }{ \boldsymbol{h}^{+} \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right) \boldsymbol{h }} \end{align}`
UMACEは基準`$J'(\boldsymbol{h})$`を最大化させる問題を解く。<br>
`\begin{align} \nabla_{\boldsymbol{h}} \left[ J' (\boldsymbol{h}) \right] = & 2 \frac{ \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} \boldsymbol{h} }{ \boldsymbol{h}^{+} \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right) \boldsymbol{h} } \\ & -2 \frac{ \left( \boldsymbol{h}^{+} \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} \boldsymbol{h} \right) \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right) \boldsymbol{h} }{ \left[ \boldsymbol{h}^{+} \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right) \boldsymbol{h} \right]^2 } = \boldsymbol{0} \\ & \frac{1}{ \boldsymbol{h}^{+} \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right) \boldsymbol{h} } \left[ \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} \boldsymbol{h} - \lambda \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right) \boldsymbol{h} \right] = \boldsymbol{0} \end{align}`
ただし、<br>
`\begin{align} \lambda = \frac{ {bf h}^{+} \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} \boldsymbol{h} }{ \boldsymbol{h}^{+} \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right) \boldsymbol{h} } \end{align}`
上式は以下と等価である。<br>
`\begin{align} \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} \boldsymbol{h} - \lambda \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right) &= \boldsymbol{0} \\ \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right)^{-1} \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} \boldsymbol{h} &= \lambda \boldsymbol{h} \end{align}`

@divend

@div[right]
このとき、`$\boldsymbol{h}$`は`$ \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right)^{-1} \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} $`の固有ベクトルとなる。また`$\lambda = J(\boldsymbol{h})$`なので、`$\boldsymbol{h}$`は最大固有値に対応する固有ベクトルである。さらに`$\boldsymbol{S}_x + \boldsymbol{D}_y$`が対角行列であり、`$\overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+}$`はベクトルの直積であるから、固有値はただ１つしか存在しない。このようにして固有ベクトル`$\boldsymbol{h}$`が得られたとき、`$\overline{\boldsymbol{x}}^{+} \boldsymbol{h} = \alpha$`が自動的に与えられるため、以下のように書きなおすことができる。<br>
`\begin{align} \alpha \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right)^{-1} \overline{\boldsymbol{x}} &= \lambda \boldsymbol{h} \\ \boldsymbol{h} &= c \left( \boldsymbol{S}_x + \boldsymbol{D}_y \right)^{-1} \overline{\boldsymbol{x}} \; \left( c = \frac{\alpha}{\lambda} \right) \end{align}`

またASMは以下のように展開することができる。<br>
`\begin{align} {\rm ASM} &= \boldsymbol{h}^{+} \left[ \frac{1}{N} \sum_{i=1}^{N} \left( \overline{\boldsymbol{X}}_i - \overline{\boldsymbol{X}} \right)^{\ast} \left( \overline{\boldsymbol{X}}_i - \overline{\boldsymbol{X}} \right) \right] \boldsymbol{h} \\ &= \boldsymbol{h}^{+} \left( \frac{1}{N} \sum_{i=1}^{N} \overline{\boldsymbol{X}}_i \overline{\boldsymbol{X}}_i^{\ast} \right) \boldsymbol{h} - \boldsymbol{h}^{+} \overline{\boldsymbol{X}} \overline{\boldsymbol{X}}^{\ast} \boldsymbol{h} \\ \boldsymbol{h}^{+} \boldsymbol{D}_x \boldsymbol{h} - \boldsymbol{h}^{+} \overline{\boldsymbol{X}} \overline{\boldsymbol{X}}^{\ast} \overline{h} \end{align}`
したがって、`$ \boldsymbol{h}^{+} \overline{\boldsymbol{X}} \overline{\boldsymbol{X}}^{\ast} \boldsymbol{h} $`が十分小さいとき、以下のようになる。<br>
`\begin{align} \boldsymbol{h} = \boldsymbol{D} \overline{\boldsymbol{x}} \end{align}`

@divend
