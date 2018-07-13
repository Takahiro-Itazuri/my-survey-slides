#### Online Object Tracking: A Benchmark
###### Yi Wu, Jongwoo Lim, Ming-Hsuan Yang

@div[left]

__概要__<br>
Video Survaillance用のデータセットは背景が固定であり、概ね対象物体の大きさが小さく変化しないものである。本論文では、様々な状況下の映像を含むデータベースと、最新の手法を比較するため統一的な入出力と評価が行えるライブラリを作成した。<br>
<br>
__手法・新規性__<br>
テストデータは50個用意し、それぞれに11個のアトリビューションを付与した。ライブラリとして最新の29個の物体追跡アルゴリズムを用意し、それらの頑健性と特徴を評価した。評価尺度として、中心位置のずれの平均であるPrecision Plotと、Bounding Boxの重なりが閾値以上だった場合を成功とした場合の成功率であるSuccess Plotを用いた。頑健さ評価として、最初の１フレーム目を正解として与えるOne-Pass Evaluation（OPE）に加え、正解として与えるフレームに時間的な変動を与えたTemporal Robustness Evaluation（TRE）と空間的な変動を与えたSpatial Robustness Evaluation（SRE）を用いた。<br>


@divend

@div[right]

![](path/to/img =full)<br>
<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_cvpr_2013/papers/Wu_Online_Object_Tracking_2013_CVPR_paper.pdf)<br>
・[プロジェクト](http://cvlab.hanyang.ac.kr/tracker_benchmark/index.html)<br>

@divend
