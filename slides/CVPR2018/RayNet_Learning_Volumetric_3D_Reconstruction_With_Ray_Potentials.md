#### RayNet: Learning Volumetric 3D Reconstruction With Ray Potentials
###### Despoina Paschalidou, Osman Ulusoy, Carolin Schmitt, Luc Van Gool, Andreas Geiger

@div[left]

__概要__<br>
異なる視点から撮影された映像から、CNNとMRFを用いて物理的制約を考慮可能な密な３次元復元を行った論文。CNNはタスクに対してネットワーク全体をデータから学習可能であるが、物理的制約を考慮することができない。一方でRay-Potentialを用いたMRFはモデルに陽な物理的制約を与えることができる一方で、大きな表面を上手く扱うことができない。本論文ではこの２つの手法の良いところをそれぞれ活かした手法であるRayNetを提案した。<br>
<br>
__手法・新規性__<br>
構造としては、Multi-View CNNとMarkov Random Fieldから構成されている。Multi-View CNNは入力として複数の画像とそれに対応するカメラの姿勢を受け取り、視点による影響が小さい特徴量を抽出し、Rayごとにデプスの分布を出力する。Morkov Random Fieldは各視点からにおける遮蔽を考慮して、CNNから出力されたデプスの分布のノイズを除去する。<br>

@divend

@div[right]

![RayNet](assets/img/RayNet_Learning_Volumetric_3D_Reconstruction_With_Ray_Potentials.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Paschalidou_RayNet_Learning_Volumetric_CVPR_2018_paper.pdf)<br>

@divend