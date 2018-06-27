#### Kernelized Correlation Filters (KCF)

@div[left]

__導出__<br>
(1) リッジ線形回帰<br>
MSEを最小化する最適化問題<br>
`\begin{align} \mathop{\rm min}\limits_{\boldsymbol{w}} \sum_i \left( \boldsymbol{w}^T \boldsymbol{x}_i - y_i \right)^2 + \lambda \| \boldsymbol{w} \|^2 \end{align}`
上記の問題のclosed formに以下のように求まる。<br>
`\begin{align} \boldsymbol{w} = \left( \boldsymbol{X}^T \boldsymbol{X} + \lambda \boldsymbol{I} \right)^{-1} \boldsymbol{X}^T \boldsymbol{y} \end{align}`
ただし`$\boldsymbol{X} = \left( \boldsymbol{x}_1, \boldsymbol{x}_2, \cdots, \boldsymbol{x}_n \right)^T$`である。これの複素数で考えると以下のようになる。<br>
`\begin{align} \boldsymbol{w} = \left( \boldsymbol{X}^H \boldsymbol{X} + \lambda \boldsymbol{I} \right)^{-1} \boldsymbol{X}^H \boldsymbol{y} \end{align}`
ただし`$X^H$`はエルミート転置である。<br>
Correlation Filterにおいて重要な点として行列`$\boldsymbol{X}$`がベクトル`$\boldsymbol{x}$`の巡回行列であることである。ここで巡回シフト演算子`$\boldsymbol{P}$`は以下で与えられる。<br>
`\begin{align} \boldsymbol{P} = \begin{bmatrix} 0 & 0 & 0 & \cdots & 1 \\ 1 & 0 & 0 & \cdots & 0 \\ 0 & 1 & 0 & \cdots & 0 \\ \vdots & \vdots & \ddots & \ddots & \vdots \\ 0 & 0 & \cdots & 1 & 0 \end{bmatrix} \end{align}`
以上から巡回行列`$\boldsymbol{X}$`は以下で与えられる。<br>
`\begin{align} \boldsymbol{X} = C(\boldsymbol{X}) = \begin{bmatrix} (\boldsymbol{P}^0 \boldsymbol{x})^T \\ (\boldsymbol{P}^1 \boldsymbol{x})^T \\ (\boldsymbol{P}^2 \boldsymbol{x})^T \\ \vdots \\ (\boldsymbol{P}^{n-1} \boldsymbol{x})^T \end{bmatrix} \end{align}`

@divend

@div[right]

さらに、この巡回行列`$\boldsymbol{X}$`はベクトル`$\boldsymbol{x}$`のDFT`$\hat{\boldsymbol{x}}$`とDFT行列`$\boldsymbol{F}$`を用いて以下で与えられる（証明は[こちら](http://takahiro-itazuri.hatenadiary.jp/entry/2018/03/11/162122)）。<br>
`\begin{align} \boldsymbol{X} = \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}) \boldsymbol{F}^H \end{align}`
以上から`$\boldsymbol{X}^H \boldsymbol{X}$`は以下で与えられる。<br>
`\begin{align} \boldsymbol{X}^H \boldsymbol{X} &= \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}^{\ast}) \boldsymbol{F}^H \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}) \boldsymbol{F}^H \\  &= \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}^{\ast}) {\rm diag} (\hat{\boldsymbol{x}}) \boldsymbol{F}^H \\ &= \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}}) \boldsymbol{F}^H \end{align}`
ここでリッジ回帰の解に立ち返る。<br>
`\begin{align} \boldsymbol{w} &= \left( \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}}) \boldsymbol{F}^H + \lambda \boldsymbol{I} \right)^{-1} {bf X}^H \boldsymbol{y} \\ &= \left( \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}}) \boldsymbol{F}^H + \lambda \boldsymbol{F} \boldsymbol{I} \boldsymbol{F}^H \right)^{-1} {bf X}^H \boldsymbol{y} \\ &= \left( \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}} + \lambda)^{-1} \boldsymbol{F}^H \right) \boldsymbol{X}^H \boldsymbol{y} \\ &= \left( \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}} + \lambda)^{-1} \boldsymbol{F}^H \right) \boldsymbol{F} {\rm diag} (\hat{\boldsymbol{x}}^{\ast}) \boldsymbol{F}^H \boldsymbol{y} \\ &= \left( \boldsymbol{F} {\rm diag} \frac{\hat{\boldsymbol{x}}^{\ast}}{\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}} + \lambda} \boldsymbol{F}^H \right) \boldsymbol{y} \end{align}`
上式に左からDFT行列をかけると、以下の式が得られる。<br>
`\begin{align} \boldsymbol{F} \boldsymbol{w} &= {\rm diag} \left( \frac{\hat{\boldsymbol{x}}^{\ast}}{\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}} + \lambda} \right) \boldsymbol{F} \boldsymbol{y} \\ \hat{\boldsymbol{w}} &= {\rm diag} \left( \frac{\hat{\boldsymbol{x}}^{\ast}}{\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}} + \lambda} \right) \hat{\boldsymbol{y}} \\ \hat{\boldsymbol{w}} &= \frac{\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{y}}}{\hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}} + \lambda} \end{align}`

@divend