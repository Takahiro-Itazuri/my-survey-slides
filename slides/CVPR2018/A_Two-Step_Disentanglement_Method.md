#### A Two-Step Disentanglement Method
###### Naama Hadad, Lior Wolf, Moni Shahar

@div[left]

__概要__<br>
Disentanglementタスクを敵対的ネットワークの構造を利用して行った論文。Disentanglementとは要因を分解するようなタスクであり、手書き文字であれば何の文字が書かれているかという情報と書かれている文字のスタイルを分離するようなタスクである。提案手法は最初に正解ラベルを与えられるようなタスクを学習させた後、それ以外の要素を抽出するようにもう一つのネットワークを学習させることでこれを実現した。実験では、分離した2つの要因を補間したり、掛け合わせたりする検証と2つの要因に相関が無くなっているかを確認するための検索タスクを行った。<br>
<br>
__手法・新規性__<br>
まず初めにネットワークSを正解ラベルの存在するクラス分類のタスクで学習させる。次にSとは異なるネットワークZを学習するのだが、SのエンコーダとZのエンコーダから得られた特徴量からReconstructionするように学習するブランチと、Zのエンコーダから得られた特徴量からできるだけクラス分類の精度が下がるように学習するブランチで学習する。特にクラス分類の精度を下げるように学習する方は、クラス分類に必要な情報をできるだけ忘れるようになっており、Disentanglementのタスクに効いている。<br>

@divend

@div[right]

![](assets/img/A_Two-Step_Disentanglement_Method.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Hadad_A_Two-Step_Disentanglement_CVPR_2018_paper.pdf)<br>
・[GitHub](https://github.com/naamahadad/A-Two-Step-Disentanglement-Method)<br>

@divend