#### Distractor-aware Siamese Networks for Visual Object Tracking
###### Zheng Zhu, Qiang Wang, Bo Li, Wei Wu, Junjie Yan, Weiming Hu

@div[left]

__概要__<br>
Siamese Networkを用いた物体追跡手法は追跡精度と実行速度のバランスが良く、近年多くの注目を浴びている。Siamese Networkはオフライン学習のみであるため、高速である一方で、追跡対象に十分に特化することができず、類似した物体や背景（Distractor）に脆弱である。Siamese Networkは一般的に使用可能な類似度関数を学習するが、従来手法では追跡対象に対して背景が単純なものばかりが学習画像に入っているため、前景と背景を分離するための特徴量を学習してしまっていた。本論文では、Distractorを学習データとして用いることで、Instance-levelの特徴量表現をオフライン学習し、オンライン追跡時にDistractorの影響を明示的に抑える機構を導入した物体追跡手法（DaSiamRPN）を提案した。<br>
<br>
__手法・新規性__<br>
従来手法が用いているVideo Detection用のデータセットはカテゴリ数が少ないため、追跡時にRegion Proposal Networkに新しいカテゴリが与えられた時に非常に悪い推定を行ってしまう。提案手法はオフライン学習時にはImageNet DetectionやCOCO Detectionのようなカテゴリ数の多いデータセットを用いて、同じカテゴリから得られるnegative pairを大量に学習させる。また検出されたトップの`$k$`個のProposal `$\mathcal{P}$`とDistractor `$\mathcal{D}=\left\{\forall d_i, f(z,d_i) > h \cap d_i \neq z_t \right\}$`以下の目的関数を用いて最終的な結果を得る。<br>
`\begin{align} q = \mathop{\rm arg~max}\limits_{p_k \in \mathcal{P}} f(x, p_k) - \frac{\hat{\alpha} \sum_i^n \alpha_i f(d_i, p_k)}{\sum_i^n \alpha_i} \end{align}`


@divend

@div[right]

![DaSiamRPN](assets/img/Distractor-aware_Siamese_Networks_for_Visual_object_Tracking.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_ECCV_2018/papers/Zheng_Zhu_Distractor-aware_Siamese_Networks_ECCV_2018_paper.pdf)<br>
・[GitHub](https://github.com/foolwood/DaSiamRPN)<br>

@divend