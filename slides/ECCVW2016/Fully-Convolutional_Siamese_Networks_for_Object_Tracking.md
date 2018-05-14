#### Fully-Convolutional Siamese Networks for Object Tracking
###### Luca Bertinetto, Jack Valmadre, Joao F. Henriques, Andrea Vedaldi, Philip H. S. Toor

@div[left]

__概要__<br>
対象動画から得られる学習データのみから、陽に見た目情報のモデルを学習していた従来手法は表現力に制限がある。一方で、深層学習ベースの手法は、追跡対象が事前に与えられないことから、オンラインでSGDを行う必要があり、十分な速度が出ないという問題がある。物体検出用データセット（Object detection from video (ILSVRC2015)）で学習させたEnd-to-EndのFully-Convolution Siamese Network（SiameseFC）を提案し、リアルタイム以上の速度とSOTAを実現した。<br>

__手法・新規性__<br>
見本画像$z$と候補画像$x$を比較する関数$f(z,x)$は両方の画像を特徴量に変換する関数$\phi$と得られた特徴量を統合する関数$g$によって$f(z,x)=g(\phi(z), \phi(x))$となる。<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1606.09549.pdf)<br>
・[プロジェクト](https://www.robots.ox.ac.uk/~luca/siamese-fc.html)<br>
・[GitHub](https://github.com/bertinetto/cfnet)<br>
・[発表動画](https://youtu.be/jZoUalMMZ_0)<br>
・[スライド](https://pdfs.semanticscholar.org/presentation/4c91/827cceb97183c4d48ca09e1c7587577c8d54.pdf)<br>

@divend


@div[right]

<!-- ![](path/to/img =full) -->

@divend