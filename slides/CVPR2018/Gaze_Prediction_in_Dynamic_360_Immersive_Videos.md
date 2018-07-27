#### Gaze Prediction in Dynamic 360° Immersive Videos
###### Yanyu Xu, Yanbing Dong, Junru Wu, Zhengzhong Sun, Zhiru Shi, Jingyi Yu, Shenghua Gao

@div[left]

__概要__<br>
動的に映像内容が変化する360°動画における視線推定を行った論文。まず動的に映像内容が変化する360°動画の大規模データセットを構築し、そこから視線推定には過去の視線のパスと映像内容が重要であると分析し、その上でCNNとLSTMを組み合わせて顕著性と過去の視線のパスの両方を考慮した視線推定手法を提案した。<br>
<br>
__手法・新規性__<br>
論文で対象としている動画と従来研究が使用している動画の違いとして、1) 通常の映像では受動的に動画を視聴しがちであるが、360°動画では能動的に視聴しようとする点。2) 従来の360°動画は静的な映像内容のものを扱っていた点。3) 提案手法ではHMD内に搭載可能な7invensu a-Glassを用いており、頭部の動きに加えて注視点の情報を取得している点を挙げている。データセットには音声情報もついており、360°動画における音声情報を考慮した研究も今後行っていくとのこと。<br>


@divend

@div[right]

![](assets/img/Gaze_Prediction_in_Dynamic_360_Immersive_Videos.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Xu_Gaze_Prediction_in_CVPR_2018_paper.pdf)<br>
・[Supplemental Material](http://openaccess.thecvf.com/content_cvpr_2018/Supplemental/2529-supp.pdf)<br>

@divend