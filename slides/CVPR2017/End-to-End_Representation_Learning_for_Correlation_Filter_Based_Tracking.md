#### End-to-End Representation Learning for Correlation Filter Based Tracking
###### Jack Valmadre, Luca Bertinetto, João F. Henriques, Andrea Vedaldi, Philip H. S. Torr

@div[left]

__概要__<br>
オフラインで学習したCNNとオンライン学習可能なCorrelation Filter（CF）を利用した手法は、CNNにCFを結合しただけであるため、CNNの部分を効率的に利用できていない。本論文ではCNNとCFを組み合わせた手法において、CFを微分可能なレイヤーとすることでEnd-to-Endに学習できるようにしたネットワーク（CFNet）を提案する。CFを追加したことによる精度向上は見られなかったが、より浅いネットワークでSoTAに近い精度を実現することが可能となった。<br>
<br>
__手法・新規性__<br>
提案手法は周波数領域におけるリッジ回帰問題を解くことで得た特徴量マップ`$x = f_{\rho}(x')$`に対して計算したCFテンプレート`$\omega = \omega(x)$`とスカラーパラメータ`$s$`と`$b$`を用いて、以下のように記述する。
`\begin{align} h_{\rho, s, b} = s \omega \left( f_{\rho} (x') \right) \ast f_{\rho} (z') + b \end{align}`
CFは以下の最適化問題を解く問題である。<br>
`\begin{align} \frac{1}{2n} \| \omega \star x - y \|^2 + \frac{\lambda}{2} \| \omega \|^2 \end{align}`
この最適化問題は以下のようにclosed-formに解が求まることが知られており、その解は以下の式を満たすことが分かっている。<br>
`\begin{align} k &= \frac{1}{n} \left( x \star x \right) + \lambda \delta \\ k \ast \alpha &= \frac{1}{n} y \\ w = &= \alpha \ast x \end{align}`
この式に基づいて計算グラフを構築し微分を行えば、誤差逆伝搬を行えるようになる。

@divend

@div[right]

![CFNet](assets/img/CFNet.png =full)<br>
<br>
__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2017/papers/Valmadre_End-To-End_Representation_Learning_CVPR_2017_paper.pdf)<br>
・[Supplemental](http://openaccess.thecvf.com/content_cvpr_2017/supplemental/Valmadre_End-To-End_Representation_Learning_2017_CVPR_supplemental.pdf)<br>
・[プロジェクト](https://www.robots.ox.ac.uk/~luca/cfnet.html)<br>
・[GitHub](https://github.com/bertinetto/cfnet)<br>

@divend