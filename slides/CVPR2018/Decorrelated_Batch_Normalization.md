#### Decorrelated Batch Normalization
###### Lei Huang, Dawei Yang, Bo Lang, Jia Deng

@div[left]

__概要__<br>
本論文は、Batch Normalizationに白色化を導入したDecorrelated Batch Normalizationを提案した。通常のBatch Normalizationは標準化を行っているが、白色化を行っていない。したがって、白色化を導入することにより、Batch Normalizationよりさらに早く学習を収束させることが可能になった。<br>
<br>
__手法・新規性__<br>
PCAを用いた白色化を行うとstochastic axis swappingという問題が発生する。データxが与えられたとき、それに対する正規直交基底をDとすると、異なるイテレーションから得られたデータx1とx2に対する正規直交基底D1とD2において、D1=D2とならない現象のことをいう。この現象を避けるため、Decorrelated Batch NormalizationではZCAを用いた白色化を行う。<br>


@divend

@div[right]

![DBN](assets/img/Decorrelated_Batch_Normalization.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Huang_Decorrelated_Batch_Normalization_CVPR_2018_paper.pdf)<br>
・[Supplemental Materials](http://openaccess.thecvf.com/content_cvpr_2018/Supplemental/1134-supp.pdf)<br>

@divend