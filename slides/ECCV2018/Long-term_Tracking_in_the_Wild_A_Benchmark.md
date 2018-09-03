#### Long-term Tracking in the Wild: A Benchmark
###### Jack Valmadre, Luca Bertinetto, Joao F. Henriques, Ran Tao, Andrea Vedaldi, Arnold Smeulders, Philip Torr, Efstratios Gavves

@div[left]

__概要__<br>
従来の物体追跡データセットは短時間動画ばかりで構成されており、そのような短時間動画に特化した手法が提案されてきた。しかし、実用の際に必要となるのは、長時間動画における物体追跡であるため、そのような長時間動画の物体追跡データセット（OxUvA）を作成した。OxUvAは366動画で構成され、全体で14時間に及ぶ。またOxUvAの動画は追跡対象が、途中で画面から外れることが多く、再検出が必要な場合を多く含んでいる。<br>
<br>
__手法・新規性__<br>
OxUvAはYouTube BoundingBoxes（YTBB）から抽出している。YTBBにおける問題は、trackletが20秒以下に制限されていることである。しかし、同一クラスに対して複数のtrackletがラベル付けされていることがあり、それを利用することで長いtrackletを生成する。また初期フレームとして最適なものを選択し、動画ないで動きの少ない物体はデータセットから除いた。これらの作業をアノテータが行う。最終的に337動画、366個の軌跡からデータセットは構成されており、動画の平均長は2.36分と非常に長いものである。またこのような長時間動画に対する物体追跡の評価指標を提案し、ベンチマークテストを行った。<br>


@divend

@div[right]

![OxUvA](assets/img/Long-term_Tracking_in_the_Wild_A_Benchmark.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1803.09502.pdf)<br>
・[プロジェクト](https://oxuva.github.io/long-term-tracking-benchmark/)<br>

@divend