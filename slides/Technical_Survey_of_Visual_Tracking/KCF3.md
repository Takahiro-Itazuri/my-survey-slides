#### Kernelized Correlation Filters (KCF)

@div[left]

__導出__<br>
(2) 非線形リッジ回帰<br>
Representer Theoremより、`$\boldsymbol{w}$`は非線形関数`$\boldsymbol{\varphi}(\boldsymbol{x}_i)$`を用いて以下のように記述できる。<br>
`\begin{align} \boldsymbol{w} = \sum_i \alpha_i \boldsymbol{\varphi} (\boldsymbol{x}_i) \end{align}`
ここで以下のようなカーネル関数`$\kappa(\boldsymbol{x}, \boldsymbol{x}')$`を定義する。<br>
`\begin{align} \kappa (\boldsymbol{x}, \boldsymbol{x}') = \boldsymbol{\varphi} (\boldsymbol{x}, \boldsymbol{x}') \end{align}`
すべてのサンプルのペアのカーネル関数を並べたカーネル行列`$\boldsymbol{K}$`を定義する。<br>
`\begin{align} \boldsymbol{K}_{ij} = \kappa (\boldsymbol{x}, \boldsymbol{x}') \end{align}`
このとき高次元非線形関数`$\boldsymbol{\varphi}$`の内積を簡単な式で表せるとき、その高次元非線形関数を求めることなく、カーネル関数を計算すること可能となることをカーネルトリックと呼ぶ。<br>
カーネルリッジ回帰の解は以下で与えられる。<br>
`\begin{align} \boldsymbol{\alpha} = \left( \boldsymbol{K} + \lambda \boldsymbol{I} \right)^{-1} \boldsymbol{y} \end{align}`
任意の置換行列`$\boldsymbol{M}$`に対して`$\kappa (\boldsymbol{x}, \boldsymbol{x}') = \kappa (\boldsymbol{M} \boldsymbol{x}, \boldsymbol{M}, \boldsymbol{x}')$`の場合、以下が成り立つ。<br>
`\begin{align} K_{ij} &= \kappa (\boldsymbol{P}^i \boldsymbol{x}, \boldsymbol{P}^j \boldsymbol{x}) \\ &= \kappa (\boldsymbol{P}^{-i} \boldsymbol{P}^{i} \boldsymbol{x}, \boldsymbol{P}^{-i} \boldsymbol{P}^j \boldsymbol{x}) \\ &= \kappa (\boldsymbol{x}, \boldsymbol{P}^{(j-i) \: {\rm mod} \: n} \boldsymbol{x}) \end{align}`
以上から巡回行列`$\boldsymbol{X}$`に関するカーネル行列`$\boldsymbol{K}$`も巡回行列である。<br>

@divend

@div[right]

`$\boldsymbol{K}$`が巡回行列であることから、以下のように解が求まる。<br>
`\begin{align} \hat{\boldsymbol{\alpha}} = \frac{\hat{\boldsymbol{y}}}{\hat{\boldsymbol{k}}^{\boldsymbol{xx}} + \lambda} \end{align}`
ここで実際に追跡を行う場合は、画像パッチ`$\boldsymbol{z}$`に対して、以下を計算する。<br>
`\begin{align} \boldsymbol{f} (\boldsymbol{z}) = \boldsymbol{w}^T \boldsymbol{z} = \sum_{i=1}^n \alpha_i \kappa (\boldsymbol{z}, \boldsymbol{x}_i) \end{align}`
ここで追跡対象のサンプル`$\boldsymbol{x}$`と画像パッチ`$\boldsymbol{z}$`に対して、カーネル行列`$\boldsymbol{K}^{\boldsymbol{z}}$`の`$(i, j)$`成分が`$\kappa (\boldsymbol{P}^{i-1} \boldsymbol{z}, \boldsymbol{P}^{j-1} \boldsymbol{x})$`とすると、以下を得ることができる。<br>
`\begin{align} \boldsymbol{K}^{\boldsymbol{z}} = C \left( \boldsymbol{k}^{\boldsymbol{xz}} \right) \end{align}`
以上から<br>
`\begin{align} \boldsymbol{f}(\boldsymbol{z}) &= \left( \boldsymbol{K}^{\boldsymbol{z}} \right)^T \boldsymbol{\alpha} \\ \hat{\boldsymbol{f}} (\boldsymbol{z}) &= \hat{\boldsymbol{k}}^{\boldsymbol{xz}} \odot \hat{\boldsymbol{\alpha}} \end{align}`
またカーネル関数`$\boldsymbol{k}^{\boldsymbol{xx}'}$`も巡回行列の性質を利用して計算できる。<br>
`\begin{align} k_i^{\boldsymbol{xx}'} &= \kappa (\boldsymbol{x}', \boldsymbol{P}^{i-1}\boldsymbol{x}) = h \left( \| \boldsymbol{x}' - \boldsymbol{P}^{i-1} \boldsymbol{x} \|^2 \right) \\ &= h \left( \| \boldsymbol{x} \|^2 + \| \boldsymbol{x}' \|^2 - 2 \boldsymbol{x}' \boldsymbol{P}^{i-1} \boldsymbol{x} \right) \\ \boldsymbol{k}^{\boldsymbol{xx}'} = h \left( \| \boldsymbol{x} \|^2 + \| \boldsymbol{x}' \|^2 - 2 \mathcal{F}^{-1} \left( \hat{\boldsymbol{x}}^{\ast} \odot \hat{\boldsymbol{x}}' \right) \right) \end{align}`

@divend