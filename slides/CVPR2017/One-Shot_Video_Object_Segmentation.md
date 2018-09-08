#### One-Shot Video Object Segmenation
###### Sergi Caelles, Kevis-Kokitsi Maninis, Jordi Pont-Tuset, Laura Leal-Taixe, Daniel Cremers, Luc Van Gool

@div[left]

__概要__<br>
本論文では、動画の一枚目におけるforeground maskのみで学習するOne-Shot Video Object Segmentation（OSVOS）を提案した。OSVOSはframe-by-frameに処理を行っているが、十分なtemporal consistencyを持つ。OSVOSはSoTAを大きく上回り、学習画像を増やせば増やすほど精度に向上が見られた。<br>
<br>
__手法・新規性__<br>
人間が物体を追跡する時は、「それが物体であるかどうか」を認識した後、「それが特定の物体であるかどうか」を認識する。これに感化され、提案手法はまず前景になりうる一般的な物体を分離できるように学習した後、特定の与えられた物体に対して若干のfine-tuningを行う手法を提案した。Foreground Maskを推定するForeground Maskに加えて、境界を推定するContour Branchを加えたTwo-Stream構造を取り、最後にBoundary Snappingというより正確なForeground Maskを抽出する処理を行う手法も提案したが、これの精度と処理時間はトレードオフである。<br>

@divend

@div[right]

![](assets/img/One-Shot_Video_Object_Segmentation.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2017/papers/Caelles_One-Shot_Video_Object_CVPR_2017_paper.pdf)<br>
・[プロジェクト](http://people.ee.ethz.ch/~cvlsegmentation/osvos/)<br>
・[GitHub (PyTorch)](https://github.com/kmaninis/OSVOS-PyTorch)<br>
・[GitHub (Caffe)](https://github.com/kmaninis/OSVOS-caffe)<br>
・[GitHub (TensorFlow)](https://github.com/scaelles/OSVOS-TensorFlow)<br>

@divend