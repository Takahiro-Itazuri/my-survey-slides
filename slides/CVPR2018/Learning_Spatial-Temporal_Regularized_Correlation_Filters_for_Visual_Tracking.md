#### Learning Spatial-Temporal Regularized Correlation Filters for Visual Tracking
###### Feng Li, Cheng Tian, Wangmeng Zuo, Lei Zhang, Ming-Hsuan Yang
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    In this work, by introducing temporal regularization to Spatially Regularized Discriminative Correlation Filter (SRDCF) with single sample, we present our spatial-temporal regularized correlation filters (STRCF). <br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>A STRCF model is presented by incorporating both spatial and temporal reguralization into the DCF framework. Based on online PA, STRCF can not only serve as a rational approximation of the SRDCF formulation on multiple training images, but also provide a more robust appearance model than SRDCF in the case of large appearance variations.</li>
      <li>An ADMM algorithm is developed for solving STRCF efficiently, where each sub-problem has the closed-form solution. And our algorithm can empirically converge within very few iteractions.</li>
      <li>Our STRCF with hand-crafted feature can run in real-time, achieves notable improvements over SRDCF by tracking accuracy. Furthermore, our STRCF with deep features performs favorably in comparison with the state-of-the-art trackers.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://www4.comp.polyu.edu.hk/~cslzhang/paper/CVPR18_Tracking.pdf">paper</a></li>
    </ul><br>
  </div>
  <div class="col">
     STRCF model<br>
    `$$ \mathop{\rm arg~min}\limits_{\bf f} \frac{1}{2} { \| \sum_{d=1}^{D} {\bf x}_{t}^{d} \ast {\bf f}^{d} - {\bf y} \| }^{2} + \frac{1}{2} \sum_{d=1}^{D} {\| {\bf w} \cdot {\bf f}^{d} \|}^{2} + \frac{\mu}{2} {\| {\bf f} - {\bf f}_{t-1} \|}^{2} $$`
    Augmented Lagrangian form<br>
    `$$ L({\bf w}, {\bf g}, {\bf s}) = \frac{1}{2} {\| \sum_{d=1}^{D} {\bf x}^{d}_{t} \ast {\bf f}^{d} - {\bf y} \|}^{2} + \frac{1}{2} \sum_{d=1}^{D} {\| {\bf w} \cdot {\bf g}^d \|}^{2} $$`
    `$$ + \sum_{d=1}^{D} \left( {\bf f}^{d} - {\bf g}^{d} \right)^{T} {\bf s}^{d} + \frac{\gamma}{2} \sum_{d=1}^{D} {\| {\bf f}^{d} - {\bf g}^{d} \|}^{2} + \frac{\mu}{2} {\| {\bf f} - {\bf f}_{t-1} \|}^{2} $$`
    By introducing `$ {\bf h} = \frac{1}{\gamma} {\bf s} $`<br>
    `$$ L({\bf w}, {\bf g}, {\bf s}) = \frac{1}{2} {\| \sum_{d=1}^{D} {\bf x}^{d}_{t} \ast {\bf f}^{d} - {\bf y} \|}^{2} + \frac{1}{2} \sum_{d=1}^{D} {\| {\bf w} \cdot {\bf g}^d \|}^{2} $$`
    `$$ + \frac{\gamma}{2} \sum_{d=1}^{D} {\| {\bf f}^{d} - {\bf g}^{d} + {\bf h}^{d} \|}^{2} + \frac{\mu}{2} {\| {\bf f} - {\bf f}_{t-1} \|}^{2} $$`
    By adopting ADMM algorithm<br>
    `$$ {\bf f}^{(i+1)} = \mathop{\rm arg~min}\limits_{\bf f} \| \sum_{d=1}^{D} {\bf x}^{d}_{t} \ast {\bf f}^{d} - {\bf y} \| + \gamma {\| {\bf f} - {\bf g} + {\bf h} \|}^{2} + \mu {\| {\bf f} - {\bf f}_{t-1} \|}^{2} $$`
    `$$ {\bf g}^{(i+1)} = \mathop{\rm arg~min}\limits_{\bf g} \sum_{d=1}^{D} {\| {\bf w} \cdot {\bf g}^{d} \|}^{2} + \gamma {\| {\bf f} - {\bf g} + {\bf h} \|}^{2} $$`
    `$$ {\bf h}^{(i+1)} = {bf h}^{(i)} + {\bf f}^{(i+1)} - {\bf g}^{(i+1)} $$`
  </div>
</div>
