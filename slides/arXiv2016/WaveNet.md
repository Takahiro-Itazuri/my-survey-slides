#### WaveNet: A Generative Model for Raw Audio
###### Aaron van den Oord, Sander Dieleman, Heiga Zen, Karen Simonyan, Oriol Vinyals, Alex Graves, Nal Kalchbrenner, Andrew Senior, Koray Kavukcuoglu

@div[left]

__概要__<br>
PixelRNNの構造を元に、直接生の音声波形を生成するネットワーク（WaveNet）を提案した。テキストを音声に変換するタスクに適用したところ、SoTAの精度で自然な音声の生成に成功した。<br>
<br>
__手法・新規性__<br>
音声サンプル`$x_i$`の確率分布は、それ以前の時間のサンプルの条件付き確率で与えられる自己回帰モデルとして与えられる。<br>
`\begin{align} p({\bf x}) = \prod_{t=1}^{T} p (x_t | x_1, \cdots , x_{t-1}) \end{align}`


@divend

@div[right]

![](assets/img/WaveNet.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1609.03499.pdf)<br>
・[Deepmind社ブログ](https://deepmind.com/blog/wavenet-generative-model-raw-audio/)<br>

@divend