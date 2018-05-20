#### Cross-Correlation vs Convolution

@div[left]

__Cross-Correlation__<br>
__1D Continuous Cross-Correlation__

__2D Continuous Cross-Correlation__

__1D Discrete Cross-Correlation__

__2D Discrete Cross-Correlation__
`\begin{align} h &= f \otimes g \\ h[u, v] &= \sum_{x=0}^{M} \sum_{y=0}^{N} f[x, y] g[i + u, j + v] \end{align}`

@divend

@div[right]

__Convolution__<br>
__1D Continuous Convolution__

__2D Continuous Convolution__

__1D Discrete Convolution__

__2D Discrete Convolution__
`\begin{align} h &= f \ast g \\ h[i, j] &= \sum_{u=-k}^{k} \sum_{v=-k}^{k} f[u, v] g[i - u, j - v] \end{align}`

@divend