#### Learning Attentions: Residual Attentional Siamese Network for High Performance Online Visual Tracking
###### Qiang Wang, Zhu Teng, Junliang Xing, Jin Gao, Weiming Hu, Steve Maybank

@div[left]

__概要__<br>
物体追跡のためのオフライン学習ベースの手法は精度とスピードにおいて高いポテンシャルがあるが、追跡対象に適応させることは困難である。一方で、オンライン学習ベースの手法は計算コストとオーバーフィッティングが問題になっている。本論文では、Siamese NetworkにおけるCross CorrelationをAttentionで重み付けしたRASNet（Residual Attentional Siamese Network）を提案し、リアルタイムを超える速度（83fps）とSOTAを実現した。<br><br>
__手法・新規性__<br>
通常のSiamese NetworkにAttention Mechinismを導入して、以下のように定式化した。<br>
`$$ f(z, x) = (\gamma \odot \phi(z)) \ast \phi(x) + b \cdot \mathbb{1} $$`
Attention $ \gamma $を学習させるのは困難なため、Residual AttentionとGeneral Attentionを含むDual Attention ($ \rho $)とChannel Attention ($ \beta $)を導入し、以下のように再定式化した。<br>
`$$ f_{p', q'} = \sum_{i=0}^{m-1} \sum_{j=0}^{n-1} \sum_{c=0}^{d-1} \rho_{i,j} \beta_{c} \phi_{i,j,c} (z) \phi_{p'+i,q'+j,c}(x) + b $$`

@divend

@div[right]

![RASNet](assets/img/RASNet.png =full)<br>

__リンク__<br>
・[論文](http://www.dcs.bbk.ac.uk/~sjmaybank/CVPR18RASTrackCameraV3.3.pdf)<br>
・[GitHub](https://github.com/foolwood/RASNet)<br>

@divend