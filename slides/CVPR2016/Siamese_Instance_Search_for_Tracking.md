#### Siamese Instance Search for Tracking
###### Ran Tao, Efstratios Gavves, Arnold W.M. Smeulders

@div[left]

__概要__<br>
従来の物体追跡手法は、追跡対象を表現するモデルや追跡対象の見た目の変化に対応するためのモデルの更新、遮蔽の検出などが必要であったが、本論文はモデルを持たない２つのパッチ間の類似度を計算するマッチング関数を学習するSiamese Networkを用いて、Instance Searchのようなアプローチを採る物体追跡手法（Siamese INstance search Tracker: SINT）を提案した。事前学習したマッチング関数を追跡対象に対して特化させる必要がなく、再検出も可能である。<br>
<br>
__手法・新規性__<br>
SINTはSiamese Networkを大規模画像データセットでマッチング関数を事前に学習させた後、追跡対象に対して学習やモデルの更新を行わずに、初期フレームで与えられた追跡対象と現在フレームの候補領域の類似度をマッチング関数で計算する。２つの異なるサイズのパッチの類似を計算するため、Fast RCNNで使用されているROI Poolingで固定長の特徴量にする。あらゆる見た目変化に対応可能なマッチング関数が内部で学習できているため非常に頑健であり、モデル更新がないためdriftingを起こさない一方で、追跡対象に特化させていないため類似物体に脆弱である。<br>

@divend

@div[right]

![SINT](assets/img/Siamese_Instance_Search_for_Tracking.png =full)<br>
<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Tao_Siamese_Instance_Search_CVPR_2016_paper.pdf)<br>

@divend