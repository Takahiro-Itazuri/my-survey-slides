# Survey Slides
### Takahiro Itazuri (Waseda University)
---
### Computer Vision and Pattern Recognition 2017

+++
#### Fine-grained recognition of thousands of object categories with single-example training
###### Leonid Karlinsky, Joseph Shtok, Yochay Tzur, Asaf Tzadok
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We propose an approach for the scenario of fine-grained object detection ad recognition with limited training data and large-scale datasets. The method consists of three main components: a fast initial detection and classification algorithm, Deep Neural Network (DNN) based fine-grained category refinement, and temporal integration for video inputs.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>A non-parameteric probablistic model for multi-scale, fine-grained multi-class detection and recognition, capable of working in the challenging one-training-example per class setup. Accompanied by a sequential three-step inference approach to cope with a very large space of possible unobserved variable assignments: task specific objectness -> per hypothesis class short list prediction -> per hypothesis structured prediction and refinement.</li>
      <li>A fast Nearest Neighbor (NN) search technique capable of searching for hundreds of thousands of image patch descriptors within a set of millions, in less than a second per mega-pixel.</li>
      <li>A DNN combining the detected object images and their associated classification results in order to produce fine-grained classification refinement. The network is trained on synthetic data</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://openaccess.thecvf.com/content_cvpr_2017/papers/Karlinsky_Fine-Grained_Recognition_of_CVPR_2017_paper.pdf">paper</a></li>
      <li><a href="https://www.youtube.com/watch?v=V0lFpsfkMlE">presentation</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/306f519c545396f429530dbf7e392baa2427d557/1-Figure1-1.png">
  </div>
</div>

+++
#### S3Pool: Pooling with Stochastic Spatial Sampling
###### Shuangfei Zhai, Hui Wu, Abhishek Kumar, Yu Cheng, Yongxi Lu, Zhongfei Zhang, Rogerio Feris
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We propose a novel pooling strategy with stochastic spatial sampling (S3Pool), where the regular downsamlping is replaced by a more general stochastic version. We observe that this general stochasticity acts as a strong regularizer, and can also be seen as doing implicit data augmentation by introducing distortions in the feature maps.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>S3Pool implicitly auguments the training data at each pooling stage which enables superior generalization ability of the learned model.</li>
      <li>S3Pool is simple to implement and introduces little computational overhead compared to general max pooling, which makes it a desirable design choice for learning deep CNNs.</li>
    </ul>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhai_S3Pool_Pooling_With_CVPR_2017_paper.pdf">paper</a></li>
    </ul>
  </div>
  <div class="col">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/424eacf8ee5e90c0243742563b7bf8fe0981df71/2-Figure1-1.png">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/424eacf8ee5e90c0243742563b7bf8fe0981df71/3-Figure2-1.png">
  </div>
</div>

+++
#### A Low Power, Fully Event-Based Gesture Recognition System
###### Arnon Amir, Brian Taba, David Berg, Timothy Melano, Jeffrey McKinstry, Carmelo Di Nolfo, Tapan Nayak, Alexander Andreopoulos, Guillaume Garreau, Marcela Mendoza, Jeff Kusnitz, Micheal Debole, Steve Esser, Tobi Delbruck, Myron Flickner, Dharmendra Modha
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We present the first gesture recognition system implemented end-to-end on event-based hardware, using TrueNorth neurosynaptic processor to recognize hand gestures in real-time at lower power from events streamed live by a Dynamic Vision Sensor (DVS). TrueNorth, IBM's brain-like microprocessor, has been found to be exceptionally proficient at inference work for deep neural network.
    <br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>A gesture recognition system is implemented on event-based hardware that operates on live event streams in real-time.</li>
      <li>A new hand-gesture dataset is collected with an event-based camera.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://openaccess.thecvf.com/content_cvpr_2017/papers/Amir_A_Low_Power_CVPR_2017_paper.pdf">paper</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/19e32d6a4333f9dfbd73feaafdbecfa1bcbb6d16/5-Figure4-1.png">
    <img width="50%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/19e32d6a4333f9dfbd73feaafdbecfa1bcbb6d16/5-Figure5-1.png">
  </div>
</div>

+++
#### Personalizing Gesture Recognition Using Hierarchical Bayesian Neural Networks
###### Ajjen Joshi, Soumya Ghosh, Margrit Betke, Stan Sclaroff, Hanspeter Pfister
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We develop hierarchical Bayesian neural network to capture subject-specific variations and share statistical strength across subjects. We also develop methods for adapting our model to new subjects when a small number of subject-specific personalization data is available.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>Develop hierarchical Bayesian neural networks for personalized gesture recognition in the presence of inter-subject variations</li>
      <li>Adapt reduced variance versions of stochastic variational inference for learning the posterior distribution over model parameters</li>
      <li>Utilize that inferred posterior to drive an active learning procedure that consistently improves over naive personalization.</li>
    </ul>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://openaccess.thecvf.com/content_cvpr_2017/papers/Joshi_Personalizing_Gesture_Recognition_CVPR_2017_paper.pdf">paper</a></li>
    </ul>
  </div>
  <div class="col">
    <img width="60%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/36e0ba5f46d0eb0f75ed17b8776fa90c5ba83d43/1-Figure1-1.png">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/36e0ba5f46d0eb0f75ed17b8776fa90c5ba83d43/2-Figure2-1.png">
  </div>
</div>

+++
#### Social Scene Understanding: End-to-End Multi-Person Action Localization and Collective Activity Recognition
###### Timur Bagautdinov, Alexandre Alahi, Francois Fleuret, Pascal Fua, Silvio Savarese
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    This method takes as input raw image sequences ad produces a comprehensive social scene interpretation: locations of individuals, thier individual social actions, and the collective activity.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>a unified framework for social scene understading by simultaneously solving three tasks ina single feed forward network: multi-person detection, individual's action recogntion and collective activity recognition.</li>
      <li>a novel multi-object detection scheme</li>
      <li>a person-level matching RNN model to propagate information in the temporal domain</li>
    </ul>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://www.idiap.ch/~fleuret/papers/bagautdinov-et-al-cvpr2017.pdf">paper</a></li>
      <li><a href="https://github.com/cvlab-epfl/social-scene-understanding">github</a></li>
    </ul>
  </div>
  <div class="col">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/7d14700ea26a90eeba4e9cafbfc4ce8b6ec0e9fb/8-Figure4-1.png">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/7d14700ea26a90eeba4e9cafbfc4ce8b6ec0e9fb/3-Figure2-1.png">
  </div>
</div>


+++
#### The World of Fast Moving Objects
###### Denys Rozumnyi, Jan Kotera, Filip Sroubek, Lukas Novotny, Jiri Matas

+++
#### Deep Network Flow for Multi-Object Tracking
###### Samuel Schulter, Paul Vernaza, Wongun Choi, Manmohan Chandraker

---
### Computer Vision and Pattern Recognition Workshops 2017
+++
#### Automatic Curation of Golf Highlighting using Multimodal Excitement Features
###### Michele Merler, Dhiraj Joshi, Quoc-Bao Nguyen, Stephen Hammer, John Kent, John R. Smith, Rogerio S. Feris
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    A novel approach for auto-curating sports highlights, showcasing its application in extracting golf play highlights. We measure the excitement lebel of video segments based on the following multimodal markers: player reaction, spectators, commentator. Our system is called High-Five (Highlights From Intelligent Video Engine), H5 in short.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>a first-of-kind system for automatically extracting golf highlightings by uniquely fusing multimodal excitement measures from the player, spectators, and commentators. personalized highlight retrieval or alerts based on player name, hole number, location, and time.</li>
      <li>novel techniques are introduced for learning our multimodal classifiers without requiring costly manual training data annotation.</li>
      <li>an extensive evaluation, showing the importance of each component in our proposed approach, and comparing our results with professionally curated highlights.</li>
    </ul>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8014748">paper</a></li>
    </ul>
  </div>
  <div class="col">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/2024c9e06c6e8082dadca2977ef0356a743b9905/1-Figure1-1.png">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/2024c9e06c6e8082dadca2977ef0356a743b9905/3-Figure2-1.png">
  </div>
</div>

---
### SIGGRAPH 2017
+++
#### VNect: Real-time 3D Human Pose Estimation with a Single RGB Camera
###### Dushyant Mehta, S
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    Real-time method to capture the full global 3D skeltal pose of a human in a stable, temporally consistent manner using a single RGB camera.
    <u><b>Contribution</b></u><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3073596">Paper</a></li>
      <li><a href="http://gvv.mpi-inf.mpg.de/projects/VNect/">Project Page</a></li>
      <li><a href="https://www.youtube.com/watch?v=W1ZNFfftx2E">Demo Video</a></li>
      <li><a href="https://www.youtube.com/watch?v=m3KG_Z0P_nU">Presentation Video</a></li>
      <li><a href="https://github.com/timctho/VNect-tensorflow">GitHub</a></li>
    </ul>
  </div>
  <div class="col">
    <img src="https://raw.githubusercontent.com/Takahiro-Itazuri/my-survey-slides/master/assets/img/">
  </div>
</div>

---
### Computer Visiona and Pattern Recognition 2016
+++
#### Rethinking the Inception Architecture for Computer Vision
###### Christian Szegedy, Vincent Vanhoucke, Sergey Ioffe, Jon Shlens
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    <u><b>Contribution</b></u><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Szegedy_Rethinking_the_Inception_CVPR_2016_paper.pdf">paper</a></li>
    </ul>
  </div>
  <div class="col">
    <img src="https://raw.githubusercontent.com/Takahiro-Itazuri/my-survey-slides/master/assets/img/">
  </div>
</div>

---
### European Conference on Computer Vision 2016
+++
#### Video Summarization with Long Short-term Memory
###### Ke Zhang, Wei-Lun Chao, Fei Sha, and Kristen Grauman
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    <u><b>Contribution</b></u><br>
    <u><b>Links</b></u><br>
  </div>
  <div class="col">
    <img width="100%" src="http://www-scf.usc.edu/~zhan355/ke_eccv2016.pdf">
  </div>
</div>

---
### ACM Multimedia
+++
#### 
###### Authors
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    <u><b>Contribution</b></u><br>
    <u><b>Links</b></u><br>
  </div>
  <div class="col">
    <img width="100%" src="http://delivery.acm.org/10.1145/2970000/2964286/p908-bettadapura.pdf?ip=133.9.4.18&id=2964286&acc=ACTIVE%20SERVICE&key=D2341B890AD12BFE%2EF9D920C4190321DF%2E4D4702B0C3E38B35%2E4D4702B0C3E38B35&__acm__=1523343437_56d3bdba4c80ff7bfa87563295a871b4">
  </div>
</div>

---
### Template
+++
#### Title
###### Authors
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    <br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li></li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href=""></a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="">
    <img width="100%" src="">
  </div>
</div>