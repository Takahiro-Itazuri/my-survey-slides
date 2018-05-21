#### Fourier Transform

@div[left]

__Continuous Fourier Transform__<br>
1D Continuous Fourier Transform<br>
`\begin{align} F(\mu) &= \int_{- \infty}^{\infty} f(x) e^{- 2 \pi j \mu x} dx \\ f(x) &= \int_{- \infty}^{\infty} F(\mu) e^{j 2 \pi \mu x} d \mu \end{align}`<br>
<br>
2D Continuous Fourier Transform<br>
`\begin{align} F(\mu, \nu) &= \int_{- \infty}^{\infty} f(x, y) e^{-2 \pi j (\mu x + \nu y)} dx dy \\ f(x, y) &= \int_{- \infty}^{\infty} F(\mu, \nu) e^{2 \pi j (\mu x + \nu y)} d \mu du \end{align}`<br>
<br>

@divend

@div[right]

__Discrete Fourier Transform__<br>
1D Discrete Fourier Transform<br>
`\begin{align} F[\mu] &= \sum_{x=0}^{N-1} f[x] e^{-2 \pi j \frac{\mu x}{N}} \\ f(x) &= \frac{1}{N} \sum_{\mu=0}^{N-1} F[\mu] e^{2 \pi j \frac{\mu x}{N}} \end{align}`<br>
<br>
2D Discrete Fourier Transform<br>
`\begin{align} F[\mu, \nu] &= \sum_{x=0}^{M-1} \sum_{y=0}^{N-1} f[x, y] e^{-2 \pi j \left( \frac{\mu x}{M} + \frac{\nu y}{N} \right) } \\ f[x, y] &= \sum_{\mu=0}^{M-1} \sum_{\nu=0}^{N-1} F[\mu, \nu] e^{2 \pi j \left( \frac{\mu x}{M} + \frac{\nu y}{N} \right)} \end{align}`<br>
<br>

@divend