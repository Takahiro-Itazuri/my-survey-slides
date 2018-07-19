#### Image-to-Image Translation with Conditional Adversarial Networks
###### Phillip Isola, Jun-Yan Zhu, Tinghui Zhou, Alexei A. Efros

@div[left]

__概要__<br>
これまで画像処理、CG、CVの分野で、入力画像に対応する出力画像を得るタスク（Image-to-Image Translation Task）が取り組まれてきたが、それぞれのタスクに特化した異なる損失関数を定義し、ニューラルネットワークを学習させてきた。本論文はImage-to-Image Translationタスクに対して一般的に適用可能なネットワーク（pix2pix）を提案した。<br>
<br>
__手法・新規性__<br>
pix2pixは以下の損失関数を最適化するConditional GAN（CGAN）である。<br>
`\begin{align} \mathcal{L}_{CGAN} (G, D) = \mathbb{E}_{x,y} \left[ \log D(x,y) \right] + \mathbb{E}_{x,z} \left[ \log \left( 1 - D(x, G(x, z)) \right) \right] \end{align}`
この式に対して、求めたい生成モデル`$G^\ast$`は以下のように記述できる。<br>
`\begin{align} G^{\ast} = \mathop{\rm arg~min}\limits_{G} \mathop{\rm max}_{D} \mathcal{L}_{CGAN} (G, D) \end{align}`
通常のGANは以下の損失関数を最適化する。<br>
`\begin{align} \mathcal{L}_{GAN} (G, D) = & \mathbb{E}_{y} \left[ \log D(y) \right] \\ & + \mathbb{E}_{x,z} \left[ \log \left( 1 - D(G(x,z)) \right) \right] \end{align}`
この式よりDiscriminatorへの入力に`$x$`が加わっていることがわかる。<br>
pix2pixでは上述の式に加えて、L1ロスを追加して、以下の式を最適化する。<br>
`\begin{align} G^{\ast} &= \mathop{\rm arg~min}\limits_{G} \mathop{\rm max}\limits_{D} \mathcal{L}_{CGAN} (G, D) + \lambda \mathcal{L}_{L1} (G) \\ \mathcal{L}_{L1} (G) &= \mathbb{E}_{x,y,z} \left[ \| y  G(x,z) \|_1 \right] \end{align}`
L1ロスを加えることでartifactを軽減することができる。またアーキテクチャとしてはSkip Connectionを持つU-Netを用いることで、localな情報を保持することができるため、よりリアルな画像を生成できる。

@divend

@div[right]

![pix2pix](assets/img/pix2pix.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2017/papers/Isola_Image-To-Image_Translation_With_CVPR_2017_paper.pdf)<br>
・[GitHub](https://github.com/phillipi/pix2pix)<br>

@divend
