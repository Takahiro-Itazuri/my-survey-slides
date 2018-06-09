#### A Twofold Siamese Network for Real-Time Object Tracking
###### Anfeng He, Chong Luo, Xinmei Tian, Wenjun Zeng

@div[left]

__概要__<br>
物体追跡手法の１つであるSiamFCは効率的なオフライン学習を行うことで、非常に高い識別性能を持つが、追跡対象の見た目の変化に弱かった。そこで、見た目特徴量とセマンティックな情報を別々に抽出する２つのSiamese Networkを利用することで、追跡対象の見た目変化にも強い物体追跡手法を提案した。セマンティックな情報を抽出するネットワークは画像分類タスクで学習させることで、見た目の変化に頑健な特徴量を抽出することが可能となる。<br>
<br>
__手法・新規性__<br>
推論フェーズでは、それぞれのネットワークで別々に追跡対象画像と探索画像の類似度を計算し、それを統合する。セマンティックな情報を抽出するネットワークは、見た目変化には頑健ではあるが、識別性能は不十分であるため、与えれた追跡対象に反応するチャンネルの重要度を増やすChennel Attentionを追加する。これによって追跡対象に適応する最低限の機能を追加している。<br>

@divend

@div[right]

[SA-Siam](assets/img/SA-Siam.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/He_A_Twofold_Siamese_CVPR_2018_paper.pdf)<br>

@divend