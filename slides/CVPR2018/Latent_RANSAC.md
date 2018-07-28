#### Latent RANSAC
###### Simon Korman, Roee Litman

@div[left]

__概要__<br>
データサイズに依存せず、RANSACを定数時間で行えるようにした論文。RANSACのボトルネックはサンプリングした仮説を検証するステップにあるため、従来その検証を高速化する手法が提案されてきたが、提案手法は検証を行う前に潜在空間でフィルタリングを行うことで妥当な仮説のみを検証することで高速化を行った。<br>
<br>
__手法・新規性__<br>
従来のRANSACでは全ての仮説を検証していたが、提案手法ではそれを高速にフィルタリングする。このフィルタリングのプロセスは、まず潜在空間上にパラメータ化し、それに対してRandom Grid Hashingを用いて、現在の仮説がそれ以前に生成された仮設と衝突するか否かを検証することで行われる。この検証前のプロセスの改良に伴い、それに適した探索を終了する基準も提案した。<br>


@divend

@div[right]

![](assets/img/Latent_RANSAC.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Korman_Latent_RANSAC_CVPR_2018_paper.pdf)<br>

@divend