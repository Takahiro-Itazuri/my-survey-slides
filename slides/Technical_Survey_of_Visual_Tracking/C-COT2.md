#### Continuous Convolution OPerator Tracker (C-COT)

@div[left]

フィルタ`$f$`は`$m$`個の学習サンプルペア`$\left\{ (x_j, y_j) \right\} _{1}^{m} \subset \mathcal{X} \times L^2(T) $`に対して、以下を最小化するように学習する。<br>
`\begin{align} E(f) = \sum_{j=1}^{m} \alpha_j \| S_f \left\{x_j\right\} - y_j \|^2 + \sum_{d=1}^{D} \| \omega f^d \|^2 \end{align}`
ただし、`$alpha_j$`は各学習サンプルの影響度を表す重みである。<br>
`$x^d$`のDFTは、`$X^d \left[k\right] = \sum_{n=0}^{N_d-1} x^d \left[n\right] e^{-i \frac{2\pi}{N_d} nk} $`で与えられ、これを用いて補間演算子`$J_d$`は以下のように与えられる。<br>
`\begin{align} \hat{J_d \left\{x^d\right\}} \left[k\right] = X^d \left[k\right] \hat{b}_d \left[k\right] \end{align}`
パーセバルの公式より、目的関数は以下のように変形できる。<br>
`\begin{align} E(f) = \sum_{j=1}^{m} \alpha_j \| \sum_{d=1}^{D} \hat{f}^d X_j^d \hat{b}^d - \hat{y}_j \|^2 + \sum_{d=1}^{D} \| \hat{\omega} \ast \hat{f}^d \|^2 \end{align}`

@divend

@div[right]

@divend