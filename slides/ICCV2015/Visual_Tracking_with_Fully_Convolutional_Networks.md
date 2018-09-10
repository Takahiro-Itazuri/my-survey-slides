#### Visual Tracking with Fully Convolutional Networks
###### Lijun Wang, Wanli Ouyang, Xiaogang Wang, Huchuan Lu

@div[left]

__概要__<br>
本論文では、blackboxな特徴量抽出器であるCNNの中身を考察し、異なる２つの層から得られる特徴量を相補的に用い、また追跡対象に必要な特徴量マップの選択を行うことで非常に頑健なCNNを用いた物体追跡手法（FCNT：Fully　Convolutional Network based Tracker）を提案した。<br>
<br>
__手法・新規性__<br>
VGG-16のconv4-3とconv5-3の層に注目して、ニューロンの活性化についていくつかの観察を行った。まず特定の物体に対して特徴量マップ中で活性化している領域は非常にスパースであること、ある程度の数の特徴量マップだけで前景と背景を分離するのには十分であること、より深い層ほどより抽象度の高い特徴量を抽出していることがわかった。この観察を元に、VGGのconv4-3を利用したSpecific Network（SNet）とconv5-3を利用したGeneral Network（GNet）から構成されるネットワークを提案した。それぞれの層において、追跡対象を追跡するのに必要な特徴量マップを選択する。最後にSNetとGNetから得られたヒートマップを統合することで追跡対象の位置を得る。また背景の影響を防ぐため、SNetのみをオンライン学習させる。<br>


@divend

@div[right]

![](assets/img/Visual_Tracking_with_Fully_Convolutional_Networks.png =full)<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Wang_Visual_Tracking_With_ICCV_2015_paper.pdf)<br>
・[プロジェクト](http://scott89.github.io/FCNT/)<br>
・[GitHub](https://github.com/scott89/FCNT)<br>

@divend