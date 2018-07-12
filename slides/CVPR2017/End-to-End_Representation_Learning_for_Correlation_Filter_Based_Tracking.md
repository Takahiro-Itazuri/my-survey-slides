#### End-to-End Representation Learning for Correlation Filter Based Tracking
###### Jack Valmadre, Luca Bertinetto, João F. Henriques, Andrea Vedaldi, Philip H. S. Torr

@div[left]

__概要__<br>
オフラインで学習したCNNとオンライン学習可能なCorrelation Filter（CF）を利用した手法は、CNNにCFを結合しただけであるため、CNNの部分を効率的に利用できていない。本論文ではCNNとCFを組み合わせた手法において、CFを微分可能なレイヤーとすることでEnd-to-Endに学習できるようにしたネットワーク（CFNet）を提案する。<br>
<br>
__手法・新規性__<br>
提案手法は周波数領域におけるリッジ回帰問題を解くことで得た特徴量マップ`$x = f_{\rho}(x')$`に対して計算したCFテンプレート`$\omega = \omega(x)$`とスカラーパラメータ`$s$`と`$b$`を用いて、以下のように記述する。
`\begin{align} h_{\rho, s, b} = s \omega \left( f_{\rho} (x') \right) \ast f_{\rho} (z') + b \end{align}`
CFは以下の最適化問題を解く問題である。<br>
`\begin{align} \frac{1}{2n} \| \omega \star x - y \|^2 + \frac{\lambda}{2} \| \omega \|^2 \end{align}`
この最適化問題は以下のようにclosed-formに解が求まることが知られており、その解を利用することで、以下のような微分可能な層としてみることが可能となる。<br>
`\begin{align} \hat{\nabla_{\alpha} l} &= \hat{x} \odot \left( \hat{\nabla_{\omega} l} \right)^{\ast} \\ \hat{\nabla_y l} &= \frac{1}{n} \hat{k}^{- \ast} \odot \hat{\nabla_{\alpha} l} \\ \hat{\nabla_k l} &= - \hat{k}^{- \ast} \odot \hat{\alpha}^{\ast} \odot \hat{\nabla_{\alpha} l} \\ \hat{\nabla_x l} &= \hat{\alpha} \odot \hat{\nabla_{\omega} l} + \frac{2}{n} \hat{x} \odot {\rm Re} \left\{ \hat{\nabla_k} l \right\} \end{align}`

@divend

@div[right]

![CFNet](assets/img/CFNet.png =full)<br>
<br>
__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2017/papers/Valmadre_End-To-End_Representation_Learning_CVPR_2017_paper.pdf)<br>
・[Supplemental](http://openaccess.thecvf.com/content_cvpr_2017/supplemental/Valmadre_End-To-End_Representation_Learning_2017_CVPR_supplemental.pdf)
・[プロジェクト](https://www.robots.ox.ac.uk/~luca/cfnet.html)<br>
・[GitHub](https://github.com/bertinetto/cfnet)<br>

@divend