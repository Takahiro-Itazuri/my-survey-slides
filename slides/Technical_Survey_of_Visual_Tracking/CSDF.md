#### Correlation Synthetic Discriminant Function

@div[left]

__概要__<br>
従来のSDFは出力の相関画像における中心の値だけに制約を与えていたため、negative sampleに対する相関画像の中心では0に近い値を取るが、sidelobeでは閾値を超えることが発生する。そこで本論文では、出力相関画像の中心以外の位置に対する制約を設けたCorrelation Synthetic Discriminant Functionを提案する。<br>
<br>
__手法__<br>
<u>Exact Correlation SDF-1 Synthesis</u><br>
各学習サンプルに対して、平行移動した画像を生成し、それを学習サンプルに追加する。positive sampleを`$ \left\{ \boldsymbol{f} \right\} $`、negative sampleを`$ \left\{ \boldsymbol{g} \right\} $`とするとき、各サンプルに対して`$(\pm d_s, 0), (0, \pm d_s) $`並行移動させた画像郡をそれぞれ`$ \left\{ {\bf f}' \right\}, \left\{ {\bf g}' \right\} $`とする。このように各サンプルに対して`$ N_s - 1 $`枚の学習サンプルを増やすことで、全体の学習サンプル数を`$ N_s $`倍に増やす。そして、求めたいフィルタ`$ {\bf h} $`に対して、以下のような制約を与える。<br>
`\begin{align} {\bf f} \ast {\bf h} &= 1 & {\bf f}' \ast {\bf h} &= 0 \\ {\bf g} \ast {\bf h} &= 0 & {\bf g}' \ast {\bf h} &= 0 \end{align}`
これにより、positive sampleに対しては中心でのみ高いピークを持ち、negative sampleに対しては中心の周り（sidelobe）でも低い値を保つことができる。この制約条件下において、従来のSDFと同様に以下の計算を行う。<br>
`\begin{align} {\bf V a} &= {\bf u} & {\bf V} &= {\bf X}^T {\bf X} \in \mathbb{R}^{N_T \times N_T} \end{align}`
しかし、実際には学習サンプルが線形独立である保証がないことや、学習サンプルの増やし方が他にも多くあることから、解くべき方程式の次元数が大きくなるため、次元圧縮を行うテクニックが用いられる。<br>

@divend

@div[right]

![CSDF](assets/img/CSDF.png =full)<br>
<u>Least-Squares SDF-2 Synthesis</u><br>
次元圧縮後の学習サンプルを`${{\bf z}}$`とすると、新しいフィルタ`${\bf e}$`は以下の式で与えられる。<br>
`\begin{align} {\bf Z}^T {\bf e} &= {\bf u} & {\bf Z} &= \begin{pmatrix} {\bf z}_{1} & \cdots & {\bf z}_{N_T} \end{pmatrix} \in \mathbb{R}^{d' \times N_T} \end{align}`
このとき`${\bf Z} {\bf Z}^{T} \in \mathbb{R}^{d' \times d'}$`はフルランクであるので、一意に解を求めることができ、また以下の最小二乗近似と同じ解となる。<br>
`\begin{align} J({\bf e}) = \sum_{i=1}^{N_T} ( {\bf z}_{i}^{T} {\bf e} - u_i )^2 \end{align}`

<u>Peak-to-Sidelobe Ratio Maximized Correlation SDF-3 Synthesis</u><br>
`${{\bf h}}$`による`${{\bf f}}$`の写像を信号、`${{\bf g}}, {{\bf f}'}, {{\bf g}'}$`の写像を雑音と考える。このとき、それぞれの二乗平均`$\langle {\bf f} \cdot {\bf h} \rangle, \langle {\bf g} \cdot {\bf h} \rangle + \langle {\bf f}' \cdot {\bf h} \rangle + \langle {\bf g}' \cdot {\bf h} \rangle$`を考えたとき、Peak-to-Sidelobe Ratio(PSR)は以下の式で与えられる。<br>
`\begin{align} {\rm PSR} &= \frac{{\rm mean \;\; square \;\; signal \;\; (correct \;\; peak \;\; value)}}{{\rm sum \;\; of \;\; the \;\; mean \;\; square \;\; false \;\; peak \;\; (sidelobe \;\; values)}} \\ &= \frac{\langle {\bf f} \cdot {\bf h} \rangle}{\langle {\bf g} \cdot {\bf h} \rangle + \langle {\bf f}' \cdot {\bf h} \rangle + \langle {\bf g}' \cdot {\bf h} \rangle} \\ &= \frac{{\bf e}^{T} {\bf R}_{signal} {\bf e}}{{\bf e}^T {\bf R}_{sidelobe} {\bf e}} \end{align}`

@divend
