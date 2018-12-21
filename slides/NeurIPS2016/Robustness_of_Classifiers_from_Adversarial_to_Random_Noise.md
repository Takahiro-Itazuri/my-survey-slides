#### Robustness of Classifiers: from Adversarial to Random Noise
###### Alhussein Fawzi, Seyed-Mohsen Moosavi-Dezfooli, Pascal Frossard

@div[left]

__概要__<br>
最新のクラス分類器はadversarial examplesに非常に脆弱であることがわかっている一方で、ランダムノイズに対しては頑健であることもまた知られている。そこで完全にランダムにノイズを選ぶ方法（random noise regime）とadversarial examplesのような意図的にノイズを選ぶ方法（worst-case noise regime）を一般化した、semi-ranodm noise regimeを提案し、それに基づくクラス分類器のrobustnessに関する調査を行った。<br>
<br>
__手法・新規性__<br>
`$L$`クラス分類器を`$f:\mathbb{R}^d \to \mathbb{R}^L$`とし、データポイント`$x_0 \in \mathbb{R}^d$`の推定ラベルは`$\hat{k}(x_0) = \mathop{\rm arg~max}_k f_k (x_0)$`で与えられるとする。また`$\mathcal{S}$`を次元数`$m$`の`$\mathbb{R}^d$`の任意の部分空間とする。このとき、２つのnoise regimeにおけるクラス分類器`$f$`のrobustnessを定量化する。そのために`$\mathcal{S}$`における最小のノルムとなる摂動を以下のように定義する。<br>
`\begin{align} r^{\ast}_{\mathcal{S}} (x_0) = \mathop{\rm argmin}\limits_{r \in \mathcal{S}} \|r\|_2 {\rm \; s.t. \; } \hat{k}(x_0 + r) \neq \hat{k} (x_0) \end{align}`
`$\mathcal{S} = \mathbb{R}^d$`のとき通常のadversarial perturbationに該当し、`$\mathcal{S}$`がランダムに選択された`$1$`次元の部分空間のとき、ランダムノイズに該当する。以降、adversarial perturbationを`$r^{\ast} := r^{\ast}_{\mathbb{R}^d}(x_0)$`とする。クラス分類器`$f$`のrobustnessは`$\|r^{\ast}_{\mathcal{S}}(x_0)\|_2$`で測ることができる。<br>
データから境界までの距離は、random noise regimeの場合`$\sqrt{d}$`に比例するため非常に頑健である一方で、semi-random noise regimeの場合`$\sqrt{d/m}$`に比例するため`$\mathcal{S}$`の次元数が大きくなるにつれて脆弱になることを証明し、それを実験で確認した（詳細は論文を参照）。また実験で証明したことが確認されたことから、証明の際に用いた曲率に関する仮定も成り立っていると予想され、識別器のrobustnessは境界の曲率と密接な関係が存在しえることを示唆した。

@divend

@div[right]

![](assets/img/Robustness_of_Classifiers_from_Adversarial_to_Random_Noise.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1608.08967.pdf)<br>

@divend