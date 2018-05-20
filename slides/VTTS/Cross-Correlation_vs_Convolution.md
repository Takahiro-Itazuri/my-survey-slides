#### Cross-Correlation vs Convolution

@div[left]

# Cross-Correlation
`\begin{align} G &= h \otimes F \\ G[i, j] &= \sum_{u=-k}^{k} \sum_{v=-k}^{k} h[u, v] F[i + u, j + v] \end{align}`


@divend

@div[right]

# Convolution
`\begin{align} G &= h \ast F \\ G[i, j] &= \sum_{u=-k}^{k} \sum_{v=-k}^{k} h[u, v] F[i - u, j - v] \end{align}`

@divend