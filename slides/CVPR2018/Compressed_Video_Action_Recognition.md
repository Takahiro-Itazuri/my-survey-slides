#### Compressed Video Action Recognition
###### Chao-Yuan Wu, Manzil Zaheer, Hexiang Hu, R. Manmatha, Alexander J. Smola, Philipp Krahenbuhl

@div[left]

__概要__<br>
MPEG-4やH.264のようなコーデックによって圧縮された映像を直接入力として行動認識を行う論文。背景として、映像には時間方向の冗長性が多く含まれており、その事実はコーデックによって大幅に圧縮できることが挙げられる。圧縮された状態に含まれるmotion vectorとresidualを直接入力とするネットワークCoViARによって、高速かつ高精度な行動認識に成功した。<br>
<br>
__手法・新規性__<br>
提案手法の入力として、初期フレームにおいてはRGBの情報を持っており、後続するフレームには初期フレームに対するmotion vectorとresidualを持っている。通常のコーデックでは1つ前のフレームに対するmotion vectorとresidualが格納されているので、初期フレームから注目フレームまで累積することで、初期フレームと累積したmotion vectorとresidualを用いることで現在フレームを復元することできる。実際に推定する際には、初期フレームにおけるRGBから得られた特徴量と、各フレームのmotion vectorとresidualから得られた特徴量を統合して、各フレームの行動認識スコアを出力する。異なる動画間の入力ドメインでの分布を見ると、motion vectorとresidualは領域を共有しており、その結果効率的に学習することができる。<br>


@divend

@div[right]

![CoViAR](assets/img/Compressed_Video_Action_Recognition.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wu_Compressed_Video_Action_CVPR_2018_paper.pdf)<br>

@divend