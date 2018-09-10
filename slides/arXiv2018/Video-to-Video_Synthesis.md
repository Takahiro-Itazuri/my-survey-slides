#### Video-to-Video Synthesis
###### Ting-Chun Wang, Ming-Yu Liu, Jun-Yan Zhu, Guilin Liu, Andrew Tao, Jan Kautz, Bryan Catanzaro

@div[left]

__概要__<br>
これまでImage-to-Image Synthesisのタスクが多く取り組まれてきたが、Video-to-Video Synthesisはまだあまり取り組まれていない。単純な方法としてImage-to-Image Synthesisをframe-by-frameに適用すると、temporal coherencyがなく、質の悪い結果となってしまう。本論文では、temporal coherencyのある高解像度なVideo-to-Video Synthesis手法（vid2vid）を提案した。またvid2vidは同じ入力に対して、分散を持った結果を出力することができる。<br>
<br>
__手法・新規性__<br>
入力動画`${\bf s}_1^T$`と出力動画`${\bf x}_1^T$`が与えられたとき、Sequential Generatorはマルコフ仮定により、以下のように記述できる。<br>
`\begin{align} p \left( \tilde{{\bf x}}_1^T | {\bf S}_1^T \right) = \prod_{t=1}^{T} p \left( \tilde{{\bf x}}_t | \tilde{{\bf x}}_{t-L}^{t-1}, {\bf s}_{t-L}^{t} \right) \end{align}`
ここで、条件付き確率`$p \left( \tilde{{\bf x}}_t | \tilde{{\bf x}}_{t-L}^{t-1}, {\bf s}_{t-L}^{t} \right)$`をモデル化したネットワーク`$F \left( \tilde{{\bf x}}_t = F \left( \tilde{{\bf x}}_{t-L}^{t-1}, {\bf s}_{t-L}^{t} \right) \right) $`を以下のように定義する。<br>
`\begin{align} F \left( \tilde{{\bf x}_{t-L}^{t-1}}, {\bf s}_{t-L}^{t} \right) = \left( {\bf 1} - \tilde{{\bf m}}_t \right) \odot \tilde{{\bf w}}_{t-1} (\tilde{{\bf x}}_{t-1}) + \tilde{{\bf m}}_t \odot \tilde{{\bf h}}_t \end{align}`
`$ \tilde{{\bf w}}_{t-1} $`は`$ \tilde{{\bf x}}_{t-1} $`から`$ \tilde{{\bf x}}_{t} $`へのオプティカルフローを意味し、`$ \tilde{{\bf w}}_{t-1} (\tilde{{\bf x}}_{t-1}) $`は`$ \tilde{{\bf x}}_{t-1} $`を`$ \tilde{{\bf w}}_{t-1} $`によってワーピングした結果を意味する。また`$ \tilde{{\bf h}}_t $`は生成画像であり、`$ \tilde{{\bf m}}_t $`は生成画像とワーピングして生成した画像をブレンドするマスクである。<br>
これに対して損失関数は以下を用いる。<br>
`\begin{align} \mathop{\rm min}\limits_{F} \left( \mathop{\rm max}_{D_I} \mathcal{L}_{I} \left( F, D_I \right) + \mathop{\rm max}_{D_V} \mathcal{L}_{V} \left( F, D_V \right) \right) + \lambda_W \mathcal{L}_{W} \left( F \right) \end{align}`

@divend

@div[right]

![](assets/img/ =full)<br>
<br>

__リンク__<br>
・[論文](https://tcwang0509.github.io/vid2vid/paper_vid2vid.pdf)<br>
・[プロジェクト](https://tcwang0509.github.io/vid2vid/))<br>
・[GitHub](https://github.com/NVIDIA/vid2vid)<br>

@divend