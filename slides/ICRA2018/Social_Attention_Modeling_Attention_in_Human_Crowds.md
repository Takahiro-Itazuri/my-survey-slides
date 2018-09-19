#### Social Attention: Modeling Attention in Human Crowds
###### Anirudh Vemula, Katharina Muelling, Jean Oh

@div[left]

__概要__<br>
従来の複数の人間の移動予測手法では、近傍にいる人間までの距離のみを考慮していたが、実際にはその人間の速度、衝突までの時間、加速度や方向なども考慮に入れるべきである。本論文では、Structural-RNN（S-RNN）にattetion moduleを導入したSocial Attentionを提案した。<br>
<br>
__手法・新規性__<br>
S-RNNはnodeRNNとedgeRNNから構成されており、各ノードごとに定義される。ノード間でnodeRNNと空間edgeRNNと時間edgeRNNはそれぞれ重みを共有している。提案手法では、各ノード`$v$`に対する空間edgeRNN`${\bf R}_v$`の隠れ状態`$h_v^t$`に対してsoft attentionを計算する。<br>


@divend

@div[right]

![Social Attention](assets/img/Social_Attention_Modeling_Attention_in_Human_Crowds.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1710.04689.pdf)<br>

@divend