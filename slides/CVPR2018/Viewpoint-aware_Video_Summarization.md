#### Viewpoint-aware Video Summarization
###### Atsushi Kanehira, Luc Van Gool, Yoshitaka Ushiku, Tatsuya Harada

@div[left]

__概要__<br>
そもそも要約動画として１つの最適解が存在するわけではないことを主張し、それぞれの視点に合わせて要約動画を行った研究。本研究では、動画間の類似度に着目し、フィッシャー判別から着想を得て、inner-summary variance、inner-group variance、between-group varianceに関して最適化を行うことで要約映像を生成した。また評価のためのデータセットを構築し、質的評価・量的評価を行った。<br>
<br>
__手法・新規性__<br>
要約動画として満たすべき条件として(1)要約動画内で分散があること、(2)同一グループ内の動画を代表することができること、(3)他のグループの動画と識別できることを挙げている。これらに対応する要素がフィッシャー判別から着想を得たinner-summary variance、inner-group variance、between-group varainceである。これらをC3Dで抽出した特徴量に対して計算し、最適化することで解を得る。<br>

@divend

@div[right]

![](assets/img/Viewpoint-aware_Video_Summarization.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Kanehira_Viewpoint-Aware_Video_Summarization_CVPR_2018_paper.pdf)<br>

@divend