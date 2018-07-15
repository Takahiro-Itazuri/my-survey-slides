#### HydraNets: Specialized Dynamic Architectures for Efficient Inference
###### Ravi Teja Mullapudi, William R. Mark, Noam Shazeer, Kayvon Fatahalian

@div[left]

__概要__<br>
DNNの高い精度を保持したまま計算コストの削減が可能なHydraNetを提案した。HydraNetには推論時に入力に対して良い精度を出すようにネットワークアーキテクチャの部分集合を選択するsoft gating mechanismが組み込まれている。このような動的な構造を持たせることでaccuracy-per-unit-costを向上させた。実験では、画像分類タスクにおいてResNetやDenseNetと同等の精度をより少ない計算コストで出した。<br>
<br>
__手法・新規性__<br>
HydraNetは複数のbranchで構成され、各branchは特定のsubtask特化するように学習されている。その後、gating mechanismによって動的に適切なbranchを選択し、その選択されたbranchから来る特徴量を統合し、最終的な推論を行う。HydraNetでは、各branchは最後の推論までは行わず、subtaskに対応する特徴量だけを計算するような構造になっていることが計算効率の向上につながっている。<br>


@divend

@div[right]

![HydraNets](assets/img/HydraNets.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Mullapudi_HydraNets_Specialized_Dynamic_CVPR_2018_paper.pdf)<br>

@divend