#### End-to-End Representation Learning for Correlation Filter Based Tracking
###### Jack Valmadre, Luca Bertinetto, João F. Henriques, Andrea Vedaldi, Philip H. S. Torr

@div[left]

__概要__<br>
オフラインで学習したCNNとオンライン学習可能なCorrelation Filter（CF）を利用した手法は、CNNにCFを結合しただけであるため、CNNの部分を効率的に利用できていない。本論文ではCNNとCFを組み合わせた手法において、CFを微分可能なレイヤーとすることでEnd-to-Endに学習できるようにしたネットワーク（CFNet）を提案する。<br>
<br>
__手法・新規性__<br>
従来のCNN+CFの手法は学習可能なパラメータ`$\rho$`を持つCNN`$f_{\rho}$`、追跡対象画像`$x'$`と探索領域画像`$z'$`を用いて、相関出力`$g_{\rho}$`を最大にする位置を追跡対象の推定位置とする。<br>
`\begin{align} g_{\pho} (x', z') = f_{\rho} (x') \ast f_{\rho} (z') \end{align}`
提案手法では周波数領域におけるリッジ回帰問題を解くことで得た特徴量マップ`$x = f_{\rho}(x')$`に対して計算したCFテンプレート`$\omega = \omega(x)$`とスカラーパラメータ`$s$`と`$b$`を用いて、以下のように記述する。
`\begin{align} h_{\rho, s, b} = s \omega \left( f_{\rho} (x') \right) \ast f_{\rho} (z') + b \end{align}`

@divend

@div[right]

![CFNet](https://www.robots.ox.ac.uk/~luca/cfnet/page1_teaser.jpg)<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2017/papers/Valmadre_End-To-End_Representation_Learning_CVPR_2017_paper.pdf)<br>
・[Supplemental](http://openaccess.thecvf.com/content_cvpr_2017/supplemental/Valmadre_End-To-End_Representation_Learning_2017_CVPR_supplemental.pdf)
・[プロジェクト](https://www.robots.ox.ac.uk/~luca/cfnet.html)<br>
・[GitHub](https://github.com/bertinetto/cfnet)<br>

@divend