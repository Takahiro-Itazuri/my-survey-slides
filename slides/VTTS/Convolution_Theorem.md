#### Convolution Theorem

@div[left]

__1D Continuous Convolution Theorem__<br>
`\begin{align} H(\mu) = F(\mu) \cdot G(\mu) \end{align}`

__2D Continuous Convolution Theorem__<br>
`\begin{align} H(\mu, \nu) = F(\mu, \nu) \cdot G(\mu, \nu) \end{align}`

__1D Discrete Convolution Theorem__<br>
`\begin{align} H[\mu] = F[\mu] \cdot G[\mu] \end{align}`

__2D Discrete Convolution Threorem__<br>
`\begin{align} H[\mu, \nu] = F[\mu, \nu] \cdot G[\mu, \nu] \end{align}`

@divend

@div[right]

__Proof (1D Continuous Convolution Theorem)__

`\begin{align} F(\mu) &= \mathcal{F} \left\{f \right\} = \int_{\mathbb{R}^n} f(x) e^{-2 \pi j x \cdot \mu} dx \\ G(\mu) &= \mathcal{F} \left\{ g \right\} = \int_{\mathbb{R}^n} g(x) e^{-2 \pi j x \cdot \mu} dx \\ h(z) &= \int_{\mathbb{R}^n} f(x)g(z-x) dx \\ H(\mu) &= \mathcal{F} \left\{ h \right\} = \int_{\mathbb{R}^n} h(z) e^{-2 \pi j z \cdot \mu} dz \\ &= \int_{\mathbb{R}^n} \int_{\mathcal{R}^n} f(x)g(z-x) dx e^{-2 \pi j z \cdot \mu} dz \\ &= \int_{\mathbb{R}^n} f(x) \left( \int_{\mathbb{R}^n} g(z-x) e^{-2 \pi j z \cdot \mu} dz \right) dx \\ &= \int_{\mathbb{R}^n} f(x) \left( \int_{\mathbb{R}^n} g(y) e^{-2 \pi j (y+x) \cdot \mu} dy \right) dx \\ &= \int_{\mathbb{R}^n} f(x) e^{-2 \pi j x \cdot \mu} \left( \int_{\mathbb{R}^n} g(y) e^{-2 \pi j y \cdot \mu} dy \right) \\ &= \int_{\mathbb{R}^n} f(x) e^{-2 \pi j x \cdot \mu} dx \int_{\mathbb{R}^n} g(y) e^{-2 \pi j y \cdot \mu} dy \\ &= F(\mu) \cdot G(\mu) \end{align}`

@divend