#### Large-scale Video Classification with Convolutional Neural Networks
###### Andrej Karpathy, George Toderici, Sanketh Shetty, Thomas Leung, Rahul Sukthankar, Li Fei-Fei

@div[left]

__概要__<br>
本論文では、CNNをVideo Classificationに適用し、そのためのデータセット（Sports-1M）を構築した。特に、CNNを用いてどのように時間情報を扱えば、動きの情報を有効に捉えることができるか、追加の動き情報が精度に影響するのか、という問いに取り組んだ。CNNを単純にVideo Classificationに適用する場合、大量のパラメータを学習する必要があり、膨大な学習時間を必要とするが、本論文ではその問題を軽減するためのCNNのアーキテクチャを提案した。<br>
<br>
__手法・新規性__<br>
Sports-1Mは487カテゴリの100万個のYouTube動画で構成されるデータセットである。CNNをVideoに適用させるために、時間情報をどのタイミングで統合すべきか（Time Information Fusion）について様々なパターン（Single Frame, Late Fusion, Early Fusion, Slow Fusion）で実験を行い、Slow Fusion Modelが最も良い精度を出した。またMultiresolution構造（Fovea stream & Context stream）を持つCNNでも実験を行った。驚くべきことに、Single Frame Modelでもかなり良い精度が出ており、スポーツというかなり動的なシーンにおいても、局所的な動きの情報はそこまで重要でないことがわかった。<br>


@divend

@div[right]

![](assets/img/Large-scale_Video_Classification_with_Convolutional_Neural_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_cvpr_2014/papers/Karpathy_Large-scale_Video_Classification_2014_CVPR_paper.pdf)<br>
・[スライド](https://pdfs.semanticscholar.org/6d4c/9c923e9f145d1c01a2de2afc38ec23c44253.pdf)<br>

@divend
