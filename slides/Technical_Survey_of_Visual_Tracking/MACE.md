#### Minimum Average Correlation Energy (MACE) Filters

@div[left]

__概要__<br>
PSR filterはcorrelation plane上の中央付近以外の値を抑制することを目的に学習サンプルの周囲（上下左右）の点に制約を追加しているが、相関値のピークを指定できないことと学習サンプル数が5倍になることが問題点である。MACE filterは相関値のピークを指定可能であり、またcorrelation plane全体に対して制約を与えることができる。<br>
<br>
__手法__<br>
`$i$`番目の学習サンプル画像をベクトル化したものを`${\bf x}_i$`とし、その離散フーリエ変換(DFT)を`${\bf X}_i$`とする。またそれを並べたものを`${\bf X} = \begin{pmatrix} {\bf X}_1 & \cdots & {\bf X}_N \end{pmatrix}$`とする。また求めるフィルタ画像をベクトル化したものを`${\bf h}$`とし、そのDFTを`${\bf H}$`とする。`$i$`番目の画像の第`$n$`成分`$x_i (n)$`に対し、フィルタの第`$n$`成分`$h(n)$`を適用した結果を`$g_i (n)$`とし、そのDFTを`$G_i$`とすると、Parseval's Theoremより相関エネルギー`$E_i$`は以下のようになる。<br>
`\begin{align} E_i = \sum_{n=1}^{d} | g_i (n) |^2 = \frac{1}{d} \sum_{k=1}^{d} |G_i (k)|^2 = \frac{1}{d} \sum_{k=1}^{d} |H(k)|^2 |X_i (k)|^2 \end{align}`
上式は以下のように書き換えることができる。<br>
`\begin{align} E_i = {bf H}^{+} {\bf D}_i {\bf H} \end{align}`
`$ {\bf H}^{+} $`は`$ {\bf H} $`の共役転置であり、`${\bf D}_i$`は`$ \| X_i (k) \|^2 $`を対角成分に持つ行列である。<br>
ここで、相関空間の以上の議論から、解きたい問題は以下のようになる。<br>
`\begin{align} {\bf X}^{+} {\bf H} = {\bf u} \end{align}`


@divend

@div[right]

ターゲットの位置のピークを固定値（実際には1を用いる）に拘束しながら、全体の相関値の平均を最小化する問題を解く。<br>
`\begin{align} \mathop{\rm min}\limits_{\boldsymbol{w}} \| \boldsymbol{x} \otimes \boldsymbol{w} \|^{2} \\ {\rm subject \;\; to \;\; } \boldsymbol{w}^T \boldsymbol{x} = 1 \end{align}`

@divend
