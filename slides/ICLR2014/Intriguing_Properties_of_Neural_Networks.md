#### Intriguing Properties of Neural Networks
###### Christian Szegedy, Wojciech Zaremba, Ilya Sutskever, Joan Bruna, Dumitru Erhan, Ian Goodfellow, Rob Fergus

@div[left]

__概要__<br>
DNNは誤差逆伝搬法による教師あり学習で自動的に最適化が行われるため、人間の直感に反する特性を示すことがある。本論文では、そのような人間の直感に反する2つのDNNの特性について議論を行った。<br>
<br>
__手法・新規性__<br>
1つ目の特性は、CNNの出力層に近いハイレベルなユニットは各々独立にセマンティックな情報を含んでいると考えられているが、実際はすべてのユニットを合わせた空間全体がセマンティックな情報を含んでいるという特性である。これについて、入力`$x$`から得られる活性化`$\phi (x)$`と特定の（`i`番目の）ユニットの活性化を表す基底ベクトル`$e_i$`との内積が大きくなるような画像と、任意の特定の方向を向いたベクトル`$v$`との内積が大きくなるような画像は、共に同等の異なるセマンティックな情報を含んでいることを実験で確認した。2つ目の特性は、入力`$x$`に対して知覚ができないくらい微小な摂動`$r(\|r\| < \epsilon)$`を乗せること（これにより生成されたサンプルのことをAdversarial Examplesと呼ぶ）によって、簡単にCNNの推定を任意に操ることができることである。局所的な汎化性能（入力画像の近傍においても良い識別性能を示すこと（滑らかさ））が期待されるが、以下の最適化問題をBox-constrained L-BFGSで解くことでAdversarial Examplesを生成することができる。<br>
`\begin{align} {\rm minimize} c |r| + loss_f (x+r, l) \; {\rm s.t.} \; x+r \in \left[ 0, 1 \right]^m \end{align}`
またAdversarial Examplesは異なるモデルや異なるデータセットで学習させたモデルにおいても、識別精度を落とさせることが可能であることも実験で示した。AlexNetに関してリプシッツ定数の上界を各層で計算し、微小な入力の変動に対して大きな出力の変動を生み出せることを証明した。またリプシッツ定数の上界に対して正則化を行うことでネットワークの汎化性能を上げることが可能であることを示唆した。

@divend

@div[right]

![](assets/img/Intriguing_Properties_of_Neural_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1312.6199.pdf)<br>

@divend