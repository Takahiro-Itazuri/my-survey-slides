#### Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift
###### Sergey Ioffe, Christian Szegedy

@div[left]

__概要__<br>
各層の入力の分布が学習中に変化していくことが深層学習を複雑にさせている。その結果、学習率を小さく設定したり、注意深く初期値を設定する必要がある。この現象を内部共変シフト（Internal Covariate Shift）と呼ぶ。この問題を解決するため、学習時に各ミニバッチに対して正規化を行うBatch Normalizationを提案し、勾配消失が緩和された結果、深層学習の学習を速く収束させることが可能になった。<br>
<br>
__手法・新規性__<br>
入力として`$m$`個のミニバッチ`$\mathcal{B}$`が与えられたとき、平均と分散は以下のように計算される。<br>
`\begin{align} \mathcal{B} = \left\{ \boldsymbol{x}_1 \cdots \boldsymbol{x}_m \right\} \\ \boldsymbol{\mu}_{\mathcal{B}} = \frac{1}{m} \sum_{i=1}^{m} \boldsymbol{x}_i \\ \boldsymbol{\sigma}_{\mathcal{B}}^{2} \frac{1}{m} \sum_{i=1}^{m} \left( \boldsymbol{x}_i - \boldsymbol{\mu} \right)^2 \end{align}`
これらを用いて、ミニバッチの各要素を正規化する。<br>
`\begin{align} \hat{\boldsymbol{x}}_i = \frac{\boldsymbol{x}_i - \boldsymbol{\mu}_{\mathcal{B}}}{\sqrt{\boldsymbol{\sigma}_{\mathcal{B}}}} \end{align}`
これに対して学習可能なスケーリング（`$\gamma$`）とシフト（`$\beta$`）をするパラメータを導入する。<br>
`\begin{align} \boldsymbol{y}_i = \gamma \hat{\boldsymbol{x}}_i + \beta \end{align}`
Batch Normalizationは活性化関数の直前に入れる。

@divend

@div[right]

![](assets/img/BatchNormalization.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1502.03167.pdf)<br>
・[計算グラフ](https://kratzert.github.io/2016/02/12/understanding-the-gradient-flow-through-the-batch-normalization-layer.html)<br>

@divend
