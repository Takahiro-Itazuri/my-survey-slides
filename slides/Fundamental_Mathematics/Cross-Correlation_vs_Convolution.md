#### Cross-Correlation vs Convolution

@div[left]

__Cross-Correlation__<br>
`\begin{align} h = f \star g \end{align} `<br>
<br>
1D Continuous Cross-Correlation<br>
`\begin{align} h(u) = \int_{- \infty}^{\infty} f(x) g(u + x) dx \end{align}`<br>
<br>
2D Continuous Cross-Correlation<br>
`\begin{align} h(u, v) = \int_{- \infty}^{\infty} \int_{- \infty}^{\infty} f(x, y) g(u + x, v + y) dx dy \end{align}`<br>
<br>
1D Discrete Cross-Correlation<br>
`\begin{align} h[u] = \sum_{x=0}^{N-1} f[x] g[u + x] \end{align}`<br>
<br>
2D Discrete Cross-Correlation<br>
`\begin{align} h[u, v] = \sum_{x=0}^{M-1} \sum_{y=0}^{N-1} f[x, y] g[u + x, v + y] \end{align}`<br>
<br>

@divend

@div[right]

__Convolution__<br>
`\begin{align} h = f \ast g \end{align}`<br>
<br>
1D Continuous Convolution<br>
`\begin{align} h(u) = \int_{- \infty}^{\infty} f^{\ast}(x) g(u - x) dx \end{align}`<br>
<br>
2D Continuous Convolution<br>
`\begin{align} h(u, v) = \int_{- \infty}^{\infty} \int_{- \infty}^{\infty} f^{\ast}(x, y) g(u - x, v - y) dx dy \end{align}`<br>
<br>
1D Discrete Convolution<br>
`\begin{align} h[u] = \sum_{x=0}^{N-1} f^{\ast}[x] g[u - x] \end{align}`<br
<br>
2D Discrete Convolution<br>
`\begin{align} h[u, v] = \sum_{x=0}^{M-1} \sum_{y=0}^{N-1} f^{\ast}[x, y] g[u - x, v - y] \end{align}`<br>
<br>
@divend