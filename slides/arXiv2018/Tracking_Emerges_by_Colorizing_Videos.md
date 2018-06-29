#### Tracking Emerges by Colorizing Videos
###### Carl Vondrick, Abhinav Shrivastava, Alireza Fathi, Sergio Guadarrama, Kevin Murphy

@div[left]

__概要__<br>
物体追跡のSelf-Supervised LearningとしてVideo Colorizationを学習する手法を提案した。カラーの初期フレーム（参照フレーム）から色を参照するように、白黒にした後続フレームを着色する問題をSelf-Supervised Learningさせることで、内部的に物体追跡のタスクを解かせる。これは動画中で物体の色に一貫性があることを利用している。追跡が失敗する場合は着色が失敗したことに起因しており、これは着色の性能が向上すれば追跡性能を向上することがわかる。<br>
<br>
__手法・新規性__<br>
参照フレームのピクセル`$i$`における正解色を`$c_i \in \mathbb{R}^{d}$`、ターゲットフレームのピクセル`$j$`における正解色を`$c_j \in \mathbb{R}^d$`、推定色を`$y_j \in \mathbb{R}^d$`とする。このとき推定色を以下のように記述する。<br>
`\begin{align} y_j = \sum_i A_{ij} c_i \end{align}`
ここで`$A$`は類似度行列であり、以下の式で与えられる。<br>
`\begin{align} A_{ij} = \frac{\exp \left( f_i^T f_j \right)}{\sum_k \exp \left(f_k^T f_j\right)} \end{align}`
`$f_i \in \mathbb{R}^D$`はCNNによって得た低次元特徴量である。データセットから色空間をK-meansで16個のクラスタにクラスタリングし、そのクラスタへのcross-entropy categorical lossを取る。ネットワークはこのロスを最小化するように学習する。<br>
`\begin{align} \mathop{\rm min}\limits_{\theta} \sum_j L (y_j, c_j) \end{align}`

@divend

@div[right]

![Tracking Emerges by Colorizing Videos](assets/img/Tracking_Emerges_by_Colorizing_Videos.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1806.09594.pdf)<br>

@divend
