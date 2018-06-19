#### SINT++: Robust Visual Tracking via Adversarial Positive Instance Generation
###### Xiao Wang, Chenglong Li, Bin Luo, Jin Tang

@div[left]

__概要__<br>
物体追跡タスクでは追跡対象の画像を１フレーム目においてのみ与えられるため、トレーニングデータの多様性が不足していることがDNNを適用する際の障壁となっている。そこで変形や遮蔽といった困難な環境下における正解サンプルを生成する手法（SINT++）を提案した。提案手法は他の物体追跡手法に取り入れることが可能であるため、これは今後の課題とする。<br>
<br>
__手法・新規性__<br>
VAEを用いて追跡対象の多様体を生成し、その多様体局面上を移動させることで正解サンプルを増やすネットワーク（PSGN）と識別器の認識性能にクリティカルな領域を探すように遮蔽領域を決定する強化学習ネットワーク（HPTN）を用いて、正解サンプルの多様性を増幅させる。追跡器はSINTを用いているため、与えられた追跡対象の画像に対するオフライン学習も、追跡中のオンライン学習も行わない。<br>

@divend

@div[right]

![](assets/img/SINT++.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_SINT_Robust_Visual_CVPR_2018_paper.pdf)<br>
・[プロジェクト](https://sites.google.com/view/cvpr2018sintplusplus)<br>

@divend