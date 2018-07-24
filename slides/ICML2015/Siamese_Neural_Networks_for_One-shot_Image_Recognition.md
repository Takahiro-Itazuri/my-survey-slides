#### Siamese Neural Networks for One-shot Image Recognition
###### Gregory Koch, Richard Zemel, Ruslan Salakhutdinov

@div[left]

__概要__<br>
本論文では、One-shot Image Recognitionを行うDeep Siamese Networkを提案した。Siamese Neural Networksは２つの入力を受け取り、それらが同一のクラスに属するかどうかを学習するMetric Learningの１種である。提案手法はOmniglotデータセットにおいてSoTAを達成した。<br>
<br>
__手法・新規性__<br>
`$L$`層からなるネットワークの`$l$`層目の隠れベクトルを２つの入力対してそれぞれ`${\bf h}_{1,l}, {\bf h}_{2,l}$`とする。畳み込み層の最後の層から得られた特徴量をベクトル化し、それらのL1ノルムに対して、sigmoid関数を適用したものを出力確率`$p$`とする。<br>
`\begin{align} {\bf p} = \sigma \left( \sum_j \alpha_j | {\bf h}_{1,L-1}^{(j)} - {\bf h}_{2,L-1}^{(j)} | \right) \end{align}`
出力確率`$p$`は２つの入力が同じクラスの場合に`$1$`を、異なるクラスの場合に`$0$`を出力するように学習する。この確率に対して、cross-entropy lossを損失関数とする。<br>
`\begin{align} \mathcal{L} \left( x_1^{(i)}, x_2^{(i)} \right) = {\bf y} \log {\bf p} (x_1^{(i)}, x_2^{(i)}) + (1 - {\bf y}) \log (1 - {\bf p} (x_1^{(i)}, x_2^{(i)})) + {\bf \lambda}^T |{\bf w}|^2 \end{align}`

@divend

@div[right]

![Siamese_Neural_Networks_for_One-shot_Image_Recognition](assets/img/Siamese_Neural_Networks_for_One-shot_Image_Recognition.png =full)<br>
<br>

__リンク__<br>
・[論文](https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf)<br>

@divend