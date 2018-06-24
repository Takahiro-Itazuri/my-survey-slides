#### Hierarchical Convolutional Features for Visual Tracking
###### Chao Ma, Jia-Bin Huang, Xiaokang Yang, Ming-Hsuan Yang

@div[left]

__概要__<br>
物体認識タスクで学習したネットワークにおいて、出力層に近い層では、セマンティックな情報を持つため見た目の変化強いが、空間解像度が低い。入力層に近い層では、見た目の変化に敏感であるが、十分な空間解像度を持つという特徴がある。この考察を元に、CNNの複数の層に対してCorrelation Filterを用意し、それらを階層的に利用して粗から密に追跡対象の位置を推定する。<br>
<br>
__手法・新規性__<br>
VGG19のconv3-4、conv4-4、conv5-4の層を利用し、各層に対してMulti-Channel Correlation Filterを用意する。各層から得られる相関出力の組を`$\left\{ f_l \right\}$`とし、以下の式に従って階層的に対象物体の位置を算出する。<br>
`\begin{align} \mathop{\rm arg~max}\limits_{(m,n)} f_{l-1} (m,n) + \gamma f_l (m,n) \\ {\rm s.t.} \; |m - \hat{m}| + | n - \hat{n} | \geq r \end{align}`
各層のCorrelation Filterは以下の式で更新する。<br>
`\begin{align} \boldsymbol{A}_t^d &= (1 - \eta) \boldsymbol{A}_{t-1}^{d} + \eta \boldsymbol{Y} \odot \hat{\boldsymbol{X}}_t^d \\ \boldsymbol{B}_t^d &= (1 - \eta) \boldsymbol{B}_{t-1}^{d} + \eta \sum_{i=1}^{D} \boldsymbol{X}_t^i \odot \hat{\boldsymbol{X}}_t^i \\ \boldsymbol{W}_t^d &= \frac{\boldsymbol{A}_t^d}{\boldsymbol{B}_t^d + \lambda} \end{align}`

@divend

@div[right]

![HCF](assets/img/HCF.png =full)<br>

__リンク__<br>
・[論文](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Ma_Hierarchical_Convolutional_Features_ICCV_2015_paper.pdf)<br>
・[MATLAB code](https://github.com/chaoma99/HCFTstar)<br>
・[プロジェクト](https://sites.google.com/site/chaoma99/iccv15-tracking)

@divend