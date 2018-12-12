#### Learning to Segment Object Candidates
###### Pedro O. Pinheiro, Ronan Collobert, Piotr Dollar

@div[left]

__概要__<br>
本論文では、CNNを用いてObject Proposalを生成する手法（DeepMask）を提案した。DeepMaskはEdgeやSuperpixel、Low-level Featureを用いずにSegmentation Proposalを生成することが可能である。<br>
<br>
__手法・新規性__<br>
学習データは、サンプル`$k$`に対して、RGBの入力パッチ`$x_k$`、入力パッチに対応するバイナリマスク`$m_k$`、ラベル`$y_k \in \left\{ \pm 1 \right\}$`で与えられる。ラベル`$y_k=1$`の場合、(1)パッチのおおよそ中心付近に物体が位置していることと(2)パッチ内に完全に物体が含まれることを満たしている。DeepMaskはVGGから得た特徴量を使用して、SegmentationブランチとScoringブランチに分かれた構造を持つ。Scoreは、与えられたパッチ内に物体が中心に位置し、完全に含まれているかの度合いを表す。Semantic Segmentationとは異なり、パッチ内に複数物体が存在した場合、中心の物体だけに注目させるため、Segmentationブランチは一度全結合層に情報を落としている。また損失関数は以下を使用している。<br>
`\begin{align} \mathcal{L}(\theta) \end{align}`

@divend

@div[right]

![](path/to/img =full)<br>
<br>

__リンク__<br>
・[論文](https://papers.nips.cc/paper/5852-learning-to-segment-object-candidates.pdf)<br>
・[](url)<br>

@divend