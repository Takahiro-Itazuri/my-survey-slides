#### Multi-Cue Correlation Filters for Robust Visual Tracking
###### Ning Wang, Wengang Zhou, Qi Tian, Richang Hong, Meng Wang, Houqiang Li

@div[left]

__概要__<br>
本論文は複数の異なる種類の特徴量を効率的に利用するため、DCFを使った複数のexpertを構築し、各フレームごとに適切なexpertを選択することで頑健な物体追跡手法（MCCT：Multi-Cue Correlation filter based Tracking）を提案した。深層学習から得た特徴量を用いた場合においてSoTAを達成し、従来のHandcraftedな特徴量を用いた場合において、最新の深層学習ベースの手法と同等の精度かつCPUで45fpsの速度を実現した。<br>
<br>
__手法・新規性__<br>
HCFがfeature-levelの統合のみを考慮していたのに対して、MCCTはそれぞれ得られた特徴量の強みを効率よく利用するために、decision-levelの統合も考慮する。MCCTはそれぞれの特徴量が分散を持った異なる視点の特徴量を抽出するようにし、また複数のexpertを各フレームごとに評価し選択することで、良い推定結果を得る。expertの評価にはpair-evaluationとself-evaluationを提案し、これらを統合する過程がdecision-levelの統合に当たる。<br>


@divend

@div[right]

![MCCT](assets/img/Multi-Cue_Correlation_Filters_for_Robust_Visual_Tracking.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Multi-Cue_Correlation_Filters_CVPR_2018_paper.pdf)<br>

@divend