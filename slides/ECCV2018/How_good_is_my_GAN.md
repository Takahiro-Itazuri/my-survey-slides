#### How good is my GAN?
###### Konstantin Shmelkov, Cordelia Schmid, Karteek Alahari

@div[left]

__概要__<br>
これまでGANの定量的な指標はあまり提案されておらず、また既存の評価尺度は不十分であり、特定のタスクに対して利用者が評価尺度を適合させる必要があった。そこでclass-conditional GANに対して一般的に適用できる新たな評価指標として、GAN-trainとGAN-testを提案した。GAN-trainはPrecision（質）、GAN-testはRecall（分布）に対応する。<br>
<br>
__手法・新規性__<br>
クラス分類の学習用データセットを`$S_t$`、検証用データセットを`$S_v$`とし、`$S_t$`を使って学習したGANで生成した画像データセット`$S_g$`とする。GAN-trainは、`$S_g$`で学習を行ったクラス分類器で、`$S_v$`を分類するテストを行った際の精度であり、これは`$S_g$`が`$S_t$`と同等の分布や広がりを持っているかどうかを意味しており、Recall（再現率）に対応する。一方、GAN-testは、`$S_t$`で学習を行ったクラス分類器で、`$S_g$`を分類するテストを行った際の精度であり、これは未知である`$S_t$`の分布にどれだけ`$S_g$`の分布が適合できているかを意味しており、Precision（適合率）に対応する。さらに、`$S_g$`によってデータ拡張をした際のクラス分類器の精度を比較した。データ拡張に用いた`$S_g$`のデータ数を大きくしていくと、途中で精度が飽和しており、これにより生成したデータの分散が評価できる。<br>


@divend

@div[right]

![](assets/img/How_good_is_my_GAN.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_ECCV_2018/papers/Konstantin_Shmelkov_How_good_is_ECCV_2018_paper.pdf)<br>
・[プロジェクト](http://thoth.inrialpes.fr/research/ganeval/)<br>
・[arXiv（Supplemental付き）](https://arxiv.org/pdf/1807.09499.pdf)

@divend