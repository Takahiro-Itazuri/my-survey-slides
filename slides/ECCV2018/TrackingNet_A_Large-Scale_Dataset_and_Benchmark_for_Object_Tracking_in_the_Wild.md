#### TrackingNet: A Large-Scale Dataset and Benchmark for Object Tracking in the Wild
###### Matthias Muller, Adel Bibi, Silvio Giancola, Salman Al-Subaihi, Bernard Ghanem

@div[left]

__概要__<br>
物体追跡用の大規模データセット（TrackingNet）を作成し、ベンチマークテストを行った論文。TrackingNetは30,643個の動画、14,431,266個のラベル付きフレームから構成される。従来のデータセットは大規模でなかったがゆえに、OTBデータセットで学習した後、VOTデータセットでテストするのが一般的となっていたり、複数のデータセットで共通する動画があるために、学習に使用するデータに注意を払う必要があった。<br>
<br>
__手法・新規性__<br>
物体検出用のデータセットであるYouTube-BoundingBoxes（YT-BB）からTrackingNetの学習データは生成されている。まず静的な物体に関する動画を除去した後、(1)短い時間の動画、(2)物体が画面を占める割合が50%を超える動画、(3)Bounding Boxの動きが少ない動画、計90%程度を除去した。アノテーションが疎な場合は複数の最新手法で補完した。TrackingNetのテストデータはCreative Commons LicenceがついたYouTube動画（YT-CC）から、物体のカテゴリの分散が学習データセットに近くなるように511個集め、Amazon Mechanical Turkを使って、アノテーションを付けた。TrackingNetを用いて、最新手法のベンチマークテストを行い、またTrackingNetで学習させることで、SiameseFCお精度を1.7%向上させた。<br>


@divend

@div[right]

![TrackingNet](assets/img/TrackingNet_A_Large-Scale_Dataset_and_Benchmark_for_Object_Tracking_in_the_Wild =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1803.10794.pdf)<br>
・[プロジェクト](https://silviogiancola.github.io/publication/2018-03-trackingnet/details/)<br>

@divend