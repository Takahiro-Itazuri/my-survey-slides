#### Principal Component Analysis (PCA)

@div[left]

__概要__<br>
PCAは射影後の空間における分散を最大化させる次元圧縮手法である。<br>
<br>
__手法__<br>
`$N$`個のデータ集合`$\left\{ \boldsymbol{x}_n \right\}$`が与えられたとする。このとき、平均ベクトル`$ \overline{\boldsymbol{x}} $`と共分散行列`$ \boldsymbol{S} $`は以下のように求められる。<br>
`\begin{align} \overline{\boldsymbol{x}} &= \frac{1}{N} \sum_{n=1}^{N} \boldsymbol{x}_n \\ \boldsymbol{S} &= \frac{1}{N} \sum_{n=1}^{N} (\boldsymbol{x}_n - \overline{\boldsymbol{x}}) (\boldsymbol{x}_n - \overline{\boldsymbol{x}})^T \end{align}`
<u>1次元空間への射影</u>
射影した先の直線の方向ベクトルを`$\boldsymbol{u}_1$`とし、射影されたデータを`$\boldsymbol{x'}_n$`とする。ここで`$ \boldsymbol{u}_1 $`は方向ベクトルであるため、大きさは1である。このとき、射影先の空間における平均ベクトル`$\overline{\boldsymbol{x'}}$`と共分散行列`$\boldsymbol{S'}$`がは以下のように求められる。<br>
`\begin{align} \overline{\boldsymbol{x'}} &= \sum_{n=1}^{N} \boldsymbol{u}_{1}^{T} \boldsymbol{x}_n = \boldsymbol{u}_{1}^{T} \overline{\boldsymbol{x}} \\ \boldsymbol{S'} &= \frac{1}{N} \sum_{n=1}^{N} (\boldsymbol{x'} - \overline{\boldsymbol{x'}}) (\boldsymbol{x'} - \overline{\boldsymbol{x'}})^{T} = \boldsymbol{u}_{1}^{T} \boldsymbol{S} \boldsymbol{u}_{1}^{T} \end{align}`
`$ \boldsymbol{u}_1^T \boldsymbol{u}_1 = 1 $`の制約条件下で、射影後の分散を最大化する問題をラグランジュの未定乗数法で解く。<br>
`\begin{align} \boldsymbol{u}_1^{T} \boldsymbol{S} \boldsymbol{u}_1 + \lambda_1 (1 - \boldsymbol{u}_1^{T} \boldsymbol{u}_1) \end{align}`
以上より、以下の固有方程式が得られる。<br>
`\begin{align} \boldsymbol{S} \boldsymbol{u}_1 = \lambda_1 \boldsymbol{u}_1 \end{align}`したがって、第一主成分ベクトルは共分散行列の固有ベクトルであることがわかる。

@divend

@div[right]

@divend
