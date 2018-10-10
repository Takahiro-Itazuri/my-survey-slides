#### Deep Clustering for Unsupervised Learning of Visual Features
###### Mathilde Caron, Piotr Bojanowski, Armand Joulin, Matthijs Douze

@div[left]

__概要__<br>
ImageNetはCNNの隆盛に大きな貢献をもたらしたが、現在のCNNの識別性能が飽和してきていることもまたImageNetの影響（画像枚数が100万枚ではもはや不十分、ラベル付けの誤りがある）であることを指摘し、インターネット規模のデータ数が必要であり、ラベル付けを必要としない方法が必要であると主張した。本論文では、一般的なクラスタリング手法を用いて疑似ラベルを生成し、その疑似ラベルを教師としてクラス分類タスクについてネットワークを学習することで、あらゆるタスクにおいて非常に高い精度を実現可能な特徴量表現を獲得する手法（DeepCluster）を提案した。DeepClusterは教師なし学習手法に対してSoTAを達成した。<br>
<br>
__手法・新規性__<br>
ランダムに初期化されたAlexNetから得た特徴量を元に識別器を学習すると、チャンスレートである0.1%よりはるかに高い精度である12%を表すことがわかっている。このようなCNN自身が持つ強力な事前知識を利用することで、クラスタリング結果を疑似ラベルとして用いて学習が可能となっている。単純にクラスタリング結果を疑似ラベルとして使用しようとすると、すべての入力を１つのクラスタに割り当てようとする問題や、クラスごとの学習サンプル数の不均一さの問題についても対処した。実験の結果、クラスタリング結果とImageNetラベルのNMIは学習と共に大きくなり、また`$t-1$`エポックと`$t$`エポックのクラスタリング結果のNMIも0.8程度に収束している（1に達していないが、クラス分類結果に影響はないとのこと）。また1000クラス分類問題のための表現学習であるが、k-meansのクラスタ数は10000にした際に最も良い結果が得られた。

@divend

@div[right]

![](assets/img/Deep_Clustering_for_Unsupervised_Learning_of_Visual_Features.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_ECCV_2018/papers/Mathilde_Caron_Deep_Clustering_for_ECCV_2018_paper.pdf)<br>
・[GitHub](https://github.com/facebookresearch/deepcluster)<br>
・[AI関連論文読み会スライド](https://speakerdeck.com/hoto17296/deepcluster-lun-wen-falseshao-jie)<br>

@divend