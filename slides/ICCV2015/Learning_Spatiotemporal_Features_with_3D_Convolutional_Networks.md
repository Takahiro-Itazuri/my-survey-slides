#### Learning Spatiotemporal Features with 3D Convolutional Networks
###### Du Tran, Lubomir Bourdev, Rob Fergus, Lorenzo Torresani, Manohar Paluri

@div[left]

__概要__<br>
画像分野においてCNNは大きな成果を出したが、画像の見た目の情報しか考慮できておらず、動きの情報を含む動画の特徴量としては不十分である。本論文では、動画に対する空間的・時間的な特徴量が抽出可能なネットワーク（Convolutional 3D: C3D）を提案する。C3Dは動画を表現する特徴量として必要な(1)generic、(2)compact、(3)efficient、(4)simpleといった性質を満たしている。またC3Dの特徴量は、動画に関する様々なタスクにおいて、最近の手法より良い精度を出した。<br>
<br>
__手法・新規性__<br>
ネットワーク構造に関する実験では、3x3x3のカーネルが最も良い精度を出しており、CNNにおいて3x3のカーネルが最も良い精度を出したのと類似した結果が得られた。また行動認識、行動類似度ラベリング、シーン識別、物体認識のタスクにおいて、SoTAと同等もしくはそれ以上の精度を出した。<br>


@divend

@div[right]

![C3D](assets/img/C3D.png =full)<br>
<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Tran_Learning_Spatiotemporal_Features_ICCV_2015_paper.pdf)<br>
・[プロジェクト](http://vlg.cs.dartmouth.edu/c3d/)<br>
・[Caffe Code](https://github.com/facebook/C3D)<br>

@divend