#### Learning to Segment Every Thing
###### Ronghang Hu, Piotr Dollár, Kaiming He, Trevor Darrell, Ross Girshick

@div[left]

__概要__<br>
従来のInstance Segmentationはピクセルレベルのラベル付けが必要であったため、100カテゴリ程度に限定されていた。本論文では、完璧なアノテーションがついていないデータで学習して、高品質なInstance Segmentationの実現を目標として、Partially Supervised Instance Segmentation手法Mask`${}^{X}$` R-CNNを提案する。既存の弱教師あり学習手法との差分は、カテゴリ数が多いがBounding Boxのラベルがついたデータを用いることで、3000カテゴリという多くのカテゴリのInstance Segmentationが可能となった。<br>
<br>
__手法・新規性__<br>
提案手法は、各カテゴリごとにマスクが与えられたStrongly Annotated Examplesと、Bounding Boxのみが与えられたWeakly Annotated Examplesを用いたPartially Supervised Instance Segmentationを提案する。提案手法はMask R-CNNに基づいた転移学習を行う。これはMask R-CNNがInstance Segmentationを、Bounding Boxを推定するタスクとMaskを推定するタスクの２つのサブタスクに分解して行う点が、今回使用するデータと親和性が大きいからである。Mask R-CNNのBox Weightsには各カテゴリごとのセマンティックな情報が含まれていると考えられるため、Mask Weightsを直接学習するのではなく、Box WeightsをMask Weightsに変換するClass-Agnostic Weight Transfer Functionを学習する。<br>


@divend

@div[right]

![](path/to/img =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Hu_Learning_to_Segment_CVPR_2018_paper.pdf)<br>
・[Supplemental](http://openaccess.thecvf.com/content_cvpr_2018/Supplemental/0047-supp.zip)<br>

@divend