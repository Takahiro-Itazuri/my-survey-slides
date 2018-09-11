#### The World of Fast Moving Objects
###### Denys Rozumnyi, Jan Kotera, Filip Sroubek, Lukas Novotny, Jiri Matas

@div[left]

__概要__<br>
露光時間内に自信の大きさ以上の距離を移動する物体を高速移動物体（FMO: Fast Moving Objects）と定義し、高速移動物体は現実世界で頻繁に起こりうるにも関わらず、これまであまり取り組まれてこなかった。そこで本論文は、高速移動物体に関するデータセットを構築し、高速物体を検出し、物体の回転軸や回転速度などを推定する手法を提案した。<br>
<br>
__手法・新規性__<br>
提案手法は大きく２つの問題に取り組んだ。１つはFMOを検出・追跡する問題であり、もう１つはFMOの見た目の再構成や回転軸や回転量を推定する問題である。FMOを検出・追跡する手法としては、Detector、Re-detector、Trackerの３つの要素で構成されており、ベースとしては固定背景動画に対して連続３フレームから得られる３つの差分画像を二値化したものを使って、候補領域を絞る。Detectorで検出できなければ、Re-detectorが１フレーム前のFMOのパスを利用して検出しようとする。Re-detectorが検出できなければ、TrackerがFMOの色や半径の情報から画像合成したものと実際のフレームの誤差を最小化する問題を解く。２つ目の問題に対しては、まずモーションブラーを引き起こす演算子を推定し、その後non-blind deblurringを解く。データセットは16個の動画で構成されており、既存手法よりFMOに対して良い精度を示した。また時間方向の超解像度化を行い、ハイスピードカメラの画像と同等のものが得られた。<br>


@divend

@div[right]

![](assets/img/The_World_of_Fast_Moving_Objects.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2017/papers/Rozumnyi_The_World_of_CVPR_2017_paper.pdf)<br>
・[ポスター](http://openaccess.thecvf.com/content_cvpr_2017/poster/2157_POSTER.pdf)<br>

@divend
