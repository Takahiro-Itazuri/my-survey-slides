#### Unconstrained Minimum Average Correlation Energy (UMACE)

@div[left]

以上より、負のサンプルを含めた基準は以下のようになる。<br>
`\begin{align} J' (\overline{h}) = \frac{ \overline{h}^{+} \overline{\overline{x}} \overline{\overline{x}}^{+} \overline{h} }{ \overline{h}^{+} \left( \overline{S}_x + \overline{D}_y \right) \overline{h }} \end{align}`
UMACEは基準`$J'(\overline{h})$`を最大化させる問題を解く。<br>
`\begin{align} \nabla_{\overline{h}} \left[ J' (\overline{h}) \right] &= 2 \frac{ \overline{\overline{x}} \overline{\overline{x}}^{+} \overline{h} }{ \overline{h}^{+} \left( \overline{S}_x + \overline{D}_y \right) \overline{h} } - 2 \frac{ \left( \overline{h}^{+} \overline{\overline{x}} \overline{\overline{x}}^{+} \overline{h} \right) \left( \overline{S}_x + \overline{D}_y \right) \overline{h} }{ \left[ \overline{h}^{+} \left( \overline{S}_x + \overline{D}_y \right) \overline{h} \right]^2 } = \overline{0} \\ \frac{1}{ \overline{h}^{+} \left( \overline{S}_x + \overline{D}_y \right) \overline{h} } \left[ \overline{\overline{x}} \overline{\overline{x}}^{+} \overline{h} - \lambda \left( \overline{S}_x + \overline{D}_y \right) \overline{h} \right] = \overline{0} \end{align}`
ただし、<br>
`\begin{align} \lambda = \frac{ {bf h}^{+} \overline{\overline{x}} \overline{\overline{x}}^{+} \overline{h} }{ \overline{h}^{+} \left( \overline{S}_x + \overline{D}_y \right) \overline{h} } \end{align}`
上式は以下と等価である。<br>
`\begin{align} \overline{\overline{x}} \overlin{\overline{x}}^{+} \overline{h} - \lambda \left( \overline{S}_x + \overline{D}_y \right) &= \overline{0} \\ \left( \overline{S}_x + \overline{D}_y \right)^{-1} \overline{\overline{x}} \overline{\overline{x}}^{+} \overline{h} &= \lambda \overline{h} \end{align}`
このとき、`$\overline{h}$`は`$ \left( \overline{S}_x + \overline{D}_y \right)^{-1} \overline{\overline{x}} \overline{\overline{x}}^{+} $`の固有ベクトルとなる。また`$\lambda = J(\overline{h})$`なので、`$\overline{h}$`は最大固有値に対応する固有ベクトルである。さらに`$\overline{S}_x + \overline{D}_y$`が対角行列であり、`$\overline{\overline{x}} \overline{\overline{x}}^{+}$`はベクトルの直積であるから、固有値はただ１つしか存在しない。このようにして固有ベクトル`$\overline{h}$`が得られたとき、`$\overline{\overline{x}}^{+} \overline{h} = \alpha$`が自動的に与えられるため、以下のように書きなおすことができる。<br>
`\begin{align} \alpha \left( \overline{S}_x + \overline{D}_y \right)^{-1} \overline{\overline{x}} &= \lambda \overline{h} \\ \overline{h} &= c \left( \overline{S}_x + \overline{D}_y \right)^{-1} \overline{\overline{x}} \; \left( c = \frac{\alpha}{\lambda} \right) \end{align}`

@divend

@div[right]

またASMは以下のように展開することができる。<br>
`\begin{align} {\rm ASM} &= \overline{h}^{+} \left[ \frac{1}{N} \sum_{i=1}^{N} \left( \overline{X}_i - \overline{\overline{X} \right)^{\ast} \left( \overline{X}_i - \overline{\overline{X} \right) \right] \overline{h} \\ &= \overline{h}^{+} \left( \frac{1}{}N} \sum_{i=1}^{N} \overline{X}_i \overline{X}_i^{\ast} \right) \overline{h} - \overline{h}^{+} \overline{\overline{X}} \overline{\overline{X}}^{\ast} \overline{h} \\ \overline{h}^{+} \overline{D}_x \overline{h} - \overline{h}^{+} \overline{\overline{X}} \overline{\overline{X}}^{\ast} \overline{h} \end{align}`
したがって、`$ \overline{h}^{+} \overline{\overline{X}} \overline{\overline{X}}^{\ast} \overline{h} $`が十分小さいとき、以下のようになる。<br>
`\begin{align} \overline{h} = \overline{D} \overline{\overline{x}} \end{align}`

@divend
