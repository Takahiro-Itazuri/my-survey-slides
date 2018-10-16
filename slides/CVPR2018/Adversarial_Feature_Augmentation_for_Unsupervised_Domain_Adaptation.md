#### Adversarial Feature Augmentation for Unsupervised Domain Adaptation
###### Riccardo Volpi, Pietro Morerio, Silvio Savarese, Vittorio Murino

@div[left]

__概要__<br>
GANを用いたUnsupervised Domain Adaptationにおいて、特徴量空間上でデータ拡張（Feature Augmentation）を行い、それに基づいてドメインに不変な（Feature Domain-Invariance）共通の特徴量抽出器を学習する手法を提案した。Domain-Invaraint Feature Extractorを作ること自体は既存と同様であるが、Feature Augmentationをした点とDomain-Invariant Feature Extractorをソースとターゲットの両方において最後に学習する点（ソースで事前に学習したことを忘却しない効果がある）が異なる。提案手法はいくつかのベンチマークにおいてSoTAを達成した。<br>
<br>
__手法・新規性__<br>
まずソースドメインに対して通常のクラス識別を学習させ、特徴量抽出器`$E_S$`と識別器`$C$`を得る。次に、特徴量抽出器`$E_S$`から得られる特徴量に対して、ノイズから特徴量を生成する生成器`$S$`をGANで学習する。最後に、特徴量抽出器`$E_S$`の重みで初期化された特徴量抽出器`$E_I$`を使ってソースとターゲットの両方から生成された特徴量と、生成器`$S$`がノイズから生成した特徴量に対して、GANを学習させることで、ソースとターゲットの両方に対する特徴量抽出器`$E_I$`を得ることができる。推論時には最後に学習した特徴量抽出器`$E_I$`と最初に学習した識別器`$C$`を用いる。<br>

@divend

@div[right]

![](assets/img/Adversarial_Feature_Augmentation_for_Unsupervised_Domain_Adaptation.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1711.08561.pdf)<br>
・[GitHub](https://github.com/ricvolpi/adversarial-feature-augmentation)<br>

@divend