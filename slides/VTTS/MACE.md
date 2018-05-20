#### Minimum Average Correlation Energy (MACE) Filters

@div[left]

MACEはターゲットの位置のピークを固定値(1)に拘束しながら、全体の相関の平均を最小化する問題を解く。<br>
`\begin{align} \mathop{\rm min}\limits_{\boldsymbol{w}} \| \boldsymbol{x} \otimes \boldsymbol{w} \|^{2} \\ {\rm subject \;\; to \;\; } \boldsymbol{w}^T \boldsymbol{x} = 1 \end{align}`

@divend

@div[right]

@divend