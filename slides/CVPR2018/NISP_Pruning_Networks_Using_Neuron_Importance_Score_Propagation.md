#### NISP: Pruning Networks Using Neuron Importance Score Propagation
###### Ruichi Yu, Ang Li, Chun-Fu Chen, Jui-Hsin Lai, Vlad I. Morariu, Xintong Han, Mingfei Gao, Ching-Yung Lin, Larry S. Davis

@div[left]

__概要__<br>
CNNのニューロンの冗長性を軽減するため、分類タスクにおいて分類する直前の層（FRL: Final Response Layer）の復元誤差を最小化するようなPruning（特定のニューロンを削除）するアルゴリズムNeural Importance Score Propagation（NISP）を提案した。如何に精度を落とさず、ネットワークに必要なFLOP数を減らせるかの実験を行い、AlexNetにおいては67.85%のFLOP数を削減したネットワークが1.43%しか精度を落とさないようにすることに成功した。<br>
<br>
__手法・新規性__<br>
従来手法のほとんどは層ごとに独立して考えるか、次の層までを考慮にいれてPruningをする問題を解いていたが、重要なのは最後の層に与える影響であり、提案手法はそれを直接的に考慮している。提案手法はネットワークのPruning問題を、各ニューロンを削除すべきかいなかの0-1整数計画問題として定式化し、FRLの復元誤差を最小化する最適化問題を解く。実際には、目的関数を解析的に解くことはできないため、最適上限を求める問題に帰着させることで、閉経式で解くことが可能となった。<br>


@divend

@div[right]

![](assets/img/NISP_Pruning_Networks_Using_Neuron_Importance_Score_Propagation.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Yu_NISP_Pruning_Networks_CVPR_2018_paper.pdf)<br>
・[Supplemental Material](http://openaccess.thecvf.com/content_cvpr_2018/Supplemental/0601-supp.pdf)<br>

@divend