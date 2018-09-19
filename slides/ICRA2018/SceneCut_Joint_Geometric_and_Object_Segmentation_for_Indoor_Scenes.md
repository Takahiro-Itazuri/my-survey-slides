#### SceneCut: Joint Geometric and Object Segmentation for Indoor Scenes
###### Trung T. Pham, Thanh-Toan Do, Niko Sunderhauf, Ian Reid

@div[left]

__概要__<br>
本論文は、単一RGB-D画像から、未知の物体であっても意味のある領域（物体領域やシーンの表面）に分解する手法（SceneCut）を提案した。この分解には、物体らしさ（Objectness）と幾何的適合性（Geometry Fitting）を考慮した一つのエネルギー関数で評価する。SceneCutはSemantic Class Annotationを学習に用いずに、Instance Segmentationが可能である。<br>
<br>
__手法・新規性__<br>
SceneCutは、画像領域の階層的なツリー構造をどこで切るかという問題を、動的計画法で解く。SceneCutは、まず初めにConvolutional Oriented Boundaries Network（COB）により境界検出を行い、その境界に基づきHierarchical Segmentation Treeを構築し、これに対して最適なTree Cutを計算することで出力を得る。最適なセグメンテーション`$\mathcal{S}$`とそれに対応するパラメータ`$\mathcal{\theta}$`で表されるエネルギー`$E\left( \mathcal{S}, \mathcal{\theta} \right)$`を最大化する問題を解く。<br>
`\begin{align} \left\{ \mathcal{S}^{\ast}, \mathcal{\theta}^{\ast} \right\} = \mathop{\rm arg~max}\limits_{\mathcal{S}, \mathcal{\theta}} E(\mathcal{S}, \mathcal{\theta}) \end{align}`
この問題に対して、領域`$S_i$`とそのパラメータ`$\theta_i$`が与えられたときのスコア`$\psi (S_i, \theta_i)$`を以下のように定義する。<br>
`\begin{align} \psi (S_i, \theta_i) = \begin{cases} \sum_{x \in S_i} \log g(x,\theta_i) & \theta_i {\rm represents~a~plane} \\ |S_i| \log f(S_i) & {\rm otherwise} \end{cases} \end{align}$`<br>
`$f(S_i): S_i \mapsto \left[0, 1\right] $`は物体としての尤度であるObjectness Measureを表し、`$g(x,\theta_i): x, \theta_i \mapsto \left[ 0, 1 \right]$`は`$x$`を表面パラメータ`$\theta_i$`で表される表面モデルに割り当てる際の尤度であるGoodness-of-fitを表す（これらの式の詳細は論文を参照）。

@divend

@div[right]

![](assets/img/SceneCut_Joint_Geometric_and_Object_Segmentation_for_Indoor_Scenes.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1709.07158.pdf)<br>
・[GitHub](https://github.com/trungtpham/SceneCut)<br>

@divend