#### Mimimum Average Correlation Energy (MACE) Filters

@div[left]

上式を拘束条件の式に代入。<br>
`\begin{align} \boldsymbol{X}^{+} \boldsymbol{D}^{-1} \boldsymbol{X \Lambda} &= \boldsymbol{u} \\ \boldsymbol{\Lambda} = \left( \boldsymbol{X}^{+} \boldsymbol{D}^{-1} \boldsymbol{X} \right)^{-1} \boldsymbol{u} \end{align}`
上式よりフィルタは以下の式で求まる。<br>
`\begin{align} \boldsymbol{H} = \boldsymbol{D}^{-1} \boldsymbol{X} \left( \boldsymbol{X}^{+} \boldsymbol{D}^{-1} \boldsymbol{X} \right)^{-1} \boldsymbol{u} \end{align}`

<b>一般形</b><br>
解の一般形を以下のように定義する。<br>
`\begin{align} \boldsymbol{H} = \boldsymbol{A}^{-1} \boldsymbol{X} \left( \boldsymbol{X}^{+} \boldsymbol{A}^{-1} \boldsymbol{X} \right)^{-1} \boldsymbol{u} \end{align}`
`$\boldsymbol{A}=\boldsymbol{I}$`のとき、フーリエ領域におけるSDFの式となる。また`$\boldsymbol{A} = \boldsymbol{C}^{-1}$`のとき、フーリエ領域におけるMVSDFの式となる。

@divend

@div[right]



@divend
