#### Correlation Tracking via Joint Discrimination and Realiability Learning
###### Chong Sun, Dong Wang, Huchuan Lu, Ming-Hsuan Yang

@div[left]

__概要__<br>
Correlation Filterベースの物体追跡手法は識別性と信頼性を学習するべきであるが、従来手法は識別性に着目したものが多く、Bounding Box内の予期されない顕著な領域に影響を受ける可能性がある。提案手法は識別性を保持するbase filterと信頼性を保持するreliability termのアダマール積を取ることで、より信頼性の高い領域に着目する物体追跡手法（DRT）を提案する。<br>
<br>
__手法・新規性__<br>
DRTにおけるフィルタは以下の式で与えられる。<br>
`\begin{align} {\bf w}_d &= {\bf h}_d \odot {\bf v}_d \\ {\bf v}_d &= \sum_{m=1}^{M} \beta_{m} {\bf p}_{d}^{m} \end{align}`
目的関数は以下の式で与えられる。<br>
`\begin{align} f({\bf h}, {\bf \beta}; {\bf X}) = f_1 ({\bf h}, {\bf \beta}; {\bf X}) + \eta f_2 ({\bf h}; {\bf X}) + \gamma \| {\bf h} \|_2^2 \end{align}`
`$f_1$`は学習サンプルの識別誤差項、`$f_2$`は局所応答に一貫性を持たせる制約項、最後の項はL2ノルム正則化項である。<br>
`\begin{align} & f_1 ({\bf h}, {\bf \beta}; {\bf X}) = \sum_{k=1}^{K} \left( y_k - \sum_{d=1}^{D} {\bf x}_{k, d}^{T} ({\bf v}_d \odot {\bf h}_d) \right)^2 \\ & f_2({\bf h}; {\bf X}) = \sum_{k=1}^{K} \sum_{m, n}^{M} \left( \sum_{d=1}^{D} ({\bf P}_{d}^{m}  {\bf x}_{k, d})^T {\bf h}_d - \sum_{d=1}^{D} ({\bf P}_{d}^{n} {\bf x}_{k, d})^T  {\bf h}_d \right)^2 \\ & {\bf P}_{d}^{m} = {\rm diag} ({\bf p}_{d}^{m} (1), {\bf p}_{d}^{m} (2), \cdots, {\bf p}_{d}^{m} (K)) \in \mathbb{R}^{K \times K} \end{align}`

@divend

@div[right]

![DRT](assets/img/DRT.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Sun_Correlation_Tracking_via_CVPR_2018_paper.pdf)<br>

@divend