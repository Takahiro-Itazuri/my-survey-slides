#### High-Resolution Image Synthesis and Semantc Manipulation with Conditional GANs
###### Ting-Chun Wang, Ming-Yu Ling, Jun-Yan Zhu, Andrew Tao, Jan Kautz, Bryan Catanzaro

@div[left]

__概要__<br>
通常のCG技術を用いて、photo-realisticな画像をレンダリングするには、あらゆる状況を明示的にシミュレーションする必要があり、非常に多くの時間を要する。一方で、従来のGANを用いた画像合成手法では、高解像度でphoto-realisticな画像を合成することは困難であった。本論文は、pix2pixを改良して、セマンティックラベルのついた画像から高解像でphoto-realisticな画像合成と編集が可能な手法（pix2pixHD）を提案した。pix2pixHDは2048`$\times$`1024の高品質な画像を出力することが可能であり、編集として入力のセマンティックラベルを編集する方法と、同じセマンティックラベルの入力に対して異なる出力を得る方法を提案した。<br>
<br>
__手法・新規性__<br>
pix2pixHDはCoarse-to-Fine GeneratorとMulti-scale Discriminatorで構成される。Coarse-to-Fine GeneratorはGlobal Generator Network `$G_1$`とLocal Enhancer Network `$G_2$`で構成される。まず初めに1024`$\times$`512の出力を出す`$G_1$`を学習し、次のその外側に解像度を上げる`$G_2$`を加えて再学習する。同様に外側に加えていくことで解像度を上げていくおとが可能である。またMulti-scale Discriminatorは、ダウンサンプルして得た異なる3つのスケールに対して同じネットワークを適用する。このような構造を持たないと、生成画像中に類似したパターンが繰り返し生成されてしまう。また従来のGANのAdversarial Lossに中間表現を合わせるFeature Matching Lossを加えることで、より安定した学習が行える（VAE-GANに類似）。またInstance Boundary Mapも入力に加えることで、同じカテゴリだが異なるインスタンスの物体の境界部分がより鮮明に合成される。<br>


@divend

@div[right]

![pix2pixHD](assets/img/High-Resolution_Image_Synthesis_and_Semantic_Manipulation_with_Conditional_GANs.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_High-Resolution_Image_Synthesis_CVPR_2018_paper.pdf)<br>
・[プロジェクト](https://tcwang0509.github.io/pix2pixHD/)<br>

@divend