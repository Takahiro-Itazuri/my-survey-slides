#### Tutorial on Variational Autoencoders
###### Carl Doersch

@div[left]

__概要__<br>
変分ベイズの知識を前提としないVAEのチュートリアル論文。<br>
<br>
__手法・新規性__<br>
解きたい問題は、学習データ`$X$`が生成される確率`$P(X)$`を最大化するネットワークのパラメータ`$\theta$`を求める問題である。この確率`$P(X)$`は潜在変数`$z$`で周辺化されて、以下のように記述できる。<br>
`\begin{align} P(X) = \int P(X|z;\theta) P(z) dz \end{align}`
VAEでは潜在変数に対して、ガウス分布などの確率分布を仮定することができる。<br>
`\begin{align} P(X|z;\theta) \sim \mathcal{N} (X|0, I) \end{align}`
ここで問題となるのは、(1)どのようにして潜在変数`$z$`を決定するかと(2)潜在変数`$z$`に関する積分をどう扱うかである。

@divend

@div[right]

![](path/to/img =full)<br>
<br>

__リンク__<br>
・[](url)<br>
・[](url)<br>

@divend