#### Dataset Distillation
###### Tongzhou Wang, Jun-Yan Zhu, Antonio Torralba, Alexei A. Efros

@div[left]

__概要__<br>
データセットにおける知識蒸留を行った。これまで知識蒸留の方法として、ネットワークの蒸留、アンサンブル学習における蒸留、モデル圧縮のための蒸留が提案されてきた一方で、提案手法では大量にデータから構成されるデータセットの情報を非常に少ない数のデータに蒸留する。<br>
<br>
__手法・新規性__<br>
データセット`$ \boldsymbol{x} = \left\{x_i\right\}_{i=1}^{N}$`に対して、通常のSGDでは、モデルのパラメータ`$\theta$`は`$t$`ステップ目のミニバッチ`$\boldsymbol{X}_t$`に対して、以下の式でモデルが更新される。<br>
`\begin{align} \theta_{t+1} = \theta_t - \eta \nabla_{\theta_t} l(\boldsymbol{x}_t, \theta_t) \end{align}`
提案手法はこれに対して、少量のデータ`$\hat{\boldsymbol{x}}=\left\{ \hat{x}_i \right\}_{i=1}^{M} (M \ll N)$`と学習率`$\hat{\eta}$`を用いてモデルのパラメータを以下のように更新する。<br>
`\begin{align} \theta_1 = \theta_0 - \hat{\eta} \nabla_{\theta_0} l (\hat{\boldsymbol{x}}, \theta_0) \end{align}`
このような更新に基づいて学習されたパラメータが最適になるように少量のデータ`$\hat{\boldsymbol{x}}$`と学習率`$\hat{\eta}$`を以下の式で最適化する。<br>
`\begin{align} \min_{\hat{\boldsymbol{x}}, \hat{\eta}} \mathcal{L} (\hat{\boldsymbol{x}}, \hat{\eta}; \theta_0) &= \min_{\hat{\boldsymbol{x}}, \hat{\eta}} l(\boldsymbol{x}, \theta_1) \\ &= \min_{\hat{\boldsymbol{x}}, \hat{\eta}} l(\boldsymbol{x}, \theta_0 - \hat{\eta} \nabla_{\theta_0} l (\hat{\boldsymbol{x}}, \theta_0)) \end{align}`
上式の定式化においては固定された初期値に対する最適化を行っているが、ある確率分布`$p(\theta_0)$`によって初期化されたモデルに対する最適化についても次式のように定式化することが可能である。<br>
`\begin{align} \min_{\hat{\boldsymbol{x}}, \hat{\eta}} \mathbb{E}_{\theta_0 \sim p(\theta_0)} \left[ \mathcal{L} (\hat{\boldsymbol{x}}, \hat{\eta}; \theta_0) \right] \end{align}`
上式においては１度の勾配降下による定式であったが、複数回の更新に適用する方法として各ステップごとに異なる蒸留データと学習率を用意することが可能である。実験の結果、特定の値で初期化された場合の蒸留データはノイズのように見えるが、確率的にランダムに初期化されるパラメータに適用できるようにdata distillationを行うと蒸留データに人間が意味を見出すことができる模様が出てきている。

@divend

@div[right]

![](assets/img/Dataset_Distillation.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1811.10959.pdf)<br>

@divend