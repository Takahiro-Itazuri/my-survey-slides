#### Mask R-CNN
###### Kaiming He, Georgia Gkioxari, Piotr Dollar, Ross Girshick

@div[left]

__概要__<br>
Fast / Faster R-CNNはObject Detectionで、Fully Convolutional NetworkはSemantic Segmentationで非常に大きな功績を残してきた。本論文では、インスタンスごとにSemantic LabelとMaskを推定するInstance Segmentationを行う手法（Mask R-CNN）を提案した。Faster R-CNNにSegmentationを行うブランチを加えた構造になっており、非常に高速にInstance Segmentationが可能である。<br>
<br>
__手法・新規性__<br>
Faster R-CNNのRoIPoolは空間量子化を行うため、Segmentationのようなpixel-levelの推定を行うタスクには向いていない。そこで量子化を行わなず正確な空間情報を保持することができるRoIAlignを提案した。<br>


@divend

@div[right]

![](path/to/img =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_ICCV_2017/papers/He_Mask_R-CNN_ICCV_2017_paper.pdf)<br>
・[GitHub](https://github.com/facebookresearch/Detectron)<br>

@divend