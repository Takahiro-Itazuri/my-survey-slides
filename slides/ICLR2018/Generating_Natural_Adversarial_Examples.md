#### Generating Natural Adversarial Examples
###### Zhengli Zhao, Dheeru Dua, Sameer Singh

@div[left]

__概要__<br>
perturbation-based adversarial examplesは不自然であり、人間にとっては意味を見出すことができないことを指摘した上で、データの多様体上に存在する自然なadversarial examplesを生成するため、低次元な密な潜在変数からデータ多様体へ写像する関数をGANで学習し、GANでadversarial examplesを生成する手法を提案した。<br>
<br>
__手法・新規性__<br>
GANと同時に画像を潜在変数に射影するinverterを学習させる。generator `$\mathcal{G}_{\theta}$`、critic `$\mathcal{C}_{\omega}$`、inverter `$\mathcal{I}_\gamma$`が与えられたとき、以下の学習を行う。<br>
`\begin{align} & \min_{\theta} \max_{\omega} \mathbb{E}_{x \sim p_x} \left[ \mathcal{C}_{\omega} (x) \right] - \mathbb{E}_{z \sim p_z} \left[ \mathcal{C}_{\omega} ( \mathcal{G}_{\theta} (z) ) \right] \\ & \min_{\gamma} \mathbb{E}_{x \sim p_x} \| \mathcal{G}_{\theta} ( \mathcal{I}_{\gamma} (x) ) - x \| + \lambda \cdot \mathbb{E}_{z \sim p_z} \left[ \mathcal{L} (z, \mathcal{I}_{\gamma} (\mathcal{G}_{\theta} (z))) \right] \end{align}`
上述の学習を行ったモデルを利用して、以下のようなadversarial examplesを探索する。<br>
`\begin{align} x^{\ast} = \mathcal{G}_{\theta} (z^{\ast}) {\rm \; where \;} z^{\ast} = \mathop{\rm arg~min}\limits_{\hat{z}} \| \hat{z} - \mathcal{I}_{\gamma} (x) \| {\rm \; s.t. \;} f(\mathcal{G}_{\theta} (\hat{z})) \neq f(x) \end{align}`
これを探索する方法として、iterative stochastic searchとhybrid shrinking searchを提案した。

@divend

@div[right]

![](assets/img/Generating_Natural_Adversarial_Examples.png =full)<br>
<br>

__リンク__<br>
・[論文](https://openreview.net/pdf?id=H1BLjgZCb)<br>
・[GitHub](https://github.com/zhengliz/natural-adversary)<br>

@divend