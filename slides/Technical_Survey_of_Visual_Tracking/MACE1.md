#### Minimum Average Correlation Energy (MACE) Filters

@div[left]

__概要__<br>
PSR filterはcorrelation plane上の中央付近以外の値を抑制することを目的に学習サンプルの周囲（上下左右）の点に制約を追加しているが、相関値のピークを指定できないことと学習サンプル数が5倍になることが問題点である。MACEは相関値のピークを指定可能であり、またCorrelation Plane全体に対して制約を与えることができる。<br>
<br>
__手法__<br>
`$N$`枚の学習サンプル画像のうち`$i$`番目をベクトル化したものを`${\bf x}_i$`とし、その離散フーリエ変換(DFT)を`${\bf X}_i$`とし、それらを並べたものを`${\bf X} = \begin{pmatrix} {\bf X}_1 & \cdots & {\bf X}_N \end{pmatrix}$`とする。またフィルタをベクトル化したものを`${\bf h}$`とし、そのDFTを`${\bf H}$`とする。`$i$`番目の学習サンプル`${\bf x}$`とフィルタ`${\bf h}$`の相関を`${\bf g}_i$`とし、そのDFTを`$G_i$`とすると、Parseval's Theoremより相関エネルギー`$E_i$`は以下のようになる。<br>
`\begin{align} E_i = \sum_{n=1}^{d} | {bf g}_i (n) |^2 = \frac{1}{d} \sum_{k=1}^{d} |G_i (k)|^2 = \frac{1}{d} \sum_{k=1}^{d} |H(k)|^2 |X_i (k)|^2 \end{align}`
上式は以下のように書き換えることができる。<br>
`\begin{align} E_i = {\bf H}^{+} {\bf D}_i {\bf H} \end{align}`
`$ {\bf H}^{+} $`は`$ {\bf H} $`の共役転置であり、`${\bf D}_i = diag \left\{ | X_i (k) |^2 \right\} $`であり、パワースペクトルを対角成分に持った行列である。また制約条件は以下の通り。<br>
`\begin{align} {\bf X}^{+} {\bf H} = {\bf u} \;\;\; \left( {\bf X} = \begin{bmatrix} {\bf X}_1 & {\bf X}_2 & \cdots & {\bf X}_N \end{bmatrix} \right) \end{align}`

@divend

@div[right]

各サンプルごとに各拘束条件上で相関エネルギー`$E_i$`を最小化するようなフィルタ`${\bf H}$`を生成するのは困難である。そこでMACEはすべての相関エネルギーの平均`$E_{av}$`を制約条件下で最小化する。相関エネルギーの平均は以下の通り。<br>
`\begin{align} E_{av} &= \frac{1}{N} \sum_{i=1}^{N} E_i = \frac{1}{N} \sum_{i=1}^{N} {\bf H}^{+} {\bf D}_i {\bf H} \\ &= \frac{1}{N} {\bf H}^{+} \left( \sum_{i=1}^{N} {\bf D}_i \right) \end{align}`
MACEではパワースペクトル行列`${\bf D}_i$`を重み付けした`${\bf D}$`を使用する。<br>
`\begin{align} {\bf D} = \sum_{i=1}^{N} {\bf D}_i \end{align}`
以上を用いて、ラグランジュの未定乗数法よりMACEは以下を最小化する問題に定式化できる。<br>
`\begin{align} {\bf H}^{+} {\bf DH} - \sum_{i=1}^{N} \lambda_i {\bf H}^{+} {\bf X}_i - u_i \end{align}`
これを`${\bf H}$`で微分すると、以下のようになる。<br>
`\begin{align} {\bf DH} &= \sum_{i=1}^{N} \lambda_i {\bf X}_i \\ {\bf H} &= \sum_{i=1}^{N} \lambda_i {\bf D}^{-1} {\bf X}_i = {\bf D}^{-1} {\bf X} {\bf \Lambda} \;\; \left( {\bf Lambda} = {\begin{bmatrix} \lambda_1 & \lambda_2 & \cdots \lambda_N  \end{bmatrix}}^{+} \right) \end{align}`

@divend
