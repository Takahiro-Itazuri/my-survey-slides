#### Deep Back-Projection Networks for Super-Resolution
###### Muhammad Haris, Gregory Shakhnarovich, Norimichi Ukita

@div[left]

__概要__<br>
高解像のタスクに対して、アップサンプリングとダウンサンプリングを交互に繰り返す構造を持つDeep Back-Projection Networks（DBPN）を提案した。従来のネットワークはアップサンプリングを行う方向（feed-forward connection）しか考えておらず、それをダウンサンプリングする方向（feedback connection）を考えていなかったため、大きなスケール変化に対応できていなかった。本論文は1991年のCVGIPで発表された論文に発想を得て、アップサンプリングとダウンサンプリングを交互に繰り返す構造を取り、SoTAを達成した。<br>
<br>
__手法・新規性__<br>
DBPNはup-projection unitとdown-projection unitからなる。up-projection unitの手順は、1) 一つ前の状態の低解像度画像（LR）をスケールアップし高解像度画像（HR）を生成し、2) 次にHRをスケールダウンさせたLRを得る、3) スケールアップとスケールダウンを経て得られたLRと入力のLRの差分を計算した後、4) その差分を元に再度スケールアップをすることでHRを得る、5) 最後にこのHRと最初にスケールアップで得られたHRを足し合わせたものを最終的なHRの出力とする。down-projection unitはこの反対の操作を行う。
<br>


@divend

@div[right]

![](assets/img/DBPN.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Haris_Deep_Back-Projection_Networks_CVPR_2018_paper.pdf)<br>
・[Supplemental Material](http://openaccess.thecvf.com/content_cvpr_2018/Supplemental/3606-supp.pdf)<br>

@divend