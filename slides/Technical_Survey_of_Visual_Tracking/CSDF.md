#### Correlation Synthetic Discriminant Function

@div[left]

__概要__<br>
従来のSDFは出力の相関画像における中心の値だけに制約を与えていたため、negative sampleに対する相関画像の中心では0に近い値を取るが、sidelobeでは閾値を超えることが発生する。そこで本論文では、出力相関画像の中心以外の位置に対する制約を設けたCorrelation Synthetic Discriminant Functionを提案する。
<br>
__手法__<br>
<u>Exact Correlation SDF-1 Synthesis</u><br>
各学習サンプルに対して、平行移動した画像を生成し、それを学習サンプルに追加する。positive sampleを`$ \left\{ f \right\} $`、negative sampleを`$ \left\{ g \right\} $`とするとき、各サンプルに対して`$(\pm d_s, 0), (0, \pm d_s)$`並行移動させた画像郡をそれぞれ`$ \left\{ f' \right\}, \left\{ g' \right\} $`とする。このように各サンプルに対して`$ N_s - 1 $`枚の学習サンプルを増やすことで、全体の学習サンプル数を`$ N_s $`倍に増やす。そして、求めたいフィルタ`$ h $`に対して、以下のような制約を与える。<br>
`\begin{align} f \ast h &= 1 \\ f' \ast h &= 0 \\ g \ast h &= 0 \\ g' \ast h &= 0 \end{align}`
これにより、positive sampleに対しては中心でのみ高いピークを持ち、negative sampleに対しては中心の周り（sidelobe）でも低い値を保つことができる。この制約条件下において、従来のSDFと同様の計算を行う。実際には非常に大きな行列の逆行列を計算する必要が生じてしまうため、次元圧縮を行う。


@divend

@div[right]

![](path/to/img =full)<br>
<br>

__リンク__<br>
・[](url)<br>
・[](url)<br>

@divend
