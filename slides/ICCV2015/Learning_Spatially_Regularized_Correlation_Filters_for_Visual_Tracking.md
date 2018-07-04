#### Learning Spatially Regularized Correlation Filters for Visual Tracking
###### Martin Danelljan, Gustav Häger, Fahad Shahbaz Khan, Michael Felsberg

@div[left]

__概要__<br>
DCFは学習サンプルの周期性を利用して効率的に識別器を学習を行うが、限られた範囲しか探索できないため高速な物体を追跡できないことや、boundary effectにより良いnegative sampleが得られない点から、追跡精度を落とす原因となっている。本論文では、空間正則化項を追加することで、より頑健な物体追跡手法（SRDCF）を提案した。<br>
<br>
__手法・新規性__<br>
学習サンプル`$\left\{ \left( x_k, y_k \right) \right\}_{k=1}^t$`が与えられたとき、各学習サンプル`$x_k$`から抽出した`$d$`次元の特徴量`$z$`に対して、multi-channel correlation filter `$f$`を適用させたときの相関出力`$S_f \left(x\right)$`は以下で与えられる。<br>
`\begin{align} S_f \left(x\right) = \sum_{l=1}^{d} x^l \star f^l \end{align}`
SRDCFは、DCFの正則化項に対して位置に依存する重み付けを行う。<br>
`\begin{align} \varepsilon (f) = \sum_{k=1}^{t} \alpha_k \| S_f \left( x_k \right) - y_k \|^2 + \sum_{t=1}^{d} \| \omega \cdot f^l \|^2 \end{align}`
この式を周波数空間上で表現すると、以下のようになる。<br>
`\begin{align} \varepsilon (\hat{f}) &= \sum_{k=1}^{t} \alpha_k \| \sum_{l=1}^{d} \hat{x}_k^l \cdot \hat{f}^l - \hat{y}_k \|^2 + \sum_{l=1}^{d} \| \frac{\hat{\omega}}{MN} \star \hat{f}^l \| \\ &= \sum_{k=1}^{t} \alpha_k \| \sum_{l=1}^{d} \mathcal{D} \left( \hat{{\bf x}}_{k}^{l} \right) \hat{{\bf f}}^l - \hat{{\bf y}}_k \|^2 + \sum_{l=1}^{d} \| \frac{\mathcal{C} \left( {\bf \omega} \right)}{MN} \hat{{\bf f}}^l \|^2 \end{align}`

@divend

@div[right]

![SRDCF](assets/img/SRDCF.png =full)<br>
<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Danelljan_Learning_Spatially_Regularized_ICCV_2015_paper.pdf)<br>
・[スライド（VOT2015）](http://data.votchallenge.net/vot2015/presentations/presentation_Danelljan.pdf)<br>

@divend