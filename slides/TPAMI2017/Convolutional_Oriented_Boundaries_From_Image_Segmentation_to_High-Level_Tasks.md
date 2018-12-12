#### Convolutional Oriented Boundaries
###### Kevis-Kokitsi Maninis, Jordi Pont-Tuset, Pablo Arbelaez, Luc Van Gool

@div[left]

__概要__<br>
マルチスケールな方向情報を持つ輪郭を出力するCNN（COB：Convolutional Oriented Boundaries）を提案した。COBは１回のCNNの順伝搬でマルチスケールな輪郭検出が可能であるため、0.8秒/フレームと高速に実行可能である。また輪郭の強度（確率）マップを階層的な境界マップに変換する手法であるUltrametric Contour Map（UCM）は精度は良いが低速であるため、これの高速化を行った。COBを様々な高レベルなタスクで精度評価を行い、非常に良い精度を出した。<br>
<br>
__手法・新規性__<br>
CNNがマルチスケールな特徴量抽出器であることから、COBはCNNの中間層の特徴量を利用して、マルチスケールな境界とその向きを推定する。CNNを5ステージに分け、入力層に近い方から4ステージを使って細かいスケールの出力を行い、出力層に近い方から4ステージを使って粗い出力を行う。<br>


@divend

@div[right]

![](path/to/img =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1608.02755.pdf)<br>
・[プロジェクト](http://www.vision.ee.ethz.ch/~cvlsegmentation/cob/)<br>
・[GitHub](https://github.com/kmaninis/COB)<br>

@divend