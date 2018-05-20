#### Cross-Correlation vs Convolution

@div[left]

__Cross-Correlation__<br>
`\begin{align} h &= f \otimes g \\ h[i, j] &= \sum_{u=-k}^{k} \sum_{v=-k}^{k} f[u, v] g[i + u, j + v] \end{align}`


@divend

@div[right]

__Convolution__<br>
`\begin{align} h &= f \ast g \\ h[i, j] &= \sum_{u=-k}^{k} \sum_{v=-k}^{k} f[u, v] g[i - u, j - v] \end{align}`

@divend