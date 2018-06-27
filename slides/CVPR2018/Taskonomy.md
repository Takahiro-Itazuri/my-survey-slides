#### Taskonomy: Disentangling Task Transfer Learning
###### Amir R. Zamir, Alexander Sax, William Shen, Leonidas Guibas, Jitendra Malik, Silvio Savarese

@div[left]

__概要__<br>
様々なCVのタスクには互いに密接な関係があり、それらが織り成す構造を明らかにすること（<b>taskonomy</b>: <b>task</b> tax<b>onomy</b>）が本論文の目的である。これにより転移学習に大きな貢献をもたらす。taskonomyは計算によって求められた転移学習のしやすさの概念を示す有向グラフである。本論文では26のCVのタスクにおいて実験を行った。<br>
<br>
__手法・新規性__<br>
４つのステップでtaskonomyを構築する。<br>
<b>Step 1. Task-Specific Modeling</b>: 各タスクにおいてencoder-decoder構造のネットワークを学習する。<br>
<b>Step 2. Transfer Modeling</b>: ロス関数`$L_t$`を最小化するようにdecoder（readout function）を学習する。<br>
`\begin{align} D_{s \to t} = \mathop{\rm arg~min}\limits_{\theta} \mathbb{E}_{I \in D} \left\[ L_t \left( D_{\theta} \left( E_s (I) \right), f_t (I) \right) \right\] \end{align}`


@divend

@div[right]

![Taskonomy](assets/img/Taskonomy.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Zamir_Taskonomy_Disentangling_Task_CVPR_2018_paper.pdf)<br>
・[プロジェクト](http://taskonomy.stanford.edu/)<br>
・[Supplemental](http://taskonomy.stanford.edu/taskonomy_supp_CVPR2018.pdf)

@divend
