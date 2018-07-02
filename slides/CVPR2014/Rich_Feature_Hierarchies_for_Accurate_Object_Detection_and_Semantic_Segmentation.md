#### Rich Feature Hierarchies for Accurate Object Detection and Semantic Segmentation
###### Ross Girshick, Jeff Donahue, Trevor Darrell, Jitendra Malik

@div[left]

__概要__<br>
本論文は物体認識タスクで成功したCNNを物体検出に適応させ、またラベル付けされたデータが少ない場合のfine-tuningの手法を提案した。その結果、従来手法より大きく精度を向上させた。<br>
<br>
__手法・新規性__<br>
Step 1. Selective SearchでProposalを生成する。<br>
Step 2. Proposalを固定サイズにWarpし、CNNで特徴量を抽出する。<br>
Step 3. 各クラスごとに学習されたlinear SVMで分類する。<br>
テスト時には2k個のProposalを作成する。同じクラスに分類されたProposalはIoU（Intersection over Union）に対してNon-Maximum Suppressionを行う。

@divend

@div[right]

![R-CNN](assets/img/R-CNN.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2014/papers/Girshick_Rich_Feature_Hierarchies_2014_CVPR_paper.pdf)<br>
・[](url)<br>

@divend