#### Auto-Encoding Variational Bayes
###### Diederik P. Kingma, Max Welling

@div[left]

__概要__<br>
生成モデルである変分ベイズでは、複雑なモデルにおいてEMアルゴリズムで解析解を得ることができない点や潜在変数の因子分解が可能でなければいけない点が問題である。一方で通常のオートエンコーダーで得られた潜在変数の決まった分布が存在しないため、生成するときに必要な潜在変数に対して良い値を選択することができないという問題点がある。そこで潜在変数が特定の分布に従うように変分下限を変形し、またSGDで学習できるようにReperameterization Trickを導入した。<br>
<br>
__手法・新規性__<br>
変分ベイズにおける変分下限を最大化する問題を帰着させたのち、変分下限を以下のように変形する。<br>
`\begin{align} & KL(q_\phi (z|X)||p_\theta (z|X)) \\ & \; = - KL (q_\phi(z|X)||p(z)) + {\bf E}_{q_\phi (z|X)} \left[ \ln p_{\theta} (X|z) \right] \end{align}`
第一項は潜在変数を任意の確率分布`$p(x)$`に近づけるためのKLダイバージェンスであり、第二項はエンコーダ`$ q_\phi (z|X) $`に関するデータ`$X$`の対数尤度`$ \ln p_\theta (X|z)$`の期待値を最大化する項である。<br>
エンコーダに平均と分散を出力させ、それに基づいて潜在変数をサンプリングし、それをデコードするというネットワーク構造になっている。しかし、このままではサンプリングのところでSGDを適用できなくなってしまうため、分散にランダムノイズを乗せるテクニック（Reparameterization Trick）を提案した。

@divend

@div[right]

![VAE](assets/img/VAE.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1312.6114.pdf)

@divend
