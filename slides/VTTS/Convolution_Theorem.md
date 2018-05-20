#### Convolution Theorem

@div[left]

__1D Continuous Convolution Theorem__<br>

__1D Discrete Convolution Theorem__<br>

__2D Continuous Convolution Theorem__<br>

__2D Discrete Convolution Threorem__<br>


@divend

@div[right]

__Proof (1D Continuous COnvolution Theorem)__

`\begin{align} F(u) &= \mathcal{F} \left\{f \right\} = \int_{\mathbb{R}^n} f(x) e^{-2 \pi j x \cdot u} dx \\ G(u) &= \mathcal{F} \left\{ g \right\} = \int_{\mathbb{R}^n} g(x) e^{-2 \pi j x \cdot u} dx \\ h(z) &= \int_{\mathbb{R}^n} f(x)g(z-x) dx \\ H(u) &= \mathcal{F} \left\{ h \right\} = \int_{\mathbb{R}^n} h(z) e^{-2 \pi j z \cdot u} dz \\ &= \int_{\mathbb{R}^n} \int_{\mathcal{R}^n} f(x)g(z-x) dx e^{-2 \pi j z \cdot u} dz \\ &= \int_{\mathbb{R}^n} f(x) \left( \int_{\mathbb{R}^n} g(z-x) e^{-2 \pi j z \cdot u} dz \right) dx \\ &= \int_{\mathbb{R}^n} f(x) \left( \int_{\mathbb{R}^n} g(y) e^{-2 \pi j (y+x) \cdot u} dy \right) dx \\ &= \int_{\mathbb{R}^n} f(x) e^{-2 \pi j x \cdot u} \left( \int_{\mathbb{R}^n} g(y) e^{-2 \pi j y \cdot u} dy \right) \\ &= \int_{\mathbb{R}^n} f(x) e^{-2 \pi j x \cdot u} dx \int_{\mathbb{R}^n} g(y) e^{-2 \pi j y \cdot u} dy \\ &= F(u) \cdot G(u) \end{align}`

@divend