#### What Makes Video a Video: ANalyzing Temporal INformation in Video Understanding Models and Datasets
###### De-An Huang, Vignesh Ramanathan, Dhruv Mahajan

@div[left]

__概要__<br>
動き表現が行動認識の精度にどのように影響するかを調査した論文。動画から1フレームをサンプリングし、それを複数フレームに複製して入力すると、精度が25%落ちるが、これは一概に動画中の動き情報の欠如によるものであると結論付けるのは早計である。このようなサブサンプリングによって、著しく時間方向の分散が変わった点と行動認識にとって重要な情報が欠けてしまった可能性がある点が発生していると考えられる。そこでこれらのアーティファクトを取り除いて、動き表現の有無による結果の違いを評価するため、Class-Agnostic Temporal GeneratorとMotion-Invariant Frame Selectorを提案し、行動認識の精度のギャップを25%から6%まで近づけることに成功し、この6%こそが動き情報によるものであると結論付けた。<br>
<br>
__手法・新規性__<br>
Class-Agnostic Temporal Generatorは、元動画から得られる特徴量の活性化を再現するような動画を、サブサンプリングされたフレームからクラス情報を用いずに生成するネットワークである。つまり、Class-Agnostic Temporal Generatorはサブサンプリングされたフレームから想定される潜在的な動き情報を生成することを目的としている。Motion-Invariant Frame Selectorは、なるべく潜在的な動き情報を含んだフレームを選択する方法である。これらにより、行動認識に動き情報を必要としないクラスと必要とするクラスが存在することがわかった。<br>


@divend

@div[right]

![](assets/img/What_Makes_Video_a_Video_Analyzing_Temporal_Information_in_Video_Understanding_Models_and_Datasets.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Huang_What_Makes_a_CVPR_2018_paper.pdf)<br>

@divend