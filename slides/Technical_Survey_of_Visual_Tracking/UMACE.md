#### Unconstrained Minimum Average Correlation Energy (UMACE)

@div[left]

__概要__<br>
MACEは背景クラッタには頑強だが、強い制約が原因で対象物体の変形に脆弱であった。UMACEは強い制約を外し、統計的な変形耐性基準を陽に用いる。強い制約を外し、解が取ることの可能な領域を広げることができ、その上で変形に強い解を得ている。<br>
<br>
__手法__<br>
`$N$`枚の学習サンプル画像の`$i$`番目を`${\bf x}_i$`とし、そのフーリエ変換を対角成分に持つ行列を`${\bf X}_i$`とする。またフィルタを`${\bf h}$`とし、そのフーリエ変換を`${\bf H}$`とする。このとき`$i$`番目のサンプル`${\bf x}_i$`とフィルタ`${\bf h}$`のCross-Correlationを`${\bf g}_i$`とし、そのフーリエ変換を`${\bf G}_i$`とするとき、以下の式が成り立つ。<br>
`\begin{align} {\bf G}_i = {\bf X}^{\ast}_i {\bf H} \end{align}`
Cross-Correlationの理想の出力のフーリエ変換を`${\bf F}$`とするとき、二乗誤差平均（ASE）は以下のようになる。<br>
`\begin{align} {\rm ASE} = \frac{1}{N} \sum_{i=1}^{N} \left( {\bf G}_i - {\bf F} \right)^{+} \left( {\bf G}_i {\bf F} \right)  \end{align}`
UMACEはASEが最小にする`${\bf F}$`を最適と定義する。<br>
`\begin{align} \nabla_{{\bf F}} {\rm ASE} &= \frac{2}{N} \sum_{i=1}^{N} \left( {\bf G}_i - {\bf F} \right) \\ {\bf F}_{\rm opt} &= \frac{1}{N} \sum_{i=1}^{N} {\bf G}_i = \overline{{\bf G}} = \frac{1}{N} \sum_{i=1}^{N} {\bf X}^{\ast}_i {\bf H} = \overline{{\bf X}}^{\ast} {\bf H} \end{align}`

@divend

@div[right]

![](path/to/img =full)<br>
<br>

@divend
