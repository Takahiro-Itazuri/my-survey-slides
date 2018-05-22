#### Principal Component Analysis (PCA)

@div[left]

__概要__<br>
PCAは射影後の空間における分散を最大化させる次元圧縮手法である。<br>
<br>
__手法__<br>
`$N$`個のデータ集合`$\left\{ \boldsymbol{x}_n \right\}$`が与えられたとする。このとき、平均ベクトル`$ \overline{\boldsymbol{x}} $`と共分散行列`$ \boldsymbol{S} $`は以下のように求められる。<br>
`\begin{align} \overline{\boldsymbol{x}} &= \frac{1}{N} \sum_{n=1}^{N} \boldsymbol{x}_n \\ \boldsymbol{S} &= \frac{1}{N} \sum_{n=1}^{N} (\boldsymbol{x}_n - \overline{\boldsymbol{x}}) (\boldsymbol{x}_n - \overline{\boldsymbol{x}})^T \end{align}`
<u>1次元空間への射影</u><br>
射影した先の直線の方向ベクトルを`$\boldsymbol{u}_1$`とし、射影されたデータを`$\boldsymbol{x'}_n$`とする。ここで`$ \boldsymbol{u}_1 $`は方向ベクトルであるため、大きさは1である。このとき、射影先の空間における平均ベクトル`$\overline{\boldsymbol{x'}}$`と共分散行列`$\boldsymbol{S'}$`がは以下のように求められる。<br>
`\begin{align} \overline{\boldsymbol{x'}} &= \sum_{n=1}^{N} \boldsymbol{u}_{1}^{T} \boldsymbol{x}_n = \boldsymbol{u}_{1}^{T} \overline{\boldsymbol{x}} \\ \boldsymbol{S'} &= \frac{1}{N} \sum_{n=1}^{N} (\boldsymbol{x'} - \overline{\boldsymbol{x'}}) (\boldsymbol{x'} - \overline{\boldsymbol{x'}})^{T} = \boldsymbol{u}_{1}^{T} \boldsymbol{S} \boldsymbol{u}_{1} \end{align}`
`$ \boldsymbol{u}_1^T \boldsymbol{u}_1 = 1 $`の制約条件下で、射影後の分散を最大化する問題をラグランジュの未定乗数法で解く。<br>
`\begin{align} \boldsymbol{u}_1^{T} \boldsymbol{S} \boldsymbol{u}_1 + \lambda_1 (1 - \boldsymbol{u}_1^{T} \boldsymbol{u}_1) \end{align}`
以上より、以下の固有方程式が得られる。<br>
`\begin{align} \boldsymbol{S} \boldsymbol{u}_1 = \lambda_1 \boldsymbol{u}_1 \end{align}`したがって、第一主成分ベクトルは共分散行列の固有ベクトルであることがわかる。また上式に左から`$ \boldsymbol{u}_1^{T} $`をかけると、以下のようになる。

@divend

@div[right]

`\begin{align} \boldsymbol{u}_1^{T} \boldsymbol{S} \boldsymbol{u}_1 = \lambda_1 \boldsymbol{u}_1^{T} \boldsymbol{u}_1 = \lambda_1 \end{align}`
以上より分散と固有値が等しいことがわかる。したがって、最大固有値`$\lambda_1$`を選んだとき、分散は最大となり、それ対応する固有ベクトルが第一主成分ベクトルになる。<br>
<u>多次元空間への射影</u><br>
すでに得られた主成分ベクトルと直交するという制約条件下で、射影後の分散を最大化する問題を解くことで、逐次的に主成分を求めることができる。したがって、`$M$`次元空間への射影を考える場合、分散行列の固有値を大きい順に並べた`$\lambda_1, \lambda_2, \cdots, \lambda_M$`に対応する固有ベクトル`$ \boldsymbol{u}_1, \boldsymbol{u}_2, \cdots, \boldsymbol{u}_M $`を求めることにより`$M$`個の主成分を得ることができる。<br>
<u>固有値分解</u><br>
射影前と射影後の次元数`$d$`を同じとした場合、以下のことが導き出される。<br>
`$ \begin{align} \boldsymbol{x}_n &= \sum_{i=1}^{d} a_i^{(n)} \boldsymbol{u}_i \\ \boldsymbol{S'} &= \frac{1}{N} \sum_{n=1}^{N} ( \sum_{i=1}^{d} (a_i^{(n) - \overline{a}_i}) \boldsymbol{u}_i ) ( \sum_{i=1}^{d} (a_i^{(n) - \overline{a}_i}) \boldsymbol{u}_i )^{T} \\ &= \sum_{n=1}^{N} \sum_{i=1}^{d} \boldsymbol{u}_i  (a_i^{(n)} - \overline{a}_i)^2 \boldsymbol{u}_i^T \\ &= \begin{pmatrix} \boldsymbol{u}_1 & \boldsymbol{u}_2 & \cdots & \boldsymbol{u}_d \end{pmatrix} \begin{pmatrix} \lambda_1^2 & 0 & \cdots & 0 \\ 0 & \lambda^2 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & \lambda_n^2 \end{pmatrix} \begin{pmatrix} \boldsymbol{u}_1^T \\ \boldsymbol{u}_2^T \\ \vdots \\ \boldsymbol{u}_d^T \end{pmatrix} \end{align} $`
以上より固有ベクトルを並べた行列と固有値を体格成分に持つ行列に分解することが可能である。この行列分解の方法を固有値分解という。

@divend

