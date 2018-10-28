#### cGANs with Projection Discriminator
###### Takeru Miyato, Masanori Koyama

@div[left]

__概要__<br>
従来のconditional GAN（cGAN）のDiscriminatorでは、条件の情報を潜在変数や特徴量に連結させて学習させていたが、GANのDiscriminatorの最適解を変形し、その裏に潜む確率モデルにおける条件の情報の役割を考慮することで導かれる構造（projection）を提案した。これにより、ILSVRC2012の1000クラスの画像であっても高い質の画像を生成することが可能になった。<br>
<br>
__手法・新規性__<br>
入力`$x$`、条件`$y$`が与えられ、`$q$`を目的の分布、`$p$`をGeneratorの分布とする。このとき、cGANの損失関数は以下の式で表すことができる。<br>
`\begin{align} \mathcal{L}(D) = - E_{q(y)} \left[ E_{q(x|y)} \left[ \log D(x,y) \right] \right]- E_{p(y)} \left[ E_{p(x|y)} \left[ \log (1 - D(x,y)) \right] \right]  \end{align}`
この損失関数に対するDiscriminatorの最適解は以下のようになる。<br>
`\begin{align} D(x,y) = \frac{q(x|y)q(y)}q(x|y)q(y) + {p(x|y)p(y)} \end{align}`
出力層における活性化関数がSoftmax関数であることを考慮すると、以下のように２つの対数尤度の比の和で表すことができる。<br>
`\begin{align} f^{\ast}(x,y) = \log \frac{q(x|y)q(y)}{p(x|y)p(y)} = \log \frac{q(y|x)}{p(y|x)} + \log \frac{q(x)}{p(x)} \end{align}`
この２つの対数尤度を出力するような関数`$f_1, f_2$`を学習させる場合、以下の形式で表現することができる（詳細は論文を参照）。<br>
`\begin{align} f(x,y;\theta) = f_1(x,y;\theta) + f_2 (x;\theta) = y^T V \phi (x;\theta_{\Phi}) + \psi (\phi (x;\theta_{\Phi}); \theta_{\Psi}) \end{align}`
特筆すべきは、クラスの情報を連結ではなく内積によって導入することである。実際には、この定式化はGeneratorの学習を不明瞭にするが、`$p$`と`$q$`が比較的シンプル（ガウス分布等）であることを仮定することによって、安定的に学習することが可能になる。

@divend

@div[right]

![](assets/img/cGANs_with_Projection_Discriminator.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1802.05637.pdf)<br>
・[GitHub](https://github.com/pfnet-research/sngan_projection)<br>

@divend