#### Minimum-Variance Synthetic Discriminant Functions (MVSDF)

@div[left]

__概要__<br>
SDFは様々な変形に対応できる一方で、学習サンプルの質に大きく依存している。これまでSDFの限界について言及されてこなかったため、本論文では、学習サンプル上に乗っているであろうノイズに着目して、SDFの一般化した定式化を行った。<br>
<br>
__手法__<br>
まず平均0のノイズベクトル`$\boldsymbol{n}$`が学習サンプルに乗っていると仮定する。また従来のSDFと同様にノイズが載っていない学習サンプル`$ \boldsymbol{x}_i $`に対して定数値`$u_j$`が得られるとする。しかし、実際はノイズによる寄与`$y (= \boldsymbol{h}^T \boldsymbol{n}) $`が発生する。この寄与`$y$`は以下の性質を示す。<br>
`\begin{align} E[y] &= 0 \\ Var[y] &= E[\boldsymbol{h}^T \boldsymbol{n} \boldsymbol{n}^T \boldsymbol{h} ] = \boldsymbol{h}^T E[ \boldsymbol{n} \boldsymbol{n}^T ] \boldsymbol{h} = \boldsymbol{h}^T \boldsymbol{C} \boldsymbol{h} \end{align}`
このノイズによる寄与を上述の制約下で最小化する問題に帰着することができる。ラグランジュの未定乗数法を用いると、以下のように再定式化が可能である。<br>
`\begin{align} L &= \boldsymbol{h}^T \boldsymbol{C} \boldsymbol{h} - \sum_{i=1}^{N}  2 \lambda_i ( \boldsymbol{h}^T \boldsymbol{x}_i ) \\ \boldsymbol{C} \boldsymbol{h}_{opt} &= \sum_{i=1}^{N} \lambda_1 \boldsymbol{x}_i \\  \boldsymbol{h}_{opt} &= \sum_{i=1}^{N} \lambda_i \boldsymbol{C}^{-1} \boldsymbol{x}_{i} \end{align}`

@divend

@div[right]
<br>
以上の式を行列形式に変換すると、以下のようになる。<br>
`\begin{align} \boldsymbol{h}_{opt} &= \boldsymbol{C}^{-1} \boldsymbol{X} \boldsymbol{\Lambda} \\ \boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X} \boldsymbol{\Lambda} &= \boldsymbol{u} \end{align}`
ただし<br>
`\begin{align} \boldsymbol{X} &= \begin{pmatrix} \boldsymbol{x}_1 & \boldsymbol{x}_2 & \cdots & \boldsymbol{x}_{N} \end{pmatrix} \\ \boldsymbol{\Lambda} &= { \begin{pmatrix} \lambda_1 & \lambda_2 & \cdots & \lambda_N \end{pmatrix} }^T \\ \boldsymbol{u} &= { \begin{pmatrix} u_1 & u_2 & \cdots & u_N \end{pmatrix} }^T \end{align}`
`$\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X}$`は正則なので、`$\boldsymbol{\Lambda}$`は一意に求まる。<br>
ここでノイズが分散`$\sigma^2$`の白色ノイズであった場合、`$\boldsymbol{C} = \sigma^2 \boldsymbol{I} $`であるので、従来のSDFと等価であることが確認できる。しかし、実際のノイズは白色であるとは限らないため、`$ \boldsymbol{C}^{-1} $`の計算は計算量が大きい。
`\begin{align} \sigma_{opt}^2 &= \boldsymbol{h}_{opt}^{T} \boldsymbol{C} \boldsymbol{h}_{opt} = ( \boldsymbol{C}^{-1} \boldsymbol{X} \boldsymbol{\Lambda} )^{T} \boldsymbol{C} ( \boldsymbol{C}^{-1} \boldsymbol{X} \boldsymbol{\Lambda} ) \\ &= \boldsymbol{\Lambda}^{T} \boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X} \boldsymbol{\Lambda} \\ &= [( \boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X} )^{-1} \boldsymbol{u}]^T (\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X}) [( \boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X} )^{-1} \boldsymbol{u}] \\ &= \boldsymbol{u}^T ( \boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X} )^{-1}  (\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X}) ( \boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X} )^{-1} \boldsymbol{u} \\ &= \boldsymbol{u}^{T} (\boldsymbol{X}^{T} \boldsymbol{C}^{-1} \boldsymbol{X})^{-1} \boldsymbol{u} \\ \sigma_{SDF}^{2} &= \boldsymbol{h}_{SDF}^{T} \boldsymbol{C} \boldsymbol{h}_{SDf} \\ &= \frac{1}{\sigma^4} \boldsymbol{\Lambda}^T \boldsymbol{X}^{T} \boldsymbol{C X \Lambda} \\ &= [(\boldsymbol{X}^T \boldsymbol{X})^{-1} \boldsymbol{u}]^{T} \boldsymbol{X}^T \boldsymbol{CX} [(\boldsymbol{X}^T \boldsymbol{X})^{-1} \boldsymbol{u}] \\ &= \boldsymbol{u}^T (\boldsymbol{X}^T \boldsymbol{X})^{-1} (\boldsymbol{X}^T \boldsymbol{CX}) (\boldsymbol{X}^T \boldsymbol{X})^{-1} \boldsymbol{u} \end{align}`

@divend
