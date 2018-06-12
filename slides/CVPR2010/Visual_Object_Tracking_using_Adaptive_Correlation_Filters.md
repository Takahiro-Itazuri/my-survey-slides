#### Visual Object Tracking using Adaptive Correlation Filters
###### David S. Bolme, J. Ross Beveridge, Bruce A. Draper, Yui Man Lui

@div[left]

__概要__<br>
ASEFやUMACEは非常に高速である一方で、物体追跡タスクでは動画の１フレーム目においてのみ正しい追跡物体の位置が与えられる点や追跡物体の見た目の変化に適応しなければならない点から、物体追跡に適していない。MOSSEは必要なサンプル数が少なくても良く、適応的に更新していくことが可能である。<br>
<br>
__手法・新規性__<br>
`$i$`番目の学習画像を`$f_i$`、それに対応する正解の相関出力を`$g_i$`とし、それぞれのフーリエ変換を`$F_i$`と`$G_i$`とする。このとき、MOSSEフィルタは求めたいフィルタ`$h$`のフーリエ変換`$H$`は、実際の相関出力と正解の相関出力の誤差の二乗和を最小化することで得る。<br>
`\begin{align} \mathop{\rm min}\limits_{H^{\ast}} \sum_i | F_i \odot H^{\ast} - G_i |^2 \end{align}`
この問題は周波数領域において各要素で独立に解くことができる。<br>
`\begin{align} 0 &= \frac{\partial}{\partial H_{\omega \nu}^{\ast}} \sum_i | F_{\omega \nu} H_{\omega \nu}^{\ast} - G_{i \omega \nu} |^2 \\  0 &= \sum_i | F_{i \omega \nu} F_{i \omega \nu}^{\ast} H_{\omega \nu} - F_{i \omega \nu} G_{i \omega \nu}^{\ast} | \\ H &= \frac{ \sum_i F_i \odot G_i^{\ast} }{ \sum_i F_i \odot F_i^{\ast} } \end{align}`
MOSSEの更新式は以下の通り。
`\begin{align} H_i^{\ast} &= \frac{A_i}{B_i} \\ A_i &= \eta G_i \odot F_i^{\ast} + (1 - \eta) A_{i-1} \\ B_i &= eta F_i \odot F_i^{\ast} + (1 - \eta) B_{i-1} \end{align}`

@divend

@div[right]

![](path/to/img =full)<br>
<br>

__リンク__<br>
・[論文](http://www.cs.colostate.edu/~vision/publications/bolme_cvpr10.pdf)<br>
・[デモ](https://youtu.be/Wx3o354xazU)<br>
・[MATLAB code (by amoudgl)](https://github.com/amoudgl/mosse-tracker)<br>
・[Python code (by opencv)](https://github.com/opencv/opencv/blob/master/samples/python/mosse.py)<br>
・[C++ code (by artivis)](https://github.com/artivis/MOSSE_tracker)

@divend
