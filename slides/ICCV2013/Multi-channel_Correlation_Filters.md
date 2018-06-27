#### Multi-channel Correlation Filters
###### Hamed Kiani Galoogahi, Terence Sim, Simon Lucey

@div[left]

__概要__<br>
従来single-channelのCorrelation Filter（CF）における進歩があったが、multi-channelのCFを効率的に学習する手法がなかった。本論文では時間計算量と空間計算量の効率が良いmulti-channel CFを提案した。<br>
<br>
__手法・新規性__<br>
以下の式を最小化する問題を解く。<br>
`\begin{align} E ({\bf h}) = \frac{1}{2} \sum_{i=1}^{N} \sum_{j=1}^{D} \| {\bf y}_i (j) - \sum_{k=1}^{K} {\bf h}^{(k)T} {\bf x}_i^{(k)} \left[ \Delta \tau_j \right] \|^2 + \frac{\lambda}{2} \sum_{k=1}^{K} \| {\bf h}^{(k)} \|^2 \end{align}`
これを周波数空間上で考えると、以下のようになる。<br>
`\begin{align} E(\hat{{\bf h}}) &= \frac{1}{2} \sum_{i=1}^{N} \| \hat{{\bf y}}_i - \sum_{k=1}^{K} {\rm diag} \left( \hat{{\bf x}}_i^{(k)} \hat{{\bf h}}^{(k)} \right) \|^2 + \frac{\lambda}{2} \sum_{k=1}^{K} \| \hat{{\bf h}}^{(k)} \|^2 \\ &= \frac{1}{2} \sum_{i=1}^{N} \| \hat{{\bf y}}_i - \hat{{\bf X}}_i \hat{{\bf h}} \|^2 + \frac{\lambda}{2} \| \hat{{\bf h}} \|^2 \end{align}`
ただし、`$\hat{{\bf h}} = \left[ \hat{{\bf h}}^{(1)T}, \cdots, \hat{{\bf h}}^{(K)T} \right]$`、`$\hat{{\bf X}}_i = \left[ {\rm diag} \left( \hat{{\bf x}}_i^{(1)} \right), \cdots, {\rm diag} \left( \hat{{\bf x}}_i^{(K)} \right) \right]$`である。以上より<br>
`\begin{align} \hat{{\bf h}}^{\ast} = \left( \lambda {\bf I} + \sum_{i=1}^{N} \hat{{X}}_i^T \hat{{\bf X}}_i \right)^{-1} \sum_{i=1}^{N} \hat{{\bf X}}_i^T \hat{{\bf y}}_i \end{align}`

@divend

@div[right]

![MCCF](assets/img/MCCF.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_iccv_2013/papers/Galoogahi_Multi-channel_Correlation_Filters_2013_ICCV_paper.pdf)<br>

@divend