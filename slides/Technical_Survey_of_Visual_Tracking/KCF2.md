#### Kernelized Correlation Filters (KCF)

@div[left]

__導出__<br>
(1) リッジ線形回帰<br>
MSEを最小化する最適化問題<br>
`\begin{align} \mathop{\rm min}\limits_{{\bf w}} \sum_i \left( {\bf w}^T {\bf x}_i - y_i \right)^2 + \lambda \| {\bf w} \|^2 \end{align}`
上記の問題のclosed formに以下のように求まる。<br>
`\begin{align} {\bf w} = \left( {\bf X}^T {\bf X} + \lambda {\bf I} \right)^{-1} {\bf X}^T {\bf y} \end{align}`
ただし`${\bf X} = \left( {\bf x}_1, {\bf x}_2, \cdots, {\bf x}_n \right)^T$`である。これの複素数で考えると以下のようになる。<br>
`\begin{align} {\bf w} = \left( {\bf X}^H {\bf X} + \lambda {\bf I} \right)^{-1} {\bf X}^H {\bf y} \end{align}`
ただし`$X^H$`はエルミート転置である。<br>
Correlation Filterにおいて重要な点として行列`${\bf X}$`がベクトル`${\bf x}$`の巡回行列であることである。ここで巡回シフト演算子`${\bf P}$`は以下で与えられる。<br>
`\begin{align} {\bf P} = \begin{bmatrix} 0 & 0 & 0 & \cdots & 1 \\ 1 & 0 & 0 & \cdots & 0 \\ 0 & 1 & 0 & \cdots & 0 \\ \vdots & \vdots & \ddots & \ddots & \vdots \\ 0 & 0 & \cdots & 1 & 0 \end{bmatrix} \end{align}`
以上から巡回行列`${\bf X}$`は以下で与えられる。<br>
`\begin{align} {\bf X} = C({\bf X}) = \begin{bmatrix} ({\bf P}^0 {\bf x})^T \\ ({\bf P}^1 {\bf x})^T \\ ({\bf P}^2 {\bf x})^T \\ \vdots \\ ({\bf P}^{n-1} {\bf x})^T \end{bmatrix} \end{align}`

@divend

@div[right]

さらに、この巡回行列`${\bf X}$`はベクトル`${\bf x}$`のDFT`$\hat{{\bf x}}$`とDFT行列`${\bf F}$`を用いて以下で与えられる（証明は[こちら](http://takahiro-itazuri.hatenadiary.jp/entry/2018/03/11/162122)）。<br>
`\begin{align} {\bf X} = {\bf F} {\rm diag} (\hat{{\bf x}}) {\bf F}^H \end{align}`
以上から`${\bf X}^H {\bf X}$`は以下で与えられる。<br>
`\begin{align} {\bf X}^H {\bf X} &= {\bf F} {\rm diag} (\hat{{\bf x}}^{\ast}) {\bf F}^H {\bf F} {\rm diag} (\hat{{\bf x}}) {\bf F}^H \\  &= {\bf F} {\rm diag} (\hat{{\bf x}}^{\ast}) {\rm diag} (\hat{{\bf x}}) {\bf F}^H \\ &= {\bf F} {\rm diag} (\hat{{\bf x}}^{\ast} \odot \hat{{\bf x}}) {\bf F}^H \end{align}`
ここでリッジ回帰の解に立ち返る。<br>
`\begin{align} {\bf w} &= \left( {\bf F} {\rm diag} (\hat{{\bf x}}^{\ast} \odot \hat{{\bf x}}) {\bf F}^H + \lambda {\bf I} \right)^{-1} {bf X}^H {\bf y} \\ &= \left( {\bf F} {\rm diag} (\hat{{\bf x}}^{\ast} \odot \hat{{\bf x}}) {\bf F}^H + \lambda {\bf F} {\bf I} {\bf F}^H \right)^{-1} {bf X}^H {\bf y} \\ &= \left( {\bf F} {\rm diag} (\hat{{\bf x}}^{\ast} \odot \hat{{\bf x}} + \lambda)^{-1} {\bf F}^H \right) {\bf X}^H {\bf y} \\ &= \left( {\bf F} {\rm diag} (\hat{{\bf x}}^{\ast} \odot \hat{{\bf x}} + \lambda)^{-1} {\bf F}^H \right) {\bf F} {\rm diag} (\hat{{\bf x}}^{\ast}) {\bf F}^H {\bf y} \\ &= \left( {\bf F} {\rm diag} \frac{\hat{{\bf x}}^{\ast}}{\hat{{\bf x}}^{\ast} \odot \hat{{\bf x}} + \lambda} {\bf F}^H \right) {\bf y} \end{align}`
上式に左からDFT行列をかけると、以下の式が得られる。<br>
`\begin{align} {\bf F} {\bf w} &= {\rm diag} \left( \frac{\hat{{\bf x}}^{\ast}}{\hat{{\bf x}}^{\ast} \odot \hat{{\bf x}} + \lambda} \right) {\bf F} {\bf y} \\ \hat{{\bf w}} = {\rm diag} \left( \frac{\hat{{\bf x}}^{\ast}}{\hat{{\bf x}}^{\ast} \odot \hat{{\bf x}} + \lambda} \right) \hat{{\bf y}} \\ \hat{{\bf w}} &= \frac{\hat{{\bf x}}^{\ast} \odot \hat{{\bf y}}}{\hat{{\bf x}}^{\ast} \odot \hat{{\bf x}} + \lambda} \end{align}`

@divend