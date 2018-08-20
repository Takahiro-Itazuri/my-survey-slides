#### End-to-End Flow Correlation Tracking with Spatial-temporal Attention
###### Zheng Zhu, Wei Wu, Wei Zou, Junjie Yan

@div[left]

__概要__<br>
Correlation Filterを用いた物体追跡手法のほとんどは空間的情報のみを用いており、動き情報のような時間的情報を考慮していない。本論文では、フロー情報を用いて特徴量表現を向上させる手法としてFlowTrackを提案し、SoTAを達成した。提案手法では、過去の特徴量表現を適用的に統合するためのSpatial-Temporal Attention Mechanismを提案し、またFlowTrackはEnd-to-Endに学習することが可能である。<br>
<br>
__手法・新規性__<br>
FlowTrackはEnd-to-Endに学習可能なSiamese Networkである。Siamese NetworkはHistorical BranchとCurrent Branchに分かれる。Current BranchはFeatureNetから空間特徴量を取得し、Historical Branchは`$t-1$`フレーム目に対してはFeatureNetにより空間特徴量を抽出し、それ以前のフレームと`$t-1$`フレーム目とのフロー情報をFlowNetにより推定し、このフロー情報を用いて`$t-1$`フレーム目との位置合わせを行う。位置合わせを行ったあと、活性化の共起に基づくSpatial Attentionを適応した後、各フレームから得た特徴量に対してGlobal Poolingを行い、それに対してTemporal Attentionを適応する。このようにして得られたHistorical Branchの特徴量とCurrent Branchの特徴量に対してCorrelation Filterを適応する。<br>

@divend

@div[right]

![FlowTrack](assets/img/End-to-End_Flow_Correlaion_Tracking_with_Spatial-temporal_Attention.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Zhu_End-to-End_Flow_Correlation_CVPR_2018_paper.pdf)<br>

@divend