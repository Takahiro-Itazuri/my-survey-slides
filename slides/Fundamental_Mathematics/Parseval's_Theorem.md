#### Parseval's Theorem

@div[left]

<b>General</b><br>
`\begin{align} \int_{- \infty}^{\infty} f(x) g^{\ast} (x) dx = \frac{1}{2 \pi} \int_{- \infty}^{\infty} F(\mu) G^{\ast} (\mu) d \mu \end{align}`
`\begin{align} \sum_{n=0}^{N-1} f[n] g^{\ast}[n] = \frac{1}{N} \sum_{\mu =0}^{N-1} F[\mu] G[\mu] \end{align}`

<b>Specific</b><br>
`\begin{align} \int_{- \infty}^{\infty} \| f(x) \|^2 dx = \frac{1}{2 \pi} \int_{- \infty}^{\infty} \| F(\mu) \|^2 d \mu \end{align}`
`\begin{align} \sum_{n=0}^{N-1} \| f[n] \|^2 = \frac{1}{N} \sum_{\mu =0}^{N-1} \| F[\mu] \|^2 \end{align}`

@divend

@div[right]

<b>Proof</b><br>
`\begin{align} & \int_{- \infty}^{\infty} F(\mu) G^{\ast} (\mu) d \mu \\ = & \int_{- \infty}^{\infty} \left( \int_{\infty}^{\infty} f(x) e^{-2 \pi j x \mu} dx \right) \left( \int_{\infty}^{\infty} g^{\ast}(y) e^{-2 \pi j y \mu} dy \right) d \mu \\ = & \int_{- \infty}^{\infty} \int_{- \infty}^{\infty} f(x) g^{\ast} (y) \left( \int_{- \infty}^{\infty} e^{-2 \pi j (x - y)} d \mu \right) dx dy \\ = & \int_{- \infty}^{\infty} \int_{- \infty}^{\infty} f(x) g^{\ast} (y)2 \pi \delta (x-y) dx dy \\ = & 2 \pi \int_{- \infty}^{\infty} f(x) g^{\ast} (x) dx \end{align}`

@divend