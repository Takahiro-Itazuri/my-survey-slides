#### VITAL: VIsual Tracking via Adversarial Learning
###### Yibing Song, Chao Ma, Xiaohe Wu, Lijun Gong, Linchao Bao, Wangmeng Zuo, Chunhua Shen, Rynson Lau, Ming-Hsuan Yang
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    The tracking-by-detection framework consists of two stages, i.e., drawing samples around the target object in the first stage and classifying each sample as the target object or as background in the second stage. The performance of existing trackers using deep classification networks is limited by two aspects. First, the positive samples in each frame are highly spatially overlapped, and they fail to capture rich appearance variations. Second, there exists extreme class imbalance between positive and negative samples. This paper presents the VITAL algorithm to address these two problems via adversarial learning.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>We propose to use a generative adversarial network (GAN) to augment positive samples in the feature space to capture a variety of appearance changes over a temporal span.</li>
      <li>We propose to use higher-order cost sentsitive loss to mine hard negative samples to handle class imbalance.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://arxiv.org/abs/1804.04273">paper</a></li>
      <li><a href="https://youtu.be/uGMoOom6_90">demo</a></li>
      <li><a href="https://ybsong00.github.io/cvpr18_tracking/index">project</a></li>
      <li><a href="https://github.com/ybsong00/Vital_release">code</a></li>
      <li><a href="https://sites.google.com/site/chaoma99/">author</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://ybsong00.github.io/cvpr18_tracking/pipeline.png">
  </div>
</div>