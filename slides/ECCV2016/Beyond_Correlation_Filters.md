#### Beyond Correlation Filters: Learning Continuous Convolution Operators for Visual Tracking
###### Martin Danelljan, Andreas Robinson, Fahad Khan, Michael Felsberg

@div[left]

__概要__<br>
物体認識ではCNNの最後の層のみを利用する一方で、物体追跡ではより正確な位置推定のため、高い空間解像度を持つ浅い層を利用した手法が提案されている。DCFは複数の入力が同一の解像度を持たなければいけない制約があるため、CNNの複数の層を利用する方法は議論されるべき問題である。本論文では、連続的な空間領域におけるCorrelation Filterを学習し、また各層に対してConfidence Mapを用意することで、多重解像度のCNNの層を統合してDCFに適用することを可能にした。<br>
<br>
__手法・新規性__<br>
学習サンプル`$x_j$`が`$D$`チャンネルの特徴量`$x_j^1, \cdots, x_j^D$`で与えられたとき、以下のような補間演算子`$J_d: \mathbb{R}^{N_d} \to L^2 (T) $`を以下のように定義する。<br>
`\begin{align} J_d \left\{ x^d \right\} (t) = \sum_{n=0}^{N_d-1} x^d \left[n\right] b_d \left( t - \frac{T}{N_d} n \right) \end{align}`
求めたい関数は畳み込み関数`$S_f: \mathcal{X} \to L2 (T)$`であり、これはサンプル`$x \in \mathcal{X}$`からconfidence map `$s(t) = S_f \left\{ x \right\} (t) $`への射影である。畳み込み演算`$S_f$`は`$D$`個の線形フィルタ`$f = \left(f^1, \cdots, f^D\right) \in L^2 (T)^D $`を用いて、以下のように定義される。<br>
`\begin{align} S_f \left\{x\right\} = \sum_{d=1}^{D} f^d \ast J_d \left\{x^d\right\} \end{align}`
この畳み込み演算子`$S_f$`のパラメータであるフィルタ`$f$`は`$m$`個の学習サンプルペア`$\left\{ (x_j, y_j) \right\} _{1}^{m} \subset \mathcal{X} \times L^2(T) $`に対して、以下を最小化するように学習する。<br>
`\begin{align} E(f) = \sum_{j=1}^{m} \alpha_j \| S_f \left\{x_j\right\} - y_j \|^2 + \sum_{d=1}^{D} \| \omega f^d \|^2 \end{align}`

@divend

@div[right]

![C-COT](assets/img/C-COT.png =full)<br>
<br>

__リンク__<br>
・[論文](https://www.cvl.isy.liu.se/research/objrec/visualtracking/conttrack/C-COT_ECCV16.pdf)<br>
・[プロジェクト](http://www.cvl.isy.liu.se/research/objrec/visualtracking/conttrack/index.html)<br>
・[GitHub](https://github.com/martin-danelljan/Continuous-ConvOp)<br>

@divend