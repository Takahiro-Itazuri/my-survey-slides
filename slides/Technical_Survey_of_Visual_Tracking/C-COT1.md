#### C-COT

@div[left]

__概要__<br>
DCFは複数の入力が同一の解像度を持たなければいけない制約があるため、CNNの複数の層を利用する方法は議論されるべき問題である。本論文では、連続空間領域におけるCorrelation Filterを学習し、また各層に対してConfidence Mapを用意することで、多重解像度のCNNの層を統合してDCFに適用することを可能にした。<br>
<br>
__手法__<br>
周期`$T$`を持つ`$L^2$`空間を`$L^2(T)$`とし、この空間における内積と畳み込み演算を以下のように定義する。<br>
`\begin{align} \langle g, h \rangle &= \frac{1}{T} \int_{0}^{T} g(t) \overline{h(t)} dt \\ &= \frac{1}{T} \int_{0}^{T} g(t-s) h(s) ds \end{align}`
複素指数関数`$ e_k(t) = e^{i \frac{2\pi}{T} kt} $`は上記の畳み込み演算の固有関数であり、集合`$\left\{ e_k \right\}_{-\infty}^{\infty} $`は`$L^2(T)$`空間の直交基底である。このときフーリエ係数は`$ \hat{g} \left[k\right] = \langle g, e_k \rangle $`で与えられる。<br>
学習サンプル`$x_j$`に対して、異なる解像度を持つ`$D$`チャンネルの特徴量`$x_j^1, \cdots x_j^D$`が与えられたとき、`$N_d$`を`$d$`チャンネル目の特徴量の要素数とすると、サンプル空間は`$\mathcal{X} = \mathbb{R}^{N_1} \times \mathbb{R}^{N_D} $`で定義される。<br>
ここで問題を連続空間領域で定式化するために、学習サンプルの陰的補間モデルを導入する。各チャンネルに対して、補間演算子`$$J_d: \mathbb{R}^{N_d} \to L^2 (T) `を以下のように定義する。<br>
`\begin{align} J_d \left\{x^d\right\}(t) = \sum_{n=0}^{N_d-1} x^d \left[n\right] b_d \left( t-\frac{T}{N_d}n \right) \end{align}`
ただし、`$b_d \in L^2(T)$`は補間関数である。<br>

@divend

@div[right]

![C-COT](assets/img/C-COT.png =full)

求めたいものは線形畳み込み演算子`$S_f: \mathcal{X} \to L^2(T) $`であり、これはサンプル`$x \in \mathcal{X}$`から`$ s(t) = S_f \left\{x\right\} (t) $`へ射影である。`$s(t) \in \mathbb{R}$`は位置`$t \in \left[0,T\right)$`における追跡対象のconfidence scoreである。この演算子`$S_f$`は畳み込みフィルタの組`$f = \left( f^1, \cdots, f^D \right) \in L^2 (T)^D $`をパラメータとして持つ。このとき畳み込み演算子`$S_f$`は以下のように定義される。<br>
`\begin{align} S_f \left\{x\right\} = \sum_{d=1}^{D} f^d \ast J_d \left\{x^d\right\} \end{align}`
通常のDCFの場合、各学習サンプルに対して所望の畳み込み出力を表す離散関数がラベル付けされる一方で、提案手法では連続空間領域に対してconfidence function`$y_j \in L^2(T)$`が与えられる。フィルタ`$f$`は`$m$`個の学習サンプルペア`$$\left\{ (x_j, y_j) \right\} _{1}^{m} \subset \mathcal{X} \times L^2(T) `に対して、以下を最小化するように学習する。<br>
`\begin{align} E(f) = \sum_{j=1}^{m} \alpha_j \| S_f \left\{x_j\right\} - y_j \|^2 + \sum_{d=1}^{D} \| \omega f^d \|^2 \end{align}`
ただし、`$alpha_j$`は各学習サンプルの影響度を表す重みである。<br>
`$x^d$`のDFTは、`$X^d \left[k\right] = \sum_{n=0}^{N_d-1} x^d \left[n\right] e^{-i \frac{2\pi}{N_d} nk} $`で与えられ、これを用いて補間演算子`$J_d$`は以下のように与えられる。<br>
`\begin{align} \hat{\J_d \left\{x^d\right\}} \left[k\right] = X^d \left[k\right] \hat{b}_d \left[k\right] \end{align}`
パーセバルの公式より、目的関数は以下のように変形できる。<br>
`\begin{align} E(f) = \sum_{j=1}^{m} \alpha_j \| \sum_{d=1}^{D} \hat{f}^d X_j^d \hat{b}^d - \hat{y}_j \|^2 + \sum_{d=1}^{D} \| \hat{\omega} \ast \hat{f}^d \|^2 \end{align}`

@divend