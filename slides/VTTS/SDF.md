#### Synthetic Discriminant Function (SDF)

@div[whole]

与えられた学習サンプル`$\boldsymbol{x}_i$`に対して、次のような制約を与える。<br>
`\begin{align} u_i = \boldsymbol{w}^T \boldsymbol{x}_i \end{align}`<br>
ただし<br>
`\begin{align} u_i &= 0 & {\rm (negative \;\; sample)} \\ u_i &= 1 & {\rm (positive \;\; sample)} \end{align}`<br>
<br>
しかし、与えられた学習画像の枚数が`$\boldsymbol{w}$`の自由度より小さい場合、解が一意に定まらない。そこでSDFは`$\boldsymbol{w}$`が学習サンプル`$\boldsymbol{x}_i$`の線型結合で与えられるという追加の制約を設ける。

@divend