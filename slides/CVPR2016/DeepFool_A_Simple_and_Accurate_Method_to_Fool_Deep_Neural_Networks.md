#### DeepFool: A Simple and Accurate Method to Fool Deep Neural Networks
###### Seyed-Mohsen Moosavi-Dezfooli, Alhussein Fawzi, Pascal Frossard

@div[left]

__概要__<br>
adversarial examplesに対する頑健さ（adversarial robustness）を定量化するためには、効率的かつ正確にadversarial perturbationを計算する必要がある。L-BFGSを用いた手法は最適解を得ることができる一方で計算量が大きくなる。FGSMは線形近似により求めた準最適解であり、最適解より非常に大きいperturbationとなってしまう。提案手法（DeepFool）は線形近似を反復的に繰り返すことによって、FGSMより最適解に近い準最適解を得ることができる。以上のことを実験で示した上で、adversarial trainingにおいて、過剰なperturbationによる学習は画像のコンテンツ自体が変化してしまい、むしろadversarial robustnessを下げることを確認した。<br>
<br>
__手法・新規性__<br>
DeepFoolは、入力サンプル`$\boldsymbol{x}$`に関する勾配情報を求め、線形近似してboundary上に乗るようなperturbationを計算し、perturbationを加える操作を反復的に繰り返すことによってperturbationを求める。ここでは２クラス分類器の場合を説明する（多クラス分類への適用は論文を参照）。スカラー値関数`$f:\mathbb{R}^n \to \mathbb{R}$`を用いて、２クラス分類器は`$\hat{k}(\boldsymbol{x})={\rm sign}(f(\boldsymbol{x}))$`と表せる。関数`$f$`がアフィン変換関数であるとすると、`$f(\boldsymbol{x})=\boldsymbol{w}^t \boldsymbol{x} + b$`と表すことができ、分類境界は`$\mathcal{F} = \left\{ \boldsymbol{x}: f(\boldsymbol{x})=0 \right\}$`となる。このようなとき最適なperturbation`$\boldsymbol{r}_{\ast}$`は以下の式で表せる。<br>
`\begin{align} \boldsymbol{r}_{\ast}(\boldsymbol{x}) = - \frac{f(\boldsymbol{x})}{\|\boldsymbol{w}\|_{2}^{2}} \boldsymbol{w} \end{align}`
実際には識別結果を変化させるにはboundaryをわずかに超える必要があるため、`$1+\eta (\eta << 1)$`倍（論文中では`$\eta=0.02$`）する必要がある。また実際の識別器は線形ではないため、上述の計算を反復的に繰り返すことによって解を得る。<br>
またadversarial robustnessの指標として以下の指標を利用した。<br>
`\begin{align} \rho_{adv} (\hat{k}) \mathbb{E}_{\boldsymbol{x}} \frac{\Delta (\boldsymbol{x}; \hat{k})}{\|\boldsymbol{x}\|_2} \end{align}`

@divend

@div[right]

![](assets/img/DeepFool_A_Simple_and_Accurate_Method_to_Fool_Deep_Neural_Networks.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1511.04599.pdf)<br>
・[GitHub](http://github.com/lts4/deepfool)<br>

@divend