#### Tracking the Invisible: Learning Where the Object Might be
###### Helmut Grabner, Jiri Matas, Luc Van Gool, Philippe Cattin

@div[left]

__概要__<br>
Object Detectionにおいては、コンテキストの情報を使った手法は繰り返し提案されてきたが、Object Trackingにおいては提案されていない。本論文では、物体だけではなく、その周りにある情報（コンテキスト情報）の中で追跡対象を追跡するのに非常に有益な情報を与えるものをSupportersとして利用することで、たとえ完全に遮蔽されていたり、画面外に出てしまった場合であっても追跡することが可能な手法を提案する。<br>
<br>
__手法・新規性__<br>
提案手法はGeneralized Hough Transform（GHT）を用いて、追跡対象のSupportersとなり得るかどうかを判定する。物体検出のタスクは画像`$I$`に対する物体の位置`$x$`を表す確率モデル`$P(x|I)$`を考えたとき、以下のように変形することができる。<br>
`\begin{align} P(x|I) \propto S = \sum_{f \in \mathcal{F}} P(x|f) P(f|I) \end{align}`
`$i$`番目の特徴点`$x^{(i)}$`とその特徴量`$f^{(i)}$`と追跡対象`$x^{\star}$`が与えられたとき、相対位置`$\overline{x}=x^{\star} - x^{(i)}$`に対して、以下のようにできる。<br>
`\begin{align} P_t (f|I) & \propto \alpha P_{t-1} (f|I) + (1 - \alpha) P(f|I_t) \\ P_t(\overline{x}|f) & \propto \alpha P_{t-1} (\overline{x}|f) + (1 - \alpha) P(x^{\star}_t - x_t^{(i)}|f) \end{align}`
このように推定された相対位置を画像空間上に投票していき、実際の投票数が最大となる位置を推定位置とする。

@divend

@div[right]

![](assets/img/Tracking_the_Invisible_Learning_Where_the_Object_Might_be.png =full)<br>
<br>

__リンク__<br>
・[論文](http://cmp.felk.cvut.cz/~matas/papers/grabner-tracking_the_invisible-cvpr10.pdf)<br>

@divend