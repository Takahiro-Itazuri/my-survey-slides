#### Kernelized Correlation Filters (KCF)

@div[left]

__導出__<br>
(2) 非線形リッジ回帰<br>
Representer Theoremより、`${\bf w}$`は非線形関数`${\bf \varphi}({\bf x}_i)$`を用いて以下のように記述できる。<br>
`\begin{align} {\bf w} = \sum_i \alpha_i {\bf \varphi} ({\bf x}_i) \end{align}`
ここで以下のようなカーネル関数`$\kappa({\bf x}, {\bf x}')$`を定義する。<br>
`\begin{align} \kappa ({\bf x}, {\bf x}') = {\bf \varphi} ({\bf x}, {\bf x}') \end{align}`
すべてのサンプルのペアのカーネル関数を並べたカーネル行列`${\bf K}$`を定義する。<br>
`\begin{align} {\bf K}_{ij} = \kappa ({\bf x}, {\bf x}') \end{align}`
このとき高次元非線形関数`${\bf \varphi}$`の内積を簡単な式で表せるとき、その高次元非線形関数を求めることなく、カーネル関数を計算すること可能となることをカーネルトリックと呼ぶ。<br>
カーネルリッジ回帰の解は以下で与えられる。<br>
`\begin{align} {\bf \alpha} = \left( {\bf K} + \lambda {\bf I} \right)^{-1} {\bf y} \end{align}`
任意の置換行列`${\bf M}$`に対して`$\kappa ({\bf x}, {\bf x}') = \kappa ({\bf M} {\bf x}, {\bf M}, {\bf x}')$`の場合、以下が成り立つ。<br>
`\begin{align} K_{ij} &= \kappa ({\bf P}^i {\bf x}, {\bf P}^j {\bf x}) \\ &= \kappa ({\bf P}^{-i} {\bf P}^{i} {\bf x}, {\bf P}^{-i} {\bf P}^j {\bf x}) \\ &= \kappa ({\bf x}, {\bf P}^{(j-i) \: {\rm mod} \: n} {\bf x}) \end{align}`
以上から巡回行列`${\bf X}$`に関するカーネル行列`${\bf K}$`も巡回行列である。<br>

@divend

@div[right]

`${\bf K}$`が巡回行列であることから、以下のように解が求まる。<br>
`\begin{align} \hat{{\bf \alpha}} = \frac{\hat{{\bf y}}}{\hat{{\bf k}}^{{\bf xx}} + \lambda} \end{align}`
ここで実際に追跡を行う場合は、画像パッチ`${\bf z}$`に対して、以下を計算する。<br>
`\begin{align} {\bf f} ({\bf z}) = {\bf w}^T {\bf z} = \sum_{i=1}^n \alpha_i \kappa ({\bf z}, {\bf x}_i) \end{align}`
ここで追跡対象のサンプル`${\bf x}$`と画像パッチ`${\bf z}$`に対して、カーネル行列`${\bf K}^{{\bf z}}$`の`$(i, j)$`成分が`$\kappa ({\bf P}^{i-1} {\bf z}, {\bf P}^{j-1} {\bf x})$`とすると、以下を得ることができる。<br>
`\begin{align} {\bf K}^{{\bf z}} = C \left( {\bf k}^{{\bf xz}} \right) \end{align}`
以上から<br>
`\begin{align} {\bf f}({\bf z}) &= \left( {\bf K}^{{\bf z}} \right)^T {\bf \alpha} \\ \hat{{\bf f}} ({\bf z}) &= \hat{{\bf k}}^{{\bf xz}} \odot \hat{{\bf \alpha}} \end{align}`

@divend