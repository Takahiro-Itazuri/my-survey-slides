#### Unconstrained Minimum Average Correlation Energy (UMACE)

@div[left]

__概要__<br>
MACEは背景クラッタには頑強だが、強い制約が原因で対象物体の変形に脆弱であった。UMACEは強い制約を外し、統計的な変形耐性基準を陽に用いる。強い制約を外し、解が取ることの可能な領域を広げることができ、その上で変形に強い解を得ている。<br>
<br>
__手法__<br>
`$N$`枚の学習サンプル画像の`$i$`番目のフーリエ変換を`${\bf X}_i$`、それを対角成分に並べた行列を`${\bf X}$`とする。またフィルタをのフーリエ変換を`${\bf h}$`とする。このとき`$i$`番目のサンプル`${\bf x}_i$`とフィルタ`${\bf h}$`のCross-Correlationをのフーリエ変換を`${\bf g}_i$`とするとき、以下の式が成り立つ。<br>
`\begin{align} {\bf g}_i = {\bf X}^{\ast}_i {\bf h} \end{align}`
Cross-Correlationの理想の出力のフーリエ変換を`${\bf f}$`とするとき、二乗誤差平均（ASE）は以下のようになる。<br>
`\begin{align} {\rm ASE} = \frac{1}{N} \sum_{i=1}^{N} \left( {\bf g}_i - {\bf f} \right)^{+} \left( {\bf g}_i {\bf f} \right)  \end{align}`
UMACEはASEが最小にする`${\bf f}$`を最適と定義する。<br>
`\begin{align} \nabla_{{\bf f}} {\rm ASE} &= \frac{2}{N} \sum_{i=1}^{N} \left( {\bf g}_i - {\bf f} \right) \\ {\bf f}_{\rm opt} &= \frac{1}{N} \sum_{i=1}^{N} {\bf g}_i = \overline{{\bf g}} = \frac{1}{N} \sum_{i=1}^{N} {\bf X}^{\ast}_i {\bf h} = \overline{{\bf X}}^{\ast} {\bf h} \end{align}`
このとき各Cross-Correlationと最適なCross-Correlation`$\overline{{bf g}}$`の二乗誤差平均（ASM）は以下のようになる。<br>

@divend

@div[right]

`\begin{align} {\rm ASM} &= \frac{1}{N} \sum_{i=1}^{N} \left( {\bf g}_i - \overline{{\bf g}} \right)^{+} \left( {\bf g}_i - \overline{{\bf g}} \right) \\ &= \frac{1}{N} \sum_{i=1}^{N} \left( {\bf X}_i^{\ast} {\bf h} - \overline{{\bf X}}^{\ast} {\bf h} \right)^{+} \left( {\bf X}_i^{\ast} {\bf h} - \overline{{\bf X}}^{\ast} {\bf h} \right) \\ &= {\bf h}^{+} \left[ frac{1}{N} \sum_{i=1}^{N} \left( {\bf X}_i - \overline{{\bf X}} \right)^{\ast} \left( {\bf X}_i - \overline{{\bf X}} \right) \right] {\bf h} \\ &= {\bf h}^{+} {\bf S}_x {\bf h} \end{align}`
Correlation Planeのピークは以下の通り。<br>
`\begin{align} |\overline{g} (O)|^2 = {\bf h}^{+} \overline{{\bf x}} \overline{{\bf x}} {\bf h} \end{align}`

@divend
