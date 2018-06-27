#### Kernelized Correlation Filters (KCF)

@div[left]

__概要__<br>
MOSSEは高速かつ高精度な物体追跡手法である。本論文では、カーネルリッジ回帰と巡回行列の性質を用いて、MOSSEをより一般化させたKernelized Correlation Filters（KCF）を提案する。KCFは非線形カーネルを選択することで、カーネルトリックにより、高精度な分類が可能となる。<br>
<br>
__手法__<br>
カーネルリッジ回帰の一般解はカーネル行列`$K \; (K_{ij} = \kappa (\boldsymbol{x_i}, \boldsymbol{x_j}))$`を用いて以下のようになる。<br>
`\begin{align} \boldsymbol{\alpha} = \left(K + \lambda I \right)^{-1} \boldsymbol{y} \end{align}`
ここでベクトルを１要素巡回させる行列`$P$`を用いて、ベクトル`$\boldsymbol{k}$`を定義する。<br>
`\begin{align} k_i = \kappa \left( \boldsymbol{x}, P^{i} \boldsymbol{x} \right) \end{align}`
ここでKCFは上述の式の右辺の逆行列計算を避けるため、カーネル行列`$K$`が巡回行列であることを利用して、以下のように変形する。<br>
`\begin{align} \boldsymbol{\alpha} = \mathcal{F}^{-1} \left( \frac{ \mathcal{F} (\boldsymbol{y}) }{ \mathcal{F} (\boldsymbol{k}) + \lambda } \right) \end{align}`
以上を利用すると、入力画像`$\boldsymbol{z}$`に対する相関出力`$\hat{\boldsymbol{y}}$`を、ベクトル`$\hat{\boldsymbol{k}} \; \left( \hat{k}_i = \kappa (\boldsymbol{z}, P^{i} \boldsymbol{x}) \right)$`を用いて、以下の式で得ることができる。<br>
`\begin{align} \hat{\boldsymbol{y}} = \mathcal{F}^{-1} \left( \mathcal{F} (\overline{\boldsymbol{k}}) \odot \mathcal{F} (\boldsymbol{\alpha}) \right) \end{align}`

@divend

@div[right]

ベクトル`$\boldsymbol{k}, \hat{\boldsymbol{k}}$`の計算についても巡回行列の性質を用いて、高速化することが可能である。カーネルがドット積である場合（`$\kappa (\boldsymbol{x}, \boldsymbol{x}') = g ( \langle \boldsymbol{x}, \boldsymbol{x}' \rangle)$`）、カーネル`$\boldsymbol{k}^{dp}$`は以下のように変形できる。<br>
`\begin{align} k_i^{dp} = \kappa \left( \boldsymbol{x}, P^{i} \boldsymbol{x}' \right) = g \left( \boldsymbol{x}^{T} P^{i} \boldsymbol{x}' \right) \end{align}`
さらにベクトルから巡回行列を生成する演算子`$C$`を利用して、以下のように変形できる。<br>
`\begin{align} \boldsymbol{k}^{dp} &= g \left( C(\boldsymbol{x}' \boldsymbol{x}) \right) \\ &= g \left( \mathcal{F}^{-1} (\mathcal{F} (\boldsymbol{x}) \odot \mathcal{F}^{\ast} (\boldsymbol{x}') ) \right) \end{align}`
カーネルが放射基底関数である場合（`$\kappa (\boldsymbol{x}, \boldsymbol{x}') = h \left( \|\boldsymbol{x} - \boldsymbol{x}'  \|^2 \right)$`）、カーネル`$\boldsymbol{k}^{rbf}$`以下のように変形できる。<br>
`\begin{align} k_i^{rbf} &= \kappa (\boldsymbol{x}, P^{i} \boldsymbol{x}') = h \left( \| \boldsymbol{x} - P^i \boldsymbol{x}' \|^2 \right) \\ &= h \left( \| \boldsymbol{x} \|^2 + \| \boldsymbol{x}' \|^2 - 2 \boldsymbol{x}^{T} P^{i} \boldsymbol{x}' \right) \\ \boldsymbol{k}^{rbf} &= h \left( \| \boldsymbol{x} \|^2 + \| \boldsymbol{x}' \|^2 - 2 \mathcal{F}^{-1} \left( \mathcal{F} (\boldsymbol{x}) \odot \mathcal{F}^{\ast} (\boldsymbol{x}') \right) \right) \end{align}`
カーネルがガウシアンカーネルである場合は、以下のように変形できる。<br>
`\begin{align} \boldsymbol{k}^{gauss} = \exp \left( - \frac{1}{\sigma^2} \left( \| \boldsymbol{x} \|^2 + \| \boldsymbol{x}' \|^2 - 2 \mathcal{F}^{-1} \left( \mathcal{F} (\boldsymbol{x}) \odot \mathcal{F}^{\ast} (\boldsymbol{x}') \right)  \right) \right) \end{align}`

@divend
