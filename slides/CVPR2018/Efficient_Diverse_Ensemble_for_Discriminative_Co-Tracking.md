#### Efficient Diverse Ensemble for Discriminative Co-Tracking
###### Kourosh Meshgi, Shigeyuki Oba, Shin Ishii

@div[left]

__概要__<br>
tracking-by-detectionベースの物体追跡手法は識別器の不完全性からオンライン自己学習するため、自己学習のループでドリフト問題が発生する。そこで学習する識別器に対する教師が必要であるという発想から、相補的に教師になるアンサンブル学習ベースの手法が提案されている。しかし、アンサンブル学習ベースの手法は、各識別器が互いに重複した領域を対象にする冗長性が発生する。本論文ではその冗長性を軽減することが可能なリアルタイム物体追跡手法（DEDT: Diversified Ensemble Discriminative Tracker）を提案する。<br>
<br>
__手法・新規性__<br>
DEDTは高い適応性と多様性を持つ識別器群であるCommitteeモデルと長期記憶を持つAuxiliaryモデルからなり、Committeeモデルが不明確な回答を出した入力に対しては、Auxiliaryモデルが代わりに回答する。Committeeモデルは自身が不明確な回答をしたデータを用いて学習する。またこれまでのデータから不明確な回答になるようなデータを人工的に生成し、そのデータにおけるエラー率が、推定時に冗長な結果が得られたデータのエラー率より小さくなるまで繰り返し、更新することで、冗長性を回避する。一方でAuxiliaryモデルはCommitteeモデルより更新頻度が低くすることで長記憶性を持つ。<br>

@divend

@div[right]

![DEDT](assets/img/DEDT.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Meshgi_Efficient_Diverse_Ensemble_CVPR_2018_paper.pdf)<br>

@divend