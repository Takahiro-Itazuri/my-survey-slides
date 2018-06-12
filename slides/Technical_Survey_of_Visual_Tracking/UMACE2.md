#### Unconstrained Minimum Average Correlation Energy (UMACE)

@div[left]

以上より、負のサンプルを含めた基準は以下のようになる。<br>
`\begin{align} J' ({\bf h}) = \frac{ {\bf h}^{+} \overline{{\bf x}} \overline{{\bf x}}^{+} {\bf h} }{ {\bf h}^{+} \left( {\bf S}_x + {\bf D}_y \right) {\bf h }} \end{align}`
UMACEは基準`$J'({\bf h})$`を最大化させる問題を解く。<br>
`\begin{align} \nabla_{{\bf h}} \left[ J' ({\bf h}) \right] &= 2 \frac{ \overline{{\bf x}} \overline{{\bf x}}^{+} {\bf h} }{ {\bf h}^{+} \left( {\bf S}_x + {\bf D}_y \right) {\bf h} } - 2 \frac{ \left( {\bf h}^{+} \overline{{\bf x}} \overline{{\bf x}}^{+} {\bf h} \right) \left( {\bf S}_x + {\bf D}_y \right) {\bf h} }{ \left[ {\bf h}^{+} \left( {\bf S}_x + {\bf D}_y \right) {\bf h} \right]^2 } = {\bf 0} \\ \frac{1}{ {\bf h}^{+} \left( {\bf S}_x + {\bf D}_y \right) {\bf h} } \left[ \overline{{\bf x}} \overline{{\bf x}}^{+} {\bf h} - \lambda \left( {\bf S}_x + {\bf D}_y \right) {\bf h} \right] = {\bf 0} \end{align}`

`\begin{align} \overline{{\bf x}} \overlin{{\bf x}}^{+} {\bf h} - \lambda \left( {\bf S}_x + {\bf D}_y \right) &= {\bf 0} \\ \left( {\bf S}_x + {\bf D}_y \right)^{-1} \overline{{\bf x}} \overline{{\bf x}}^{+} {\bf h} &= \lambda {\bf h} \end{align}`
このとき、`${\bf h}$`は`$ \left( {\bf S}_x + {\bf D}_y \right)^{-1} \overline{{\bf x}} \overline{{\bf x}}^{+} $`の固有ベクトルとなる。`$\lambda$`

@divend

@div[right]


@divend
