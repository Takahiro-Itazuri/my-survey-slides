#### VITAL: VIsual Tracking via Adversarial Learning
###### Yibing Song, Chao Ma, Xiaohe Wu, Lijun Gong, Linchao Bao, Wangmeng Zuo, Chunhua Shen, Rynson Lau, Ming-Hsuan Yang

@div[left]

__概要__<br>
tracking-by-detectionベースの手法は、(1)各フレームにおけるpositive sampleが空間的に重なった領域を取りやすいため、十分な見た目のばらつきを学習できない点と(2)positive sampleとnegative sampleの不均等さ（class imbalance）が顕著に出てしまうという点が問題である。本論文では、positive sampleのデータ拡張を行うため、GANを用いて長い時間のスパンで頑健な特徴を学習可能なVITALアルゴリズムを提案した。またclass imbalanceを解決するため、識別が容易なnegative sampleを取り除くためのhigh-order cost sensitive lossを提案した。<br><br>
__手法・新規性__<br>
提案手法におけるGANはimage spaceではなくfeature spaceで学習データを拡張する。CNNで抽出した特徴量に対して重みを付けるマスク$M$を学習する。<br>
\begin{align}
a = b
\end{align}
`$$ \mathcal{L}_{VITAL} = \min_{G} \min_{D} \mathbb{E} [\log D(M \cdot C)] + \mathbb{E} [\log (1 - D(G(C) \cdots C))] + \lambda \mathbb{E} \| G(C) - M \|^2 $$`
high-order cost sensitive lossは識別が簡単すぎたnegative sampleはあまり学習に寄与しないようにする。<br>

@divend

@div[right]

![VITAL](assets/img/VITAL.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1804.04273.pdf)<br>
・[デモ動画](https://youtu.be/uGMoOom6_90)<br>
・[プロジェクト](https://ybsong00.github.io/cvpr18_tracking/index)<br>
・[GitHub](https://github.com/ybsong00/Vital_release)<br>

@divend