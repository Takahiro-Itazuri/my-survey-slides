#### Depth-Based 3D Hand Pose Estimate From Current Achievements to Future Goals
###### Shanxin Yuan, Guillermo Garcia-Hernando, Bjorn Stenger et al.

@div[left]

__概要__<br>
3D Hand Pose Estimationのサーベイ的論文。主に以下の2つの点に主眼を置いている。<br>
<ul>
  <li>デプス画像からの3D Hand Pose Estimationの現状を明らかにする。</li>
  <li>次に挑戦するべきである課題は何かを明らかにする。</li>
</ul><br>
Hands In the Million Challenge (HIM2017)のトップ10の最新手法に関して、3つのタスク（単一画像からの姿勢推定、3次元トラッキング、物体とインタラクション中の姿勢推定）において調査を行った。<br>
__手法・新規性__<br>
3D Hand Pose Estimationの現状において以下の7点の洞察を得た。<br>
<ul>
  <li>3DCNNを用いた3次元表現は入力のデプス情報の空間的構造を捉えることができ、良い精度を出した。</li>
  <li>検出ベースの手法は回帰ベースの手法より良い精度を出すが、回帰ベースの手法は明示的に空間的制約を加えることで良い精度を出すことができる。</li>
  <li>明示的な構造の制約や関節間の空間的関係性をモデリングすることで、関節の遮蔽なしとありの差を大きく狭めることができる。</li>
  <li>識別的手法はまだ見ぬ手の形に著しく脆弱であり、良い生成能力を持つ機構を組み合わせることで、今後良い方向に進みそう。</li>
  <li>70~120度の見え角では、非常に良い精度を出す一方で、極端な見え角ではエラーが大きくなる。</li>
  <li>トラッキングでは、現在の識別的手法においては検出を姿勢推定の2つサブタスクに分けて問題を解いている。</li>
  <li>単一画像からの姿勢推定は良い精度を出すが、物体とのインタラクションには一般化できていない。今後の方針として、より良いセグメンテーション方法をデザインするか、物体とのインタラクションを含む大規模データセットで学習することが挙げられる。</li>
</ul>

@divend

@div[right]

![](assets/img/Depth-Based_3D_Hand_Pose_Estimation.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Yuan_Depth-Based_3D_Hand_CVPR_2018_paper.pdf)<br>

@divend