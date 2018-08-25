#### Cut, Paste and Learn: Surprisingly Easy Synthesis for Instance Detection
###### Debidatta Dwibedi, Ishan Misra, Martial Hebert

@div[left]

__概要__<br>
Object Detection用のモデルをInstance Detectionに適用する際のデータ不足の問題を解決するため、インスタンスをカットし、任意の背景にペーストする方法でデータ量を増やす論文。単純にカット・ペーストした場合に発生するアーティファクトを除去するための方法を提案した。既存のデータ合成を行う手法より21%も良い精度を出し、真のデータの10%の量から同様の精度を出すことが可能になった。<br>
<br>
__手法・新規性__<br>
手順としては、まずインスタンス画像と背景画像を収集し、次にインスタンス画像からforegrand maskを推定する。抽出したインスタンスをランダムに選択した背景にペーストする。単純にペーストしただけの場合、見た目的にはわずかな違いにも関わらず、境界部分のアーティファクトによって精度を落としてしまう。これはCNN検出器が局所特徴量に強く依存しているためである。そこで合成する際にGaussian BlurringやPoisson Smoothingを行った場合、インスタンスによっては精度の向上を確認することができたが、明らかな向上ではなかった。そこで、同じシーン、同じ物体の位置で、複数の合成方法を試した画像すべてを学習画像に加えると、そのような境界部分の影響を無視するように学習することが可能になり、非常に良い精度向上が見られた。<br>

@divend

@div[right]

![](assets/img/Cut_Paste_and_Learn_Surprisingly_Easy_Synthesis_for_Instance_Detection.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_ICCV_2017/papers/Dwibedi_Cut_Paste_and_ICCV_2017_paper.pdf)<br>

@divend