#### Learning from Synthetic Humans
###### Gul Varol, Javier Romero, Xavier Martin, Naureen Mahmood, Michael J. Black, Ivan Laptev, Cordelia Schmid

@div[left]

__概要__<br>
2D Pose Estimationでは、大規模データセットとCNNにより、非常に高い精度を出している一方で、Depth EstimationやBody-Part Segmentationなどではデータ不足のため、未だに良い精度が得られていない。そのため、合成データが使用されるが、リアルさが不足している。本論文では、よりリアルな合成データの生成手法（SURREAL: Synthetic hUmans foR REAL）を提案した。<br>
<br>
__手法・新規性__<br>
提案手法は様々なポーズ、様々なテクスチャ、様々な視点、様々なライティング、様々な背景からレンダリングしており、6,536,752フレーム、67,582個の動画のデータベースを構築した。合成データとリアルデータを組み合わせて学習することで、非常に高い精度のDepth EstimationやBody-Part Segmentationが可能になった。<br>


@divend

@div[right]

![](assets/img/Learning_from_Synthetic_Humans.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2017/papers/Varol_Learning_From_Synthetic_CVPR_2017_paper.pdf)<br>
・[プロジェクト](http://www.di.ens.fr/willow/research/surreal/)<br>
・[データセット](https://www.di.ens.fr/willow/research/surreal/data/)<br>
・[GitHub](https://github.com/gulvarol/surreal)

@divend
