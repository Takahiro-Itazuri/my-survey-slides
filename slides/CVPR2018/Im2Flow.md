#### Im2Flow: Motion Hallucination from Static Images for Action Recognition
###### Ruohan Gao, Bo Xiong, Kristen Grauman

@div[left]

__概要__<br>
人間が一枚の静止画から動き情報を推定可能であることを受け、一枚の静止画から動き情報（フロー）の事前知識を得る手法を提案。具体的には動き情報の表現方法とU-Netの構造を変形させたエンコーダ・デコーダネットワークを提案。提案手法で得たフロー情報を利用することで、行動認識の精度が向上した。<br>
<br>
__手法・新規性__<br>
動き情報を動きの大きさ`$M$`と角度`$\theta$`（角度`$\theta$`は`$cos \theta$`と`$sin \theta$`に分解）の計３チャンネルで表現する。角度`$\theta$`は`$0$`と`$2 \pi$`が同じになる周期的な構造であるが、三角関数を用いることでこれを避けることができる。損失関数は(1)フロー自体の損失と(2)動き情報のコンテンツの損失の和で構成される。動き情報のコンテンツは、ResNetをUCF-101データセット上で行動認識にfine-tuningさせたものから取得し、推定したフローと正解のフローから得られたコンテンツの差から損失を得る。<br>

@divend

@div[right]

![](assets/img/Im2Flow.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1712.04109.pdf)<br>

@divend