#### VITAL: VIsual Tracking via Adversarial Learning
###### Yibing Song, Chao Ma, Xiaohe Wu, Lijun Gong, Linchao Bao, Wangmeng Zuo, Chunhua Shen, Rynson Lau, Ming-Hsuan Yang

@div[left]

__概要__<br>
tracking-by-detectionベースの手法は、(1)各フレームにおけるpositive sampleが空間的に重なった領域を取りやすいため、十分な見た目のばらつきを学習できない点と(2)positive sampleとnegative sampleの不均等さ（class imbalance）が顕著に出てしまうという点が問題である。本論文では、positive sampleのデータ拡張を行うため、GANを用いて長い時間のスパンで頑健な特徴を学習可能なVITALアルゴリズムを提案した。またclass imbalanceを解決するため、識別が容易なnegative sampleを取り除くためのhigh-order cost sensitive lossを提案した。<br>
<br>
__手法・新規性__<br>
提案手法はCNNで抽出した特徴量に適用するマスクを複数（論文では9個）用意し、マスクを通じて重み付けられた特徴量に対して識別器$D$が対象物体か背景かの二値分類を行う。学習時には識別器$D$に最も悪い識別性能を出させたマスクを学習させる。テスト時には生成器$G$は取り除いておく。また識別が簡単すぎる大量のnegative sampleのロスが合計されて大きくなってしまう現象であるclass imbalanceを、あまり学習に寄与しないようにする。<br>
`\begin{align} \mathcal{L}_{VITAL} &= \min_{G} \min_{D} \mathbb{E} [K_1 \cdot \log D(M \cdot C)] \\ & \qquad + \mathbb{E} [K_2 \cdot \log (1 - D(G(C) \cdots C))] \\ & \qquad + \lambda \mathbb{E} \| G(C) - M \|^2 \\ K_1 &= 1 - D(M \cdot C) \\ K_2 &= D(G(C) \cdot C) \end{align}`

@divend

@div[right]

![VITAL](assets/img/VITAL_VIsual_Tracking_via_Adversarial_Learning.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1804.04273.pdf)<br>
・[デモ動画](https://youtu.be/uGMoOom6_90)<br>
・[プロジェクト](https://ybsong00.github.io/cvpr18_tracking/index)<br>
・[GitHub](https://github.com/ybsong00/Vital_release)<br>

@divend
