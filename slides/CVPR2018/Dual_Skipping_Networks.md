#### Dual Skipping Networks
###### Changmao Cheng, Yanwei Fu, Yu-Gang Jiang, Wei Liu, Wenlian Lu, Jianfeng Feng, Xiangyang Xue

@div[left]

__概要__<br>
右脳と左脳で視覚情報を処理している解像度が異なるという人間の脳の仕組みを模倣したネットワークDual Skipping Networksを提案した。このネットワークは２つのサブネットワークで構成されており、それぞれ同様の構造を持つが、左右でスキップ可能な層のパラメータが異なっており、その結果、左右非対称なネットワークがそれぞれglobalな推論とlocalな推論をするようになっている。画像分類の問題において、既存のデータセットに加えて、小さな文字で他の文字を構成するsb-MNISTデータセットで実験を行い、可視化によってそれぞれがglobalな情報とlocalな情報を保持していることを確認し、また非常に良い精度を出した。<br>
<br>
__手法・新規性__<br>
Dual Skipping Networksのネットワーク構造は、右脳と左脳に対応する２つのサブネットワークとそれらが共有するCNNから構成される。共有されているCNNは脳におけるV1領域に対応しており、２つのサブネットワークはそれぞれ右脳と左脳に対応し、globalな推論とlocalな推論をするようになっている。各サブネットワークはSkip-Dense BlockとTransition Layerを交互に重ねた構造になっており、Skip-Dense Blockにおけるスキップ率の違いが２つのサブネットワークの差になっている。Skip-Dense BlockはDense LayerとGating Networkで構成され、Gating Networkがスキップをするか否かを司っている。またglobalな推論をするネットワークからlocalな推論を行うネットワークへの情報を伝達するGuideにより、coarse-to-fineな推論が可能になった。<br>


@divend

@div[right]

![Dual Skipping Networks](assets/img/Dual_Skipping_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Cheng_Dual_Skipping_Networks_CVPR_2018_paper.pdf)<br>

@divend