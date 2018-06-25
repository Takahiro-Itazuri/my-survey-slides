#### Two-Stream Convolutional Networks for Action Recognition in Videos
###### Karen Simonyan, Andrew Zisserman

@div[left]

__概要__<br>
人間の視覚は脳内で腹側（物体認識）と背側（動き認識）に分かれているという仮説を元に、行動認識タスクにおける空間特徴量と時間特徴量を個別に抽出する2つネットワークを利用したネットワーク（Two-Stream CNN）を提案した。<br>
<br>
__手法・新規性__<br>
Temporal-stream CNNは密なオプティカルフローを入力とする。密なオプティカルフローは変位ベクトル場と捉え、`$x$`軸と`$y$`軸に分解し、2チャンネルの画像にする。密なオプティカルフロー以外にも、トラジェクトリーや双方向オプティカルフローとも比較を行った。<br>

@divend

@div[right]

![Two-Stream CNN](assets/img/Two-Stream_CNN.png =full)<br>
<br>

__リンク__<br>
・[論文](https://papers.nips.cc/paper/5353-two-stream-convolutional-networks-for-action-recognition-in-videos.pdf)<br>

@divend