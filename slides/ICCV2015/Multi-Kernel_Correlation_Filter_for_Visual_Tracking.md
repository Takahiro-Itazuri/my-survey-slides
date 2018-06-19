#### Multi-Kernel Correlation Filter for Visual Tracking
###### Ming Tang, Jiayi Feng

@div[left]

__概要__<br>
物体追跡タスクにおいて、Multi-Kernel Correlation Filter (MKCF)はKernelized Correlation Filter (KCF)のカーネルを複数にすることで識別性能を向上させているが、計算量がボトルネックとなっていた。そこで目的関数の上界を目的関数として再設定し、上から押さえるように最適化問題を解くことで、MKCFより高速（150fps）かつ高識別性能な物体追跡手法 (MKCFup)を提案した。<br>
<br>
__手法・新規性__<br>
従来のMKCFは以下を最適化する問題である。<br>
`\begin{align} \mathop{\rm min}\limits_{{\bf \alpha}, {\bf d}} F({\bf \alpha}, {\bf d}) \\ {\rm s.t.} \sum_{m=1}^{M} d_m = 1 \wedge d_m \geq 0 \end{align}`
`$F({\bf \alpha}, {\bf d})$`は以下の通り。<br>
`\begin{align} F({\bf \alpha}, {\bf d}) \end{align}`
MKCFupは`$F({\bf \alpha}, {\bf d})$`の上界を最適化する。<br>
`\begin{align} F({\bf \alpha}, {\bf d}) & \geq \frac{1}{2} \sum_{m=1}^{M} \left( \| {\bf y}_c - d_m {\bf K}_m \alpha \|^2 + \lambda d_m {\bf \alpha}^{T} {\bf K}_m {\bf \alpha} \right) \\ & \equiv U_{F({\bf \alpha}, {\bf d})} \end{align}`

@divend

@div[right]

![MKCFup](assets/img/MKCFup.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_iccv_2015/papers/Tang_Multi-Kernel_Correlation_Filter_ICCV_2015_paper.pdf)<br>

@divend