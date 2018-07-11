#### Continuous Convolution OPerator Tracker (C-COT)

@div[left]

フィルタ`$f$`は`$m$`個の学習サンプルペア`$\left\{ (x_j, y_j) \right\} _{1}^{m} \subset \mathcal{X} \times L^2(T) $`に対して、以下を最小化するように学習する。<br>
`\begin{align} E(f) = \sum_{j=1}^{m} \alpha_j \| S_f \left\{x_j\right\} - y_j \|^2 + \sum_{d=1}^{D} \| \omega f^d \|^2 \end{align}`
ただし、`$alpha_j$`は各学習サンプルの影響度を表す重みである。<br>
`$x^d$`のDFTは、`$X^d \left[k\right] = \sum_{n=0}^{N_d-1} x^d \left[n\right] e^{-i \frac{2\pi}{N_d} nk} $`で与えられ、これを用いて補間演算子`$J_d$`は以下のように与えられる。<br>
`\begin{align} \hat{J_d \left\{x^d\right\}} \left[k\right] = X^d \left[k\right] \hat{b}_d \left[k\right] \end{align}`
パーセバルの公式より、目的関数は以下のように変形できる。<br>
`\begin{align} E(f) = \sum_{j=1}^{m} \alpha_j \| \sum_{d=1}^{D} \hat{f}^d X_j^d \hat{b}^d - \hat{y}_j \|^2 + \sum_{d=1}^{D} \| \hat{\omega} \ast \hat{f}^d \|^2 \end{align}`
実践的な目的で、フィルタ`$f$`は有限なパラメータで与えられるべきである。そこで有限次元の部分空間`$V = {\rm span} \left\{ e_K \right\}_{-K_1}^{K_1} \times \cdots \times {\rm span} \left\{ e_k \right\}_{-K_D}^{K_D} \subspace L^2 (T)^D $`で縮小させる。これは、上述の問題において`$\hat{f}^d[k] = 0 (|k| > K_d)$`という制約をおいたことに等しい。実験においては、`$K_d = \lfloor \frac{N_d}{2} \rfloor $`とした。<br>
この問題の解を導出するため、ベクトル化を図る。`$\hat{{\bf f}}^d = \left( \hat{f}^d [-K_D] \cdots \hat{f}^d [K_D] \right)^T \in \mathbb{C}^{2K_d + 1} $`を導入し、フーリエ係数ベクトルを`$ \hat{{\bf f}} = \left[ \left( \hat{{\bf f}}^1 \right)^T \cdots \left( \hat{{\bf f}}^D \right)^T \right]^T $`とする。さらに`$ \hat{{\bf y}}_j = \left( \hat{y}_j [-K] \cdots \hat{y}_j [K] \right)^T $`とする。ただし、`$ K = {\rm max}_d K_d $`である。

@divend

@div[right]

@divend