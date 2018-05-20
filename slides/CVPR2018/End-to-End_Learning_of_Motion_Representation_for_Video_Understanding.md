#### End-to-End Learning of Motion Representation for Video Understanding
###### Lijie Fan, Wenbing Huang, Chuang Gan, Stefano Ermon, Boqing Gong, Junzhou Huang

@div[left]

__概要__<br>
深層学習の成功に反して映像解析では未だに手作りのオプティカルフローが使用されている。通常のオプティカルフローは、それを利用したCNNと独立してしまっている点と時間的・空間的計算コストが非常に大きい点が問題である。本論文では、オプティカルフローに代わる特徴をEnd-to-Endに学習可能なネットワーク（TVNet）を提案した。End-to-Endに学習可能になることで、特定のタスクに特化した動き特徴量を学習できる。<br>
<br>
__手法・新規性__<br>
TVNetの元となるオプティカルフローの最適化手法であるTV-L1は以下のように定式化されている。<br>
`\begin{align} \mathop{\rm min}\limits_{ \{ {\bf u}, {\bf v} \} } \sum_{ {\bf x} \in \Omega } \left( | \nabla {\bf u}_1 ( {\bf x} ) | &+ \frac{1}{2 \theta} | {\bf u} - {\bf v} |^2 \\ &+ | \nabla {\bf u}_2 ( {\bf x} ) | ) + \lambda | \rho ( {\bf u} ( {\bf x} ) \right) | \end{align}`
TVNetはTV-L1の反復過程のうち、勾配（gradient）と発散（divergence）の計算部分を畳み込み層にし、効率性の問題からBicubic補間をBilinear補間にしている。またパラメータ`${\bf u}^0$`をTV-L1では0で初期化していたが、TVNetでは初期値も学習するようにしている。

@divend

@div[right]

![TVNet](assets/img/TVNet.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1804.00413.pdf)<br>
・[GitHub](https://github.com/LijieFan/tvnet)<br>

@divend