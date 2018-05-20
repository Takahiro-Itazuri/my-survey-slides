#### Cross-Correlation Theorem

@div[left]

__1D Continuous Cross-Correlation Theorem__<br>
`\begin{align} H(\mu) = F^{\ast}(\mu) \cdot G(\mu) \end{align}`<br>
<br>
__2D Continuous Cross-Correlation Theorem__<br>
`\begin{align} H(\mu, \nu) = F^{\ast}(\mu, \nu) \cdot G(\mu, \nu) \end{align}`<br>
<br>
__1D Discrete Cross-Correlation Theorem__<br>
`\begin{align} H[\mu] = F^{\ast}[\mu] \cdot G[\mu] \end{align}`<br>
<br>
__2D Discrete Cross-Correlation Threorem__<br>
`\begin{align} H[\mu, \nu] = F^{\ast}[\mu, \nu] \cdot G[\mu, \nu] \end{align}`<br>
<br>

@divend

@div[right]

__Proof (1D Continuous Cross-Correlation Theorem)__

`\begin{align} F^{\ast}(\mu) &= \left( \mathcal{F} \left\{f \right\} \right)^{\ast} = \int_{\mathbb{R}^n} f^{\ast}(x) e^{2 \pi j x \cdot \mu} dx \\ G(\mu) &= \mathcal{F} \left\{ g \right\} = \int_{\mathbb{R}^n} g(x) e^{-2 \pi j x \cdot \mu} dx \\ h(z) &= \int_{\mathbb{R}^n} f^{\ast}(x)g(z+x) dx \\ H(\mu) &= \mathcal{F} \left\{ h \right\} = \int_{\mathbb{R}^n} h(z) e^{-2 \pi j z \cdot \mu} dz \\ &= \int_{\mathbb{R}^n} \int_{\mathcal{R}^n} f^{\ast}(x)g(z+x) dx e^{-2 \pi j z \cdot \mu} dz \\ &= \int_{\mathbb{R}^n} f^{\ast}(x) \left( \int_{\mathbb{R}^n} g(z+x) e^{-2 \pi j z \cdot \mu} dz \right) dx \\ &= \int_{\mathbb{R}^n} f^{\ast}(x) \left( \int_{\mathbb{R}^n} g(y) e^{-2 \pi j (y-x) \cdot \mu} dy \right) dx \\ &= \int_{\mathbb{R}^n} f^{\ast}(x) e^{2 \pi j x \cdot \mu} \left( \int_{\mathbb{R}^n} g(y) e^{-2 \pi j y \cdot \mu} dy \right) \\ &= \int_{\mathbb{R}^n} f^{\ast}(x) e^{2 \pi j x \cdot \mu} dx \int_{\mathbb{R}^n} g(y) e^{-2 \pi j y \cdot \mu} dy \\ &= F^{\ast}(\mu) \cdot G(\mu) \end{align}`

@divend