#### Multi-channel Correlation Filters
###### Hamed Kiani Galoogahi, Terence Sim, Simon Lucey

@div[left]

__概要__<br>
従来single-channelのCorrelation Filter（CF）における進歩があったが、multi-channelのCFを効率的に学習する手法がなかった。本論文では時間計算量と空間計算量の効率が良いmulti-channel CFを提案した。<br>
<br>
__手法・新規性__<br>
以下の式を最小化する問題を解く。<br>
`\begin{align} E (\boldsymbol{h}) = \frac{1}{2} \sum_{i=1}^{N} \sum_{j=1}^{D} \| \boldsymbol{y}_i (j) - \sum_{k=1}^{K} \boldsymbol{h}^{(k)T} \boldsymbol{x}_i^{(k)} \left[ \Delta \tau_j \right] \|^2 + \frac{\lambda}{2} \sum_{k=1}^{K} \| \boldsymbol{h}^{(k)} \|^2 \end{align}`
これを周波数空間上で考えると、以下のようになる。<br>
`\begin{align} E(\hat{\boldsymbol{h}}) &= \frac{1}{2} \sum_{i=1}^{N} \| \hat{\boldsymbol{y}}_i - \sum_{k=1}^{K} {\rm diag} \left( \hat{\boldsymbol{x}}_i^{(k)} \hat{\boldsymbol{h}}^{(k)} \right) \|^2 + \frac{\lambda}{2} \sum_{k=1}^{K} \| \hat{\boldsymbol{h}}^{(k)} \|^2 \\ &= \frac{1}{2} \sum_{i=1}^{N} \| \hat{\boldsymbol{y}}_i - \hat{\boldsymbol{X}}_i \hat{\boldsymbol{h}} \|^2 + \frac{\lambda}{2} \| \hat{\boldsymbol{h}} \|^2 \end{align}`
ただし、`$\hat{\boldsymbol{h}} = \left[ \hat{\boldsymbol{h}}^{(1)T}, \cdots, \hat{\boldsymbol{h}}^{(K)T} \right]$`、`$\hat{\boldsymbol{X}}_i = \left[ {\rm diag} \left( \hat{\boldsymbol{x}}_i^{(1)} \right), \cdots, {\rm diag} \left( \hat{\boldsymbol{x}}_i^{(K)} \right) \right]$`である。以上より<br>
`\begin{align} \hat{\boldsymbol{h}}^{\ast} = \left( \lambda \boldsymbol{I} + \sum_{i=1}^{N} \hat{{X}}_i^T \hat{\boldsymbol{X}}_i \right)^{-1} \sum_{i=1}^{N} \hat{\boldsymbol{X}}_i^T \hat{\boldsymbol{y}}_i \end{align}`

@divend

@div[right]

![MCCF](assets/img/MCCF.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_iccv_2013/papers/Galoogahi_Multi-channel_Correlation_Filters_2013_ICCV_paper.pdf)<br>

@divend