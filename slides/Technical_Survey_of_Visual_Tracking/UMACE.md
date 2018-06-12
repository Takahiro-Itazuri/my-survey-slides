#### Unconstrained Minimum Average Correlation Energy (UMACE)

@div[left]

__概要__<br>
MACEは背景クラッタには頑強だが、強い制約が原因で対象物体の変形に脆弱であった。UMACEは強い制約を外し、統計的な変形耐性基準を陽に用いる。強い制約を外し、解が取ることの可能な領域を広げることができ、その上で変形に強い解を得ている。<br>
<br>
__手法__<br>
`$N$`枚の学習サンプル画像が与えられたとき、`$i$`番目の正のサンプルのフーリエ変換を`$\boldsymbol{X}_i$`、それを対角成分に並べた行列を`$\boldsymbol{X}$`とする。またフィルタをのフーリエ変換を`$\boldsymbol{h}$`とする。このとき`$i$`番目のサンプル`$\boldsymbol{x}_i$`とフィルタ`$\boldsymbol{h}$`のCross-Correlationをのフーリエ変換を`$\boldsymbol{g}_i$`とするとき、以下の式が成り立つ。<br>
`\begin{align} \boldsymbol{g}_i = \boldsymbol{X}^{\ast}_i \boldsymbol{h} \end{align}`
Cross-Correlationの理想の出力のフーリエ変換を`$\boldsymbol{f}$`とするとき、二乗誤差平均（ASE）は以下のようになる。<br>
`\begin{align} {\rm ASE} = \frac{1}{N} \sum_{i=1}^{N} \left( \boldsymbol{g}_i - \boldsymbol{f} \right)^{+} \left( \boldsymbol{g}_i \boldsymbol{f} \right)  \end{align}`
UMACEはASEが最小にする`$\boldsymbol{f}$`を最適と定義する。<br>
`\begin{align} \nabla_{\boldsymbol{f}} {\rm ASE} &= \frac{2}{N} \sum_{i=1}^{N} \left( \boldsymbol{g}_i - \boldsymbol{f} \right) \\ \boldsymbol{f}_{\rm opt} &= \frac{1}{N} \sum_{i=1}^{N} \boldsymbol{g}_i = \overline{\boldsymbol{g}} = \frac{1}{N} \sum_{i=1}^{N} \boldsymbol{X}^{\ast}_i \boldsymbol{h} = \overline{\boldsymbol{X}}^{\ast} \boldsymbol{h} \end{align}`
このとき各Cross-Correlationと最適なCross-Correlation`$\overline{{\bf g}}$`の二乗誤差平均（ASM）は以下のようになる。<br>

@divend

@div[right]

`\begin{align} {\rm ASM} &= \frac{1}{N} \sum_{i=1}^{N} \left( \boldsymbol{g}_i - \overline{\boldsymbol{g}} \right)^{+} \left( \boldsymbol{g}_i - \overline{\boldsymbol{g}} \right) \\ &= \frac{1}{N} \sum_{i=1}^{N} \left( \boldsymbol{X}_i^{\ast} \boldsymbol{h} - \overline{\boldsymbol{X}}^{\ast} \boldsymbol{h} \right)^{+} \left( \boldsymbol{X}_i^{\ast} \boldsymbol{h} - \overline{\boldsymbol{X}}^{\ast} \boldsymbol{h} \right) \\ &= \boldsymbol{h}^{+} \left[ \frac{1}{N} \sum_{i=1}^{N} \left( \boldsymbol{X}_i - \overline{\boldsymbol{X}} \right)^{\ast} \left( \boldsymbol{X}_i - \overline{\boldsymbol{X}} \right) \right] \boldsymbol{h} \\ &= \boldsymbol{h}^{+} \boldsymbol{S}_x \boldsymbol{h} \end{align}`
Correlation Planeのピークは以下の通り。<br>
`\begin{align} |\overline{g} (O)|^2 = \boldsymbol{h}^{+} \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} \boldsymbol{h} \end{align}`
UMACEは以下を基準として用いる。<br>
`\begin{align} J(\boldsymbol{h}) = \frac{\boldsymbol{h}^{+} \overline{\boldsymbol{x}} \overline{\boldsymbol{x}}^{+} \boldsymbol{h} }{ \boldsymbol{h}^{+} \boldsymbol{S}_x \boldsymbol{h} } \end{align}`
ここで負のサンプルについても考える。`$i$`番目の負のサンプルのフーリエ変換を`${bf y}_i$`、これを対角成分に並べた行列を`${\bf Y}_i$`とするとき、相関エネルギーの平均（ACE）は以下の通り。<br>
`\begin{align} {\rm ACE} &= \frac{1}{N} \sum_{i=1}^{N} {\bf h}^{+} {\bf Y}_i {\bf Y}_{i}^{\ast} {\bf h} \\ &= {\bf h}^{+} \left( \frac{1}{N} \sum_{i=1}^{N} {\bf Y}_i {\bf Y}_i^{\ast} \right) {\bf h} = {\bf h}^{+} {\bf D}_y {\bf h} \end{align}`
以上より、負のサンプルを含めた記述は以下のようになる。<br>
`\begin{align} J' ({\bf h}) = \frac{{\bf h}^{+} \overline{{\bf x}} \overline{{\bf x}}^{+} {\bf h} }{ {\bf h}^{+} \left( {\bf S}_x + {\bf D}_y \right) {\bf h } \end{align}`
UMACEは基準`$J'({\bf h})$`を最大化させる問題を解く。したがって、これを`${\bf h}$`で微分する。

@divend
