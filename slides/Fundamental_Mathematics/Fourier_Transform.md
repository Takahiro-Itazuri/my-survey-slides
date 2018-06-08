#### Fourier Transform

@div[left]

__Continuous Fourier Transform__<br>
1D Continuous Fourier Transform<br>
`\begin{align} F(\mu) &= \int_{- \infty}^{\infty} f(x) e^{- 2 \pi j \mu x} dx \\ f(x) &= \frac{1}{2 \pi} \int_{- \infty}^{\infty} F(\mu) e^{2 \pi j \mu x} d \mu \\ F(\omega) &= \int_{- \infty}^{\infty} f(x) e^{- j \omega x} dx \\ f(x) &= \frac{1}{2 \pi} \int_{- \infty}^{\infty} F(\omega) e^{j \omega x} d \omega \end{align}`<br>
<br>
2D Continuous Fourier Transform<br>
`\begin{align} F(\mu, \nu) &= \int_{- \infty}^{\infty} f(x, y) e^{-2 \pi j (\mu x + \nu y)} dx dy \\ f(x, y) &= \frac{1}{(2 \pi)^2} \int_{- \infty}^{\infty} F(\mu, \nu) e^{2 \pi j (\mu x + \nu y)} d \mu du \\  F(\omega_x, \omega_y) &= \int_{- \infty}^{\infty} f(x, y) e^{-j (\omega_x x + \omega_y y)} dx dy \\ f(x, y) &= \frac{1}{(2 \pi)^2} \int_{- \infty}^{\infty} F(\omega_x, \omega_y) e^{j (\omega_x x + \omega_y y)} d \omega_x d \omega_y \end{align}`<br>
<br>

@divend

@div[right]

__Discrete Fourier Transform__<br>
1D Discrete Fourier Transform<br>
`\begin{align} F[\mu] &= \sum_{x=0}^{N-1} f[x] e^{-2 \pi j \frac{\mu x}{N}} \\ f(x) &= \frac{1}{N} \sum_{\mu=0}^{N-1} F[\mu] e^{2 \pi j \frac{\mu x}{N}} \\ F[\omega] &= \sum_{x=0}^{N-1} f[x] e^{-j \omega x} \\ f(x) &= \frac{1}{N} \sum_{\omega=0}^{N-1} F[\omega] e^{j \omega x} \end{align}`<br>
<br>
2D Discrete Fourier Transform<br>
`\begin{align} F[\mu, \nu] &= \sum_{x=0}^{M-1} \sum_{y=0}^{N-1} f[x, y] e^{-2 \pi j \left( \frac{\mu x}{M} + \frac{\nu y}{N} \right) } \\ f[x, y] &= \frac{1}{MN} \sum_{\mu=0}^{M-1} \sum_{\nu=0}^{N-1} F[\mu, \nu] e^{2 \pi j \left( \frac{\mu x}{M} + \frac{\nu y}{N} \right)} \\ F[\omega_x, \omega_y] &= \sum_{x=0}^{M-1} \sum_{y=0}^{N-1} f[x, y] e^{-j \left( \omega x + \omega_y y \right) } \\ f[x, y] &= \frac{1}{MN} \sum_{\omega_x =0}^{M-1} \sum_{\omega_y =0}^{N-1} F[\omega_x, \omega_y] e^{j \left( \omega_x x + \omeag_y y \right)} \end{align}`<br>
<br>

@divend