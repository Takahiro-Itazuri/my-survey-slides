#### Minimum Average Correlation Energy (MACE) Filters

@div[left]

__概要__<br>
PSR filterはcorrelation plane上の中央付近以外の値を抑制することを目的に学習サンプルの周囲（上下左右）の点に制約を追加しているが、相関値のピークを指定できないことと学習サンプル数が5倍になることが問題点である。MACEは相関値のピークを指定可能であり、またcorrelation plane全体に対して制約を与えることができる。<br>
<br>
__手法__<br>
`$i$`番目の学習サンプル画像をベクトル化したものを`${\bf x}_i$`とし、その離散フーリエ変換(DFT)を`${\bf X}_i$`とする。またそれを並べたものを`${\bf X} = \begin{pmatrix} {\bf X}_1 & \cdots & {\bf X}_N \end{pmatrix}$`とする。また求めるフィルタ画像をベクトル化したものを`${\bf h}$`とし、そのDFTを`${\bf H}$`とする。`$i$`番目の画像の第`$n$`成分`$x_i (n)$`に対し、フィルタの第`$n$`成分`$h(n)$`を適用した結果を`$g_i (n)$`とし、そのDFTを`$G_i$`とすると、相関エネルギー`$E_i$`は以下のようになる。<br>
`\begin{align} E_i = \sum_{i=1}^{d} | g_i (n) |^2 = \frac{1}{d} \sum_{k=1}^{d} |G_i (k)|^2 = \frac{1}{d} \sum_{k=1}^{d} |H(k)|^2 |X_i (k)|^2 \end{align}`

ターゲットの位置のピークを固定値（実際には1を用いる）に拘束しながら、全体の相関値の平均を最小化する問題を解く。<br>
`\begin{align} \mathop{\rm min}\limits_{\boldsymbol{w}} \| \boldsymbol{x} \otimes \boldsymbol{w} \|^{2} \\ {\rm subject \;\; to \;\; } \boldsymbol{w}^T \boldsymbol{x} = 1 \end{align}`

@divend

@div[right]

@divend
