#### Minimum-Variance Synthetic Discriminant Functions (MVSDF)

@div[left]

__概要__<br>
従来のSDFはフィルタ`$h$`が学習サンプルの線型結合であるという制約下で問題を解いていたため、ノイズが乗った画像や学習サンプルに含まれない画像が与えられた場合に上手く検出できない。そこで本論文では、学習サンプルにノイズが乗っていることを仮定し、そのノイズを従来の制約下で最小化する最適化問題を解くことで、ノイズが乗った画像でも上手く検出できるMVSDFを提案した。<br>
<br>
__手法__<br>
まず平均0のノイズベクトル`$\boldsymbol{n}$`が学習サンプルに乗っていると仮定する。また従来のSDFと同様にノイズが載っていない学習サンプル`$ \boldsymbol{x}_i $`に対して定数値`$u_j$`が得られるとする。しかし、実際はノイズによる寄与`$y (= \boldsymbol{h}^T \boldsymbol{n}) $`が発生する。この寄与`$y$`は以下の性質を示す。<br>
`\begin{align} E[y] &= 0 \\ &= Var[y] = E[\boldsymbol{h}^T \boldsymbol{n} \boldsymbol{n}^T \boldsymbol{h} ] \\ &= \boldsymbol{h}^T E[ \boldsymbol{n} \boldsymbol{n}^T ] \boldsymbol{h} \\ &= \boldsymbol{h}^T \boldsymbol{C} \boldsymbol{h} \end{align}`
このノイズによる寄与を上述の制約下で最小化する問題に帰着することができる。ラグランジュの未定乗数法を用いると、以下のように再定式化が可能である。<br>
`\begin{align} L &= \boldsymbol{h}^T \boldsymbol{C} \boldsymbol{h} - \sum_{i=1}^{N}  2 \lambda_i ( \boldsymbol{h}^T \boldsymbol{x}_i ) \\ \boldsymbol{C} \boldsymbol{h}_{opt} = \sum_{i=1}^{N} \lambda_1 \boldsymbol{x}_i \end{align}`

@divend

@div[right]


@divend
