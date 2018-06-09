#### High Performance Visual Tracking With Siamese Region Proposal Network
###### Bo Li, Junjie Yan, Wei Wu, Zheng Zhu, Xiaolin Hu

@div[left]

__概要__<br>
オフラインで学習させたDNNで得た特徴量を使用した物体追跡手法は、ターゲットの動画に特有の情報を使用していないことから、相関フィルタベースの手法より良い精度が出ていなかった。提案手法は大規模な画像ペアデータを用いて学習し、同じ特徴量抽出器を２つの入力に適応させて得た特徴量の類似度を比較するSiamese NetworkとFaster R-CNNで提案されているRegion Proposal Network（RPN）を組み合わせた上で、物体追跡をlocal one-shot detectionとして定式化することで、高速かつ高精度な追跡を実現した。<br>
<br>
__手法・新規性__<br>
従来のSiamese Networkを利用した手法とは異なり、RPNを用いることで物体の変形に合わせた矩形領域を提示することによって高い精度を出すことが可能である。また物体追跡をlocal one-shot detectionとして定式化する<br>


@divend

@div[right]

![](assets/img/Siamese-RPN.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Li_High_Performance_Visual_CVPR_2018_paper.pdf)<br>

@divend