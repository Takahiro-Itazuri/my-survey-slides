#### AttnGAN: Fine-Grained Text to Image Generation with Attention Generative Adversarial Networks
###### Tao Xu, Pengchuan Zhang, Qiuyuan Huang, Han Zhang, Zhe Gan, Xiaolei Huang, Xiaodong He

@div[left]

__概要__<br>
本論文ではテキスト入力を画像に変換するネットワークAttentional Generative Adversarial Network（AttnGAN）を提案した。従来の手法はテキスト全体を表現するglobal sentence vectorを媒介してGANで画像合成をしていたが、AttnGANはテキスト入力の各wordに対応する画像領域をAttentionとして与えることができるため、より細かな画像合成が可能である。またAttnGANに加えて、入力のテキストと生成した画像の類似度を測るモデルDeep Attentional Multimodal Similarity Model（DAMSM）を提案した。<br>
<br>
__手法・新規性__<br>
AttnGANは`$m$`個のGenerator`$(G_0, \cdots, G_{m-1})$`で構成されており、それぞれの入力となる隠れ状態`$(h_0, \cdots, h_{m-1})$`と生成された画像`$(\hat{x}_0, \cdots, \hat{x}_{m-1})$`は以下のように記述できる。<br>
`\begin{align} h_0 &= F_0 (z, F^{ca} (\overline{e})) \\ h_i &= F_i (h_{i-1}, F_i^{attn} (e, h_{i-1})) \\ \hat{x}_i &= G_i (h_i) \end{align}`
`$\overline{e}$`はglobal sentence vectorであり、`$e$`はword vectorで構成された行列である。また`$F^{ca}$`はsentence vectorをconditioning vectorに変換するConditioning Augmentation、`$F^{attn}$`はAttention Modelである。<br>
損失関数は以下の式で定義される。<br>
`\begin{align} \mathcal{L} = \mathcal{L}_G + \lambda \mathcal{L}_{DAMSM} \end{align}`
`$\mathcal{L}_G$`はGANとCGANを合わせた損失であり、`$\mathcal{L}_{DAMSM}$`は画像とテキストのマッチングを見る損失である。<br>

@divend

@div[right]

![AttnGAN](assets/img/AttnGAN.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Xu_AttnGAN_Fine-Grained_Text_CVPR_2018_paper.pdf)<br>
・[GitHub](https://github.com/taoxugit/AttnGAN)<br>

@divend