#### Singular Value Decomposition (SVD)

@div[left]

__概要__<br>
1つ前のスライドの最後に正方行列の行列分解手法である固有値分解を紹介した。特異値分解は分解の対象となる行列が正方行列でない場合の行列分解手法であり、固有値分解を一般化したものである。<br>
<br>
__手法__<br>
分解対象を`$M \times N$`行列`$\boldsymbol{X}$`とする。この行列のランクが`$r$`だった場合、以下のように分解することができる。<br>
`\begin{align} \boldsymbol{X} = \boldsymbol{U} \boldsymbol{\Sigma} \boldsymbol{V}^T \end{align}`
`$ \boldsymbol{U} $`は`$M \times M$`のユニタリ行列、`$ \boldsymbol{V} $`は`$N \times N$`のユニタリ行列でり、`$\boldsymbol{\Sigma}$`は`$ N \times M $`で対角成分が`$ \sigma_1, \sigma_2, \cdots, \sigma_r $`で、それ以外が0となる行列である。これに対して以下の式を満たす。<br>
`\begin{align} \boldsymbol{X} \boldsymbol{X}^T = \boldsymbol{U} \boldsymbol{\Sigma} \boldsymbol{V}^T \boldsymbol{V} \boldsymbol{\Sigma} \boldsymbol{U}^T = \boldsymbol{U} \boldsymbol{\Sigma} \boldsymbol{\Sigma}^T \boldsymbol{U}^T = \boldsymbol{U} \boldsymbol{\Lambda} \boldsymbol{U}^T \end{align}`
`$\boldsymbol{U}$`はユニタリ行列であり、`$\boldsymbol{\Lambda}$`は対角行列であることから、特異値`$\sigma$`は`$\boldsymbol{X} \boldsymbol{X}^T $`の固有値の平方根となる。<br>
<br>
__幾何学的解釈__<br>
行列`$\boldsymbol{U}, \boldsymbol{V}$`はユニタリ行列であるから、行列`$\boldsymbol{U}$`の列ベクトルは体`$K^M$`上（`$M$`次元空間と考えればよい）の正規直交基底を成し、行列`$\boldsymbol{V}$`の列ベクトルは体`$K^N$`の正規直交基底を成す。以上から写像`$\boldsymbol{X}: K^N \to K^M$`がこれらの正規直交基底を用いて簡単な形で表されていることとなる。また、これらの正規直交基底はそれぞれ対応しており、整数倍することで表される。

@divend

@div[right]

@divend
