#### Synthetic Discriminant Function (SDF)

@div[left]

__手法__<br>
与えられた学習サンプル`$\boldsymbol{x}_i$`（ベクトル化済み）に対し、次のような制約を与える。<br>
`\begin{align} u_i = \boldsymbol{h}^T \boldsymbol{x}_i \end{align}`
ただし<br>
`\begin{align} u_i &= 0 & {\rm (negative \;\; sample)} \\ u_i &= 1 & {\rm (positive \;\; sample)} \end{align}`
しかし、与えられた学習画像の枚数が`$\boldsymbol{w}$`の自由度より小さい場合、解が一意に定まらない。そこでSDFは`$\boldsymbol{h}$`が学習サンプル`$\boldsymbol{x}_i$`の線型結合で与えられるという追加の制約を設ける。<br>
`\begin{align} \boldsymbol{h} &= \sum_{i=1}^{N} a_i \boldsymbol{x}_i \\ &= a_1 \boldsymbol{x}_1 + a_2 \boldsymbol{x}_2 + \cdots + a_N \boldsymbol{x}_N  \end{align}`
以上より、上述の制約条件を満たす係数`$ a_1, a_2, \cdots, a_N $`を求める問題に帰着する。<br>
`\begin{align} \sum_{i=1}^{N} a_i \left( \boldsymbol{x}_i^T \boldsymbol{x}_j \right) &= u_j \\ \boldsymbol{X}^T \boldsymbol{X} \boldsymbol{a} &= \boldsymbol{u} & \left( X = \begin{pmatrix} \boldsymbol{x}_1 & \boldsymbol{x}_2 & \cdots & \boldsymbol{x}_N \end{pmatrix} \right) \end{align}`
ただし、行列`$\boldsymbol{X}^T \boldsymbol{X}$`はフルランクでない可能性があるため、Gram-Schmidtの直交化法などを用いて、行列`$ \boldsymbol{X}^T \boldsymbol{X} $`を正則にする必要がある。

@divend

@div[right]

@divend
