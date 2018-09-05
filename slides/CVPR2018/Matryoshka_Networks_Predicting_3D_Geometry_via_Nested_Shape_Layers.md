#### Matryoshka Networks: Predicting 3D Geometry via Nested Shape Layers
###### Stephan R. Richter, Stefan Roth

@div[left]

__概要__<br>
2次元画像から3次元形状を復元する論文。DNNを使って3次元形状を推定する手法は、voxelを直接出力するようになっており、GPUのメモリ容量の制限から高解像度な3次元形状を復元することができなかった。本論文では、メモリ効率を良くするため、特定の方向へ延びるtubeが各ピクセルに対応する二次元表現voxel tubeを出力するshape layerを提案した。またネスト構造を持たせたshape layerを適用することで、自己遮蔽領域への対応したネットワークMatryoshka Networkを提案した。<br>
<br>
__手法・新規性__<br>
shape layerは6軸方向から見た深度画像を出力し、各軸に対応する2つの深度画像に挟まれた領域の共有部分を出力する。この場合、すべての軸から見ても遮蔽されている領域を復元することができないため、マトリョーシカのようなネスト構造を持つshape layerを出力するMatryoshka Networkを提案し、このネットワークは集合の差と和集合を交互に繰り返すネスト構造を持つ。<br>


@divend

@div[right]

![Matryoshka Networks](assets/img/Matryoshka_Networks_Predicting_3D_Geometry_via_Nested_Shape_Layers.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Richter_Matryoshka_Networks_Predicting_CVPR_2018_paper.pdf)<br>

@divend