#### Fourier Transform

@div[left]

__Continuous Fourier Transform__<br>
1D Continuous Fourier Transform<br>
`\begin{align} F(u) &= \int_{- \infty}^{\infty} f(x) e^{- 2 \pi j u x} dx \\ f(x) &= \int_{- \infty}^{\infty} F(u) e^{j 2 \pi u x} du \end{align}`

2D Continuous Fourier Transform<br>
`\begin{align} F(u, v) &= \int_{- \infty}^{\infty} f(x, y) e^{-2 \pi j (ux + vy)} dx dy \\ f(x, y) &= \int_{- \infty}^{\infty} F(u, v) e^{2 \pi j (ux + vy)} dx dy \end{align}`

@divend

@div[right]

__Discrete Fourier Transform__<br>
1D Discrete Fourier Transform<br>
`\begin{align} F[u] &= \sum_{x=0}^{N-1} f[x] e^{-2 \pi j \frac{ux}{N}} \\ f(x) &= \frac{1}{N} \sum_{u=0}^{N-1} F[u] e^{2 \pi j \frac{ux}{N}} \end{align}`

2D Discrete Fourier Transform<br>
`\begin{align} F[u, v] &= \sum_{x=0}^{M-1} \sum_{y=0}^{N-1} f[x, y] e^{-2 \pi j (\frac{ux}{M} + \frac{vy}{N})} \\ f[x, y] &= \sum_{u=0}^{M-1} \sum_{v=0}^{N-1} F[u, v] e^{2 \pi j (\frac{ux}{M} + \frac{vy}{N})} \end{align}`

@divend