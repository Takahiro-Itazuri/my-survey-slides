#### U-Net: Convolutional Networks for Biomedical Image Segmentation
###### Olaf Ronneberger, Phillip Fischer, Thomas Brox

@div[left]

__概要__<br>
本論文では、セグメンテーションタスクで提案されたFully Convolutional Network（FCN）を改良し、非常に少ない学習データ数かつより正確な結果を得ることが可能なネットワーク（U-Net）を提案した。提案手法はISBI challengeで非常に良い精度を出した。<br>
<br>
__手法・新規性__<br>
U-Netは左右対称な構造となっており、スケールを小さくしながら抽象的な情報を抽出するcontracting pathと、contracting pathで得られた抽象的な情報を引継ぎながらスケールを大きくして詳細な位置情報を得るexpandingから構成される。また様々な変形を加えながら学習を行うことで、データ拡張を行っている。<br>


@divend

@div[right]

![U-Net](assets/img/U-Net_Convolutional_Networks_for_Biomedical_Image_Segmentation.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/abs/1505.04597)<br>
・[プロジェクト](https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/)<br>
・[デモ](https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/)

@divend