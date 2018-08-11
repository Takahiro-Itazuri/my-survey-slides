#### A Neural Algorithm of Artistic Style
###### Leon A. Gatys, Alexander S. Ecker, Matthias Bethge

@div[left]

__概要__<br>
本論文は、任意の画像のスタイルとコンテンツを分離し再統合するニューラルネットワークによるアルゴリズムを提案した。CNNの出力層に近くなるほど詳細な情報が失われ、より抽象的な情報のみが残っていく点に着目し、CNNの各層から得られるフィルタの出力を比較することで、非常に質の高い画像合成を実現した。<br>
<br>
__手法・新規性__<br>
コンテンツに関する損失関数は以下の通り。<br>
`\begin{align} \mathcal{L}_{content} (\overrightarrow{p}, \overrightarrow{x}, l) = \frac{1}{2} \sum_{i, j} \left( F_{ij}^{l} - P_{ij}^{l} \right)^2 \end{align}`
次にスタイルについては、以下のようなグラム行列を考える。<br>
`\begin{align} G_{ij}^{l} = \sum_k F_{ik}^{l} F_{jk}^{l} \end{align}`
このグラム行列はどのような特徴が共起しているかを表す。２つの画像から得られた２つのグラム行列の差分を各層で計算し、その差分の総和をスタイルの損失関数とする。<br>
`\begin{align} \mathcal{L}_{style} (\overrightarrow{a}, \overrightarrow{x}) &= \sum_{l=0}^{L} \omega_l E_l \\ &= \sum_{l=0}^{L} \omega_l \frac{1}{4 N_l^2 M_l^2} \sum_{i, j} \left( G_{ij}^{l} - A_{ij}^{l} \right)^2 \end{align}`
各損失関数にそれぞれ重みをつけて全体の損失とする。<br>
`\begin{align} \mathcal{L}_{total} = \alpha \mathcal{L}_{content} + \beta \mathcal{L}_{style} \end{align}`

@divend

@div[right]

![](assets/img/A_Neural_Algorithm_of_Artistic_Style.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1508.06576.pdf)<br>

@divend