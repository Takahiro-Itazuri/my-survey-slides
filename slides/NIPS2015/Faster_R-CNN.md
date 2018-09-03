#### Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks
###### Shaoqing Ren, Kaiming He, Ross Girshick, Jian Sun

@div[left]

__概要__<br>
Fast R-CNNはDNNを使ったリアルタイムに近い物体検出手法であるが、これはRegion Proposalの生成時間を無視した場合の話である。結果的にRegion Proposalの生成に使用しているSelective Searchがボトルネックとなっている。本論文では、CNN特徴量を元にRegion Proposalを生成するネットワーク（RPN: Region Proposal Network）を組み込んだ物体検出ネットワーク（Faster R-CNN）を提案した。<br>
<br>
__手法・新規性__<br>
RPNは画像を入力とし、物体候補領域とそのスコアが出力される。RPNはFast R-CNNのCNNの層を共有している。CNNから得た特徴量マップにsliding windowを適用して低次元の特徴量ベクトルを抽出した後、スコア出力する層（cls layer）と矩形の位置を回帰する層（reg layer）で処理する。各sliding windowを適用する位置に対して`$k$`種類のAnchor Boxを定義し、各Anchor Boxに対して物体候補領域とそのスコアを出力する。このようにして得られた各位置における複数のAnchor Boxに対するRegion Proposalの生成結果が得られるので、これに対して以下の損失関数を最小化するように学習する。<br>
`\begin{align} L \left( \left\{ p_i \right\}, \left\{ t_i \right\} \right) = \frac{1}{N_{cls}} \sum_i L_{cls} (p_i, p_i^{\ast}) + \lambda \frac{1}{N_{reg}} \sum_i p_i^{\ast} L_{reg} (t_i, t_i^{\ast}) \end{align}`

@divend

@div[right]

![Faster R-CNN](assets/img/Faster_R-CNN.png =full)<br>
<br>

__リンク__<br>
・[論文](https://papers.nips.cc/paper/5638-faster-r-cnn-towards-real-time-object-detection-with-region-proposal-networks.pdf)<br>
・[GitHub](https://github.com/ShaoqingRen/faster_rcnn)<br>

@divend
