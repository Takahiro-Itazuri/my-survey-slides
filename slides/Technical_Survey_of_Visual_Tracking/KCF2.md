#### Kernelized Correlation Filters (KCF)

@div[left]

__導出__<br>
(1) 線形回帰<br>
MSEを最小化する最適化問題<br>
`\begin{align} \mathop{\rm min}\limits_{{\bf w}} \sum_i \left( {\bf w}^T {\bf x}_i - y_i \right)^2 + \lambda \| {\bf w} \|^2 \end{align}`
上記の問題のclosed formに以下のように求まる。<br>
`\begin{align} {\bf w} = \left( {\bf X}^T {\bf X} + \lambda {\bf I} \right)^{-1} {\bf X}^T {\bf y} \end{align}`
ただし`${\bf X} = \left( {\bf x}_1, {\bf x}_2, \cdots, {\bf x}_n \right)$`である。これの複素数で考えると以下のようになる。<br>
`\begin{align} {\bf w} = \left( {\bf X}^H {\bf X} + \lambda {\bf I} \right)^{-1} {\bf X}^H {\bf y} \end{align}`
ただし`$X^H$`はエルミート転置である。<br>
Correlation Filterにおいて重要な点として行列`${\bf X}$`がベクトル`${\bf x}$`の巡回行列であることである。ここで巡回シフト演算子`${\bf P}$`は以下で与えられる。<br>
`\begin{align} {\bf P} = \begin{bmatrix} 0 & 0 & 0 & \cdots & 1 \\ 1 & 0 & 0 & \cdots & 0 \\ 0 & 1 & 0 & \cdots & 0 \\ \vdots & \vdots & ddots & ddots & vdots \\ 0 & 0 & \cdots & 1 & 0 \end{bmatrix} \end{align}`

@divend

@div[right]

以上から巡回行列`$X$`は以下で与えられる。


@divend