#### Generative Adversarial Nets
###### Ian J. Goodfellow, Jean Pouget-Abadie, Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozair, Aaron Courville, Yoshua Bengio
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We propose a new framwork for estimating generative models via an adversarial process, in which we simultaneously train two models: a generative model G that captures the data distribution, and a discriminative model D that estimates the probability that a sample came from the training data rather than G. The training procedure for G is to maximize the probability of D making a mistake. This framework corresponds to a minimax two-player game. In the space of arbitrary function G and D, a unique solution exists, with D recovering the training data distribution and D equal to 1/2 everywhere. In the case where G and D are defined by multilayer perceptrons, the entire system can be trained with backpropagation.<br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://papers.nips.cc/paper/5423-generative-adversarial-nets">paper</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2017/06/11000810/g3.png">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/6de2b1058c5b717878cce4e7e50d3a372cc4aaa6/7-Figure2-1.png">
  </div>
</div>