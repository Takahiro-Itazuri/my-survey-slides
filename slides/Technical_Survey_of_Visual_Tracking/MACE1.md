#### Minimum Average Correlation Energy (MACE) Filters

@div[left]

__概要__<br>
PSR filterはcorrelation plane上の中央付近以外の値を抑制することを目的に学習サンプルの周囲（上下左右）の点に制約を追加しているが、相関値のピークを指定できないことと学習サンプル数が5倍になることが問題点である。MACEは相関値のピークを指定可能であり、またCorrelation Plane全体に対して制約を与えることができる。<br>
<br>
__手法__<br>
`$N$`枚の学習サンプル画像のうち`$i$`番目をベクトル化したものを`$\boldsymbol{ x}_i$`とし、その離散フーリエ変換(DFT)を`$\boldsymbol{ X}_i$`とし、それらを並べたものを`$\boldsymbol{ X} = \begin{pmatrix} \boldsymbol{ X}_1 & \cdots & \boldsymbol{ X}_N \end{pmatrix}$`とする。またフィルタをベクトル化したものを`$\boldsymbol{ h}$`とし、そのDFTを`$\boldsymbol{ H}$`とする。`$i$`番目の学習サンプル`$\boldsymbol{ x}$`とフィルタ`$\boldsymbol{ h}$`の相関を`$\boldsymbol{ g}_i$`とし、そのDFTを`$G_i$`とすると、Parseval's Theoremより相関エネルギー`$E_i$`は以下のようになる。<br>
`\begin{align} E_i = \sum_{n=1}^{d} | {bf g}_i (n) |^2 = \frac{1}{d} \sum_{k=1}^{d} |G_i (k)|^2 = \frac{1}{d} \sum_{k=1}^{d} |H(k)|^2 |X_i (k)|^2 \end{align}`
上式は以下のように書き換えることができる。<br>
`\begin{align} E_i = \boldsymbol{ H}^{+} \boldsymbol{ D}_i \boldsymbol{ H} \end{align}`
`$ \boldsymbol{ H}^{+} $`は`$ \boldsymbol{ H} $`の共役転置であり、`$\boldsymbol{ D}_i = diag \left\{ | X_i (k) |^2 \right\} $`であり、パワースペクトルを対角成分に持った行列である。また制約条件は以下の通り。<br>
`\begin{align} \boldsymbol{ X}^{+} \boldsymbol{ H} = \boldsymbol{ u} \;\;\; \left( \boldsymbol{ X} = \begin{bmatrix} \boldsymbol{ X}_1 & \boldsymbol{ X}_2 & \cdots & \boldsymbol{ X}_N \end{bmatrix} \right) \end{align}`

@divend

@div[right]

各サンプルごとに各拘束条件上で相関エネルギー`$E_i$`を最小化するようなフィルタ`$\boldsymbol{ H}$`を生成するのは困難である。そこでMACEはすべての相関エネルギーの平均`$E_{av}$`を制約条件下で最小化する。相関エネルギーの平均は以下の通り。<br>
`\begin{align} E_{av} &= \frac{1}{N} \sum_{i=1}^{N} E_i = \frac{1}{N} \sum_{i=1}^{N} \boldsymbol{ H}^{+} \boldsymbol{ D}_i \boldsymbol{ H} \\ &= \frac{1}{N} \boldsymbol{ H}^{+} \left( \sum_{i=1}^{N} \boldsymbol{ D}_i \right) \end{align}`
MACEではパワースペクトル行列`$\boldsymbol{ D}_i$`を重み付けした`$\boldsymbol{ D}$`を使用する。<br>
`\begin{align} \boldsymbol{ D} = \sum_{i=1}^{N} \boldsymbol{ D}_i \end{align}`
以上を用いて、ラグランジュの未定乗数法よりMACEは以下を最小化する問題に定式化できる。<br>
`\begin{align} \boldsymbol{ H}^{+} \boldsymbol{ DH} - 2 \sum_{i=1}^{N} \lambda_i \boldsymbol{ H}^{+} \boldsymbol{ X}_i - u_i \end{align}`
これを`$\boldsymbol{ H}$`で微分すると、以下のようになる。<br>
`\begin{align} \boldsymbol{ DH} &= \sum_{i=1}^{N} \lambda_i \boldsymbol{ X}_i \\ \boldsymbol{ H} &= \sum_{i=1}^{N} \lambda_i \boldsymbol{ D}^{-1} \boldsymbol{ X}_i = \boldsymbol{ D}^{-1} \boldsymbol{ X} \boldsymbol{ \Lambda} \;\; \left( \boldsymbol{ \Lambda} = {\begin{bmatrix} \lambda_1 & \lambda_2 & \cdots \lambda_N  \end{bmatrix}}^{+} \right) \end{align}`

@divend
