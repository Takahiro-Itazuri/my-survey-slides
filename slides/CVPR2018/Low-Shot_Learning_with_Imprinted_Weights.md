#### Low-Shot Learning With Imprinted Weights
###### Hang Qi, Matthew Brown, David G. Lowe

@div[left]

__概要__<br>
クラス分類タスクに対してLow-Shot Learningを行うためのWeight Imprintingという技術を提案した論文。Low-Shot Learningは予め十分な量のデータが与えられて学習した後に、データ数が非常に少ない分類すべき新しいクラスが与えられ、その上でそれらを分類するタスクである。Weight Imprintingはすでに学習したクラスの部分に変更を加えないため、学習コストが少なく、少ないデータ数で学習可能である。<br>
<br>
__手法・新規性__<br>
Weight Imprintingはクラス分類器に適用する手法である。通常のCNNによるクラス分類器と異なる点は、畳み込み層から得られた特徴量を正規化する点と、バイアス項のない全結合層である点である。バイアス項がないため、重み係数は正規化された特徴量のテンプレートとして機能する。したがって、分類すべき新しいクラスが与えられたときに、その正規化された特徴量をそのまま重み係数とすることができる。複数のサンプルが与えられた場合は平均を計算して、重み係数とする。Weight Imprintingはテンプレートとして機能する重み係数との内積をが最大となるクラスを推定結果とするため、Nearest Neightborと同等の機能を持っている。<br>


@divend

@div[right]

![](assets/img/Low-Shot_Learning_with_Imprinted_Weights.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Qi_Low-Shot_Learning_With_CVPR_2018_paper.pdf)<br>

@divend