#### Video-to-Video Synthesis
###### Ting-Chun Wang, Ming-Yu Liu, Jun-Yan Zhu, Guilin Liu, Andrew Tao, Jan Kautz, Bryan Catanzaro

@div[left]

__概要__<br>
これまでImage-to-Image Synthesisのタスクが多く取り組まれてきたが、Video-to-Video Synthesisはまだあまり取り組まれていない。単純な方法としてImage-to-Image Synthesisをframe-by-frameに適用すると、temporal coherencyがなく、質の悪い結果となってしまう。本論文では、temporal coherencyのある高解像度なVideo-to-Video Synthesis手法（vid2vid）を提案した。またvid2vidは同じ入力に対して、分散を持った結果を出力することができる。<br>
<br>
__手法・新規性__<br>
入力動画`${\bf s}_1^T$`と出力動画`${\bf x}_1^T$`が与えられたとき、Sequential Generatorはマルコフ仮定により、以下のように記述できる。<br>
`\begin{align} p(\tilde{{\bf x}}_1^T | {\bf S}_1^T) = \prod_{t=1}^{T} p(\tilde{{\bf x}}_t | \tilde{{\bf x}}_{t-L}^{t-1}, {\bf s}_{t-L}^{t}) \end{align}`
ここで、条件付き確率`$p(\tilde{{\bf x}}_t | \tilde{{\bf x}}_{t-L}^{t-1}, {\bf s}_{t-L}^{t})$`をモデル化したネットワークを`$ \tilde{{\bf x}}_t = F( \tilde{{\bf x}}_{t-L}^{t-1}, {\bf s}_{t-L}^{t} ) $`とする。

@divend

@div[right]

![](assets/img/ =full)<br>
<br>

__リンク__<br>
・[論文](https://tcwang0509.github.io/vid2vid/paper_vid2vid.pdf)<br>
・[プロジェクト](https://tcwang0509.github.io/vid2vid/))<br>
・[GitHub](https://github.com/NVIDIA/vid2vid)<br>

@divend