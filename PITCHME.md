# Survey Slides
### Takahiro Itazuri (Waseda University)

<!--
  CVPR 2018
-->
---
### CVPR 2018
+++
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
    $$ ma = F $$
  </div>
</div>

$$ ma = F $$

<!--
  CHI 2018
-->
---
### CHI 2018

+++
#### Hoarding and Minimalism: Tendencies in Digital Data Preservation
###### Francesco Vitale, Izabelle Janzen, Joanna McGrenere
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
     We focused on a main, broad research question: how do people approach digital data preservation in the cloud age? How do they decide what to keep and discard? We interviewed 23 participants with diverse backgrounds, asking them about their perceived digital data. I an interative analysis process, we uncovered a spectrum of tendencies that drive preservation strategies, with two extremes: hoarding (where participants accumulated large amounts of data, even if considered of little value) and minimalism (where they kept as little as possible, regularly clearning their data). We contrast and compare the two extremes of the spectrum, characterize their nuanced nature, and discuss how our categorization compares to previously reported behaviors. We conclude with broad implications for shaping technology.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>bringing to light a spectrum of tendencies with hoarding and minimalism on two ends, characterizing them in depth</li>
      <li>comparing and contrasting different user behaviors, showing their common role for identity construction</li>
      <li>putting them in context compared to previously reported behaviors in the literature</li>
      <li>giving implications for shaping technology, opening rich possibilities for future work.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?doid=3173574.3174161">paper</a></li>
      <li><a href="https://youtu.be/cyBI77VsUM4">demo</a></li>
      <li><a href="http://www.francescovitale.com/">Francesco Vitale's web page</a></li>
    </ul><br>
  </div>
  <div class="col">
    <iframe width="100%" height="100%" src="https://www.youtube.com/embed/cyBI77VsUM4" frameborder="0"></iframe>
  </div>
</div>

+++
#### Pinpointing: Precise Head- and Eye-Based Target Selection for Augmented Reality
###### Authors
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    It is important to design interaction techniques that allow precise selection and manipulation of virtual objects, without bulky input devices. This paper explores Pinpointing: multimodal head and eye gaze pointing techniques for wearable AR. A comparison of speed and poiting accuracy reveals the relative merits of each method, including the achievable target size for robust selection. We demonstrate and discuss example applications for augmented reality, including compact menus wth deep structure, and a proof-of-concept method for on-line correction of calibration drift.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>A broad comparison of target selection accuracy and speed for eye gaze, head pointing, and several multimodal techniques for improved accuracy.</li>
      <li>Adoption of multimodal techniques for wearable AR, resulting in several previously unexplored implementations that refine coarse eye gaze and head pointing with fine hand gesture, device gyro and head motion input.</li>
      <li>Two example applications that demonstrate the potential of Pinpointing for improving wearable AR interaction: GazeBrowser uses gaze interaction with high precision pointing to navigate compact smart object menus. SmartPupil shows a novel online method for mitigating calibration drift of wearable eye trackers.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3173655">paper</a></li>
      <li><a href="https://youtu.be/nCX8zIEmv0s">short demo</a></li>
      <li><a href="https://youtu.be/q9cbAfxKAPI">long demo</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://www.researchgate.net/profile/Mikko_Kytoe/publication/323970135/figure/fig4/AS:607431939854342@1521834468613/Compact-fractal-radial-menus-with-deep-structure-in-GazeBrowser-a-Example-application_big.png">
    <img width="100%" src="https://www.researchgate.net/profile/Robert_Teather/publication/320315146/figure/fig3/AS:616365635420162@1523964427750/Error-rate-by-target-size-and-target-depth-for-each-input-method-Note-m-depth.png">
  </div>
</div>

+++
#### Wall++: Room-Scale Interactive and Context-Aware Sensing
###### Yang Zhang, Chouchang Yang, Scott E. Hudson, Chris Harrison, Alanson Sample
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We present Wall++, a low-cost sensing approach that allows walls to become a smart infrastructure. Instead of merely separating spaces, walls can now enhance rooms with sensing and interactivity. Our wall treatment and sesing hardware can track users' touch and gesture, as well as estimate body pose if they are close. By capturing ariborne electromagnetic noise, we can also detect what appliances are active and where they are located. Through a series of evaluations, we demonstrate Wall++ can enable robust room-scale interative and context-aware applications.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li></li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://www.yang-zhang.me/research/Wall/Wall.pdf">paper</a></li>
      <li><a href="https://youtu.be/HSPdcuDT5fU">short demo</a></li>
      <li><a href="https://youtu.be/P7htrEO9kJo">long demo</a></li>
      <li><a href="http://yang-zhang.me.s3-website-us-east-1.amazonaws.com/research/Wall/Wall.html">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="http://yang-zhang.me.s3-website-us-east-1.amazonaws.com/research/Wall/images/paint3.jpg">
    <img width="100%" src="http://yang-zhang.me.s3-website-us-east-1.amazonaws.com/research/Wall/images/single_touch.jpg">
  </div>
</div>

+++
#### Agile 3D Sketching with Air Scaffolding
###### Yongkwan Kim, Sang-Gyun An, Joon Hyub Lee, Seok-Hyung Bae
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    3D sketching using hand motion is rapid but rough, and 3D sketching using pen drawing is delicate but tedious. Our new 3D sketching workflow combines these two ina complementary manner. The user makes quick hand motions in the air to generate approximate 3D shapes, and uses them as scaffolds on which to add details via pen-based 3D sketching on a tablet device. Our air scaffolding technique and corresponding algorithm extract only the intended shapes from unconstrained hand motion.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>Propose a 3D sketching workflow combining strengths of hand and pen input.</li>
      <li>Devise an algorithm to indentify descriptive hand motions from transitory and extract air scaffolds from the identified motions.</li>
      <li>Integrate the air scaffolding technique with pen-based 3D sketching into a practical system.</li>
      <li>Evaluate our system with users to verify that air scaffolding facilities idea exploration through agile 3D sketching.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3173812">paper</a></li>
      <li><a href="https://youtu.be/Nh1cD9woB2M">short demo</a></li>
      <li><a href="https://youtu.be/CiKWnfbNjUY">long demo</a></li>
      <li><a href="http://i2dea.kaist.ac.kr/publications/2018_chi_agile_air_scaffolding">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="http://i2dea.kaist.ac.kr/images/publications/2018_chi_agile_air_scaffolding.jpg">
  </div>
</div>

+++
#### Expressive Time Series Querying with Human-Drawn Scale-Free Sketching
###### Miro Mannino, Azza Abouzied
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We present Qetch, a tool where users freely sketch patterns on a scale-less canvas to query time series data without specifying query length or amplitude. We study how humans sketch time series patterns and we develop a novel matching algorithm that accounts for human sketching errors. Qetch enables the easy construction of complex and expressive queries with two key features: <i>regular expressions over sketches</i> and <i>relative positioning of sketches</i> to query multiple time-aligned series.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>We present Qetch, a tool where users freely sketch patterns on a scale-kess canvas to query time series data without specifying query length or amplitude.</li>
      <li>We develop a novel matching algorithm that tolerantes the absence of time and amplitude scales on a sketch.</li>
      <li>Qetch outperforms commonly-used time series algorithms like dynamic time warping (DTW) and Euclidean distance (ED).</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3173962">paper</a></li>
      <li><a href="https://youtu.be/g4uI_TGl3UI">demo</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://i.ytimg.com/vi/g4uI_TGl3UI/maxresdefault.jpg">
  </div>
</div>

+++
#### Extending Manual Drawing Practices with Artist-Centric Programming Tools
###### Jennifer Jacobs, Joel Brandt, Radomir Mech, Mitchel Resnick
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    Our research question is "How can we develop programming environments thta support the integration of procedural and manual art?" We created Dynamic Brushes, a visual programming and drawing environment for blending manual and procedural production through personal tool creation.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>We introduce Dynamic Brushes, an integrated visual programming and stylus-based drawing environment.</li>
      <li>We demonstrate the Dynamic Brushes programming model, which enables the creation of numerous tool behaviors through a small number of primitives and operations.</li>
      <li>We demonstrate how procedural tool creation can extend manual practices, support reflection, and foster agency through an extended evaluation with professional artists.</li>
      <li>We provide insights for developing learnable and expressive procedural tools that are compatible with manual creation.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://joelbrandt.com/publications/jacobs-chi2018-extending-manual-drawing.pdf">paper</a></li>
      <li><a href="https://vimeo.com/241743740">demo</a></li>
      <li><a href="http://web.media.mit.edu/~jacobsj/#db">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="http://web.media.mit.edu/~jacobsj/images/dynamic_brushes/dynamic_brushes.004.png">
  </div>
</div>

+++
#### Voice Interfaces in Everyday Life
###### Martin Porcheron, Joel E. Fischer, Stuart Reeves, Sarah Sharples
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    Research that empirically examines the social and interactional issues of Voice User Interfaces (VUIs) in everyday use is lacking. Our study documents the methodical practices of VUI users, and how that use is accomplished in the complex social life of the home. We discuss how the VUI is finely coordinated with the sequential organisation of talk. Finally, we locate implications for the accountability of VUI interaction, request and response design, and raise conceptual challenges to the motion of designing 'conversational' interfaces.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>The analysis presented here explicates how VUI use is routinely accounted for and embedded in talk-in-interaction.</li>
      <li>We turned to transferring our findings from that of matters of interaction to conceptual discussion points, to inform and shape future research and design on the use of VUIs.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=2504391">paper</a></li>
    </ul><br>
  </div>
  <div class="col">
  </div>
</div>

+++
#### Data Illustrator: Augumenting Vector Design Tools with Lazy Data Binding for Expressive Visualization Authoring
###### Zhicheng Liu, John Thompson, Alan Wilson, Mira Dontcheva, James Delorey, Sam Grigg, Bernard Kerr, John Stasko
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We present a novel framework that describes the generation of visualizations from the perspective of graphic design. Based on the framework, we design and build Data Illustrator, a system that augments vector design tools with lazy data binding for visualization authoring.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>We propose a novel framwork for visualiaztion authoring based on the lazy data encoding approach. This framework describes components in a visualization using graphic design concepts such as <i>shape, anchor point, segment</i>, and <i>group</i>. Two operators, <i>repeat</i> and <i>partition</i>, generates shapes and anchor points, and attach data to them.</li>
      <li>We augment interactive techniques in modern vector design tools for direct manipulation of visualization configurations and parameters.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3173697">paper</a></li>
      <li><a href="https://youtu.be/cjX9QA7fC0s">short demo</a></li>
      <li><a href="https://vimeo.com/234587002">long demo</a></li>
      <li><a href="http://www.zcliu.org/di/">project</a></li>
      <li><a href="http://data-illustrator.com/app/index.html">app</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="http://www.zcliu.org/di/di2.png">
  </div>
</div>

<!--
  CVPR 2017
-->
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

<!--
  CVPRW 2017
-->
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

<!--
  SIGGRAPH 2017
-->
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

<!--
  CHI 2017
-->
---
### CHI 2017
+++
#### MakerWear: A Tangible Approach to Interactive Wearable Creation for Children
###### Majeed Kazemitabaar, Jason McPeak, Alexander Jiao, Liang He, Thomas Outing, Jon E. Froehlich
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We introduce <i>MakerWear</i>, a new wearable construcion kit for young children that use a tangible, 'plug-and-play' approach to wearable creation. MakerWear is comprised of two parts: (i) single-function, electronic modules and (ii) a flexible, magnetic socket mesh. Our findings reveal how children engage in wearable design, what they make (and want to make), and what challenges they face. We also explore age-related differences.
    <br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>the MakerWear system, including the 'plug-and-play' modules and custom socket design, which dramatically lowers barriers to wearable design</li>
      <li>findings from pilot studies and single- and multi-session workshops characterizing how children engage in wearable design, what they make, and the challeges therein</li>
      <li>an analysis of age-related differences in MakerWear creation and understanding</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025887">paper</a></li>
      <li><a href="https://www.youtube.com/watch?v=14Fa_VOJHIA">demo</a></li>
      <li><a href="https://youtu.be/8t6du1RDDD4">presentation video</a></li>
      <li><a href="http://lianghe.me/makerwear.html">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="http://lianghe.me/images/makerwear/fig1.png">
    <img width="100%" src="http://lianghe.me/images/makerwear/fig3.png">
    <img width="100%" src="http://lianghe.me/images/makerwear/fig2.png">
  </div>
</div>

+++
#### Organic Primitives: Synthesis and Design of pH-Reactive Materials using Molecular I/O for Sensing, Actuation, and Interaction
###### Viirj Kan, Emma Vargo, Noa Machover, Hiroshi Ishii, Serena Pan, Weixuan Chen, Yasuaki Kakehi
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We present <i>Organic Primitives</i>, an toolbox that consists of color, odor and shape changing material primitives that sense contents within fluids and convert them into sensory information. The scope of this paper focuses on sensing pH in fluid as a starting point, with the goal of developing a model methodology for future sensor-actuator development.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>We present methods for how we bring these liquid-state pH reaction mechanisms into solid-state material primitives in order to be used as sensor-actuators for HCI.</li>
      <li>We evaluated the individual output properties of our primitives within this toolbox to exhibit the human-readable rate, range, and reversibility of the changes as a function of pH 2 to 10.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025952">paper</a></li>
      <li><a href="https://youtu.be/z4SuP2RLOoI">demo</a></li>
      <li><a href="https://www.viirj.com/organic-primitives-project/">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://static1.squarespace.com/static/582042e42e69cf3e25f992fe/t/59d2b9688419c2d11fa40384/1506982331122/viirj-semiotics.png">
  </div>
</div>

+++
#### Explaining the Gap: Visualizing One's Predictions Improves Recall and Comprehension of Data
###### Yea-Suel Kim, Katharina Reinecke, Jessica Hullman
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We present multiple graphically-based techniques for eliciting and incorporating a user's prior knowledge about data into visualization interaction. We observed that providing opportunities for users to interact with their prior knowledge improves recall of data values, and is more powerful when used with visualization than with text. Our findings pave the way for a new paradigm of interactive visualization that enables users to interact with their internal representations to deepen their understanding of data.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>a set of novel elicitation techniques for eliciting users' prior knowledge in visualization interaction; (1) Prompting a user to generate self-explanations of the observed data, (2) Prompting a user to predict the data before seeing it, (3) Providing the user with feedback on her predition</li>
      <li>a controlled experiment to test the effect of these techniques on recall and comprehension of data</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025592">paper</a></li>
      <li><a href="https://youtu.be/UfX23bmgM5E">demo</a></li>
      <li><a href="https://youtu.be/m-Iyi-fFX0k">presentation video</a></li>
      <li><a href="https://medium.com/hci-design-at-uw/explaining-the-gap-visualizing-ones-predictions-improves-recall-and-comprehension-of-data-ec848d5861d9">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://cdn-images-1.medium.com/max/1200/0*uo20g3jspjjM9k1t.">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/3c12818c5a714044e1f9a0d26636b53b7c7831ce/3-Figure1-1.png">
  </div>
</div>

+++
#### Stories from Survivors: Privacy & Security Practices when Coping with Intimate Partner Abuse
###### Tara Matthews, Kathleen O'Leary, Anna Turner, Manya Sleeper, Jill Palzkill Woelfer, Martin Shelton, Cori Manthorne, Elizabeth F. Churchill, Sunny Consolvo
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We present a qualitative study of the digital privacy and security motivations, practices, and challenges of a specific population facing higher levels of risk in their daily lives: survivors of intimate partner abuse (IPA). Our research questions are "What role has digital provacy and security played in the experiences that survivors of IPA have with their abusers?", "What are IPA survivors' motivations, practices, and challenges when protecting their privacy and security online and on their devices?", and "What technology design implications do the digital privacy and security challenges faced by survivors of IPA suggest?" Results of our study were used to develop a framework organizing suvivor technology practices and challenges into three-phases of intimate partner abuse: physical control, escape, and life apart.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>a three-phase framework for organizing suvivors' techonology practices and challenges. This framework provides rmpirically sound, foundational guidance for technology creators to consier how new and existing technologies may be designed to help survivors of IPA.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025875">paper</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/1c0852f8658c2e63320008a3fcb44c3dcdac2036/5-Figure1-1.png">
  </div>
</div>

+++
#### Empowered Participation: Exploring How Citizens Use Technology in Local Governance
###### Sheena Erete, Jennifer O. Burrell
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We examine the research question: <i>How do ICTs affect political engagement and interactions with city officials around crime prevention in diverse neighbothoods?</i> In this paper, we describe how citizens use ICTs to influence local policy, particularly amoung law enforcement and local government officials.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>Our findings provide insignts into the usage of ICTs to support local governance for crime prevention, extending prior HCI research focused on the use of technology to support local engagement.</li>
      <li>Our results add to the conversation that technology alone cannot equitably empower citizens to solve deep-seated social problems such as crime without addressing the underlying inequities across communities.</li>
      <li>Our study builds on prior work in HCI that provides insights into designing for traditionally marginalized groups.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025996">paper</a></li>
      <li><a href="https://youtu.be/ggf31o5Ync0">presentation</a></li>
    </ul><br>
  </div>
  <div class="col">
  </div>
</div>

+++
#### What Can Be Predicted from Six Seconds of Driver Glances?
###### Lex Fridman, Heishiro Toyoda, Sean Seaman, Bobbie Seppelt, Linda Angell, Joonbum Lee, Bruce Mehler, Bryan Reimer
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We consider a large dataset of real-world, on-road driving from a 100-car naturalistic study to explore the predictive power of driver glances and, specifically, to answer the following question: what can be predicted about the state of the driver and the state of the driving environment from a 6-second sequence of macro-glances?<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>Just 6 seconds of coarse driver gaze regions can be used to predict a lot of things about the driver, the car, and the driving environment.</li>
      <li>Drive gaze has been used to predict attention allocation, but not to predict everything else. We try to just that for the first time and show when it works and when it doesn't.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025929">paper</a></li>
      <li><a href="https://youtu.be/FKRuxvm6HlA">presentation</a></li>
    </ul><br>
  </div>
  <div class="col">
    <iframe width="100%" height="100%" src="https://www.youtube.com/embed/FKRuxvm6HlA" frameborder="0"></iframe>  </div>
</div>

+++
#### Designing Gamified Applications that Make Safe Driving More Engaging
###### Fabius Steinberger, Ronald Schroeter, Marcus Foth, Daniel Johnson
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    The research aim was to study how to design gamiied applications that make safe driving more engaging. To address this research aim, we present a user study, our interative design process, and two prototype evaluations. We discussed how the six design lenses data, presentation, time, interface, social context and road conditions are useful to bring into focus user needs and contextual requirements throughout the entire design process.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>We offer six lenses through which to view the design of gamified driving applications.</li>
      <li>We present new empirical data from a user study and ten design recommendations derived from it.</li>
      <li>Through two prototype evaluations, we show how these lenses and recommendations can help to implement concrete applications that successfully increase task engagement.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025511">paper</a></li>
      <li><a href="https://youtu.be/VGmotlIIIeU">presentation</a></li>
    </ul><br>
  </div>
  <div class="col">
    <iframe width="100%" height="100%" src="https://www.youtube.com/embed/VGmotlIIIeU" frameborder="0"></iframe>
  </div>
</div>

+++
#### Modelling Learning of New Keyboard Layouts
###### JUssi P.P. Jokinen, Sayan Sarcar, Antti Oulasvirta, Chaklam Silpasuwanchai, Zhenxin Wang, Xiangshi Ren
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    Predicting how users learn new or changed interfaces is a long-standing objective in HCI research. This paper contributes to understanding of visual search and learning in text entry. This paper presents a model of positional learning for keyboards.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>Our model clarifies the problem by operationalising layout learning and relearning as a dynamic system consisting of visual search, visual short-term memory, long-term memory, and utility learning.</li>
      <li>The model can assist designers and decisionmakers by predicting 1) how changes in layouts influence relearning times; 2) that large changes in layouts are possible when some maximum acceptable relearning cost is assumed; and 3) how to change one layout into another subtly.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025580">paper</a></li>
      <li><a href="https://youtu.be/t8YbiCRsf5M">presentation</a></li>
      <li><a href="https://youtu.be/Zvm50g1YU7c">demo</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="http://userinterfaces.aalto.fi/wp-content/uploads/learning.png">
  </div>
</div>

+++
#### Kinecting with Orangutans: Zoo Visitors' Empathetic Responses to Animals? Use Interactive Technology
###### Sarah Webber, Marcus Carter, Sally Sherwen, Wally Smith, Zaher Joukhadar, Frank Vetere
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    To better understand the forms of empathy experienced by people observing animal-computer interaction, we designed and studied an interactive installation for orangutans at a zoo. We deployed a prototype installation, and observed and interviewed visitors who watched orangutans use the installation. Analysis of observations and interviews revealed that visitors responded with cognitive, affective and motor empathy for the animals.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>This paper contributes new evidence and understanding of people's empathetic responses to observing animal-computer interaction and confirms the value of designing for empathy in its various forms.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?doid=3025453.3025729">paper</a></li>
      <li><a href="https://youtu.be/Iu03LNciKL8">demo</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/0216ea56ae8764bc5bc632a3c1dde1135ea9473a/8-Figure3-1.png">
  </div>
</div>

+++
#### Fingertip Tactile Devices for Virtual Object Manipulation and Exploration
###### Samuel B. Schorr, Allison M. Okamura
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    One of the main barriers to immersivity during object manipulation in virtual reality is the lack of realisitc haptic feedback. Our new devices have 3 purely translational degrees of freedom, making them particularly well suited for rendering forces that act in multiple directions during object manipulation, such as weight, friction, and stiffness.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>We developed fingertip devices to investigate how cutaneous skin deformation could contribute to a compelling, immersive haptics experience for virtual reality without bulk of trasitional kinesthetic haptic devices.</li>
      <li>We show how naive users perceive changes of a virtual object's physical properties when we use skin deformation to render objects with varying mass, friction, and stiffness.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025744">paper</a></li>
      <li><a href="https://youtu.be/LKMndCEr4Mw">demo</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="70%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/ea5fe0b6fd7b2c8158f48c72f44a381ab25d953a/2-Figure1-1.png">
    <img width="70%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/ea5fe0b6fd7b2c8158f48c72f44a381ab25d953a/2-Figure2-1.png">
  </div>
</div>

+++
#### Supporting Expressive Procedural Art Creation through Direct Manipulation
###### Jannifer Jacobs, Sumit Gogia, Radmir Mech, Joel Brandt
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    Contrasting the creative opportunities of procedural art with the challenges of programming raises our research question: <i>Can we support accessible and expressive procedural art by enabling people to describe procedural relationships through direct manipulation?</i> Our approach is to augment the conventions of graphic art software to support the creation and modification of procedural relationships exclusively through manipulation of concrete artwork. We developed Para, a digital illustration tool that supports the creation of declarative constraints in vector artwork.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>We introduce Para, a new direct-manipulation tool that supports procedural art through live, non-linerar, and continuous manipulation.</li>
      <li>We demonstrate core declarative procedural operations that can be expressed through direct manipulation, are easy to use, and enable diverse creative outcomes.</li>
      <li>We provide evidence for how the direct manipulation of procedural relationships can extend manual practice through two open-ended studies.</li>
      <li>We provide recommendations for building expressive direct manipulation procedural tools, as gleaned from evaluation.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025927">paper</a></li>
      <li><a href="https://youtu.be/-slflVG4wUQ">short demo</a></li>
      <li><a href="https://vimeo.com/142400876">long demo</a></li>
      <li><a href="https://www.media.mit.edu/projects/active-drawing/overview/">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://i.vimeocdn.com/video/552359086.jpg?mw=700&mh=426">
    <img width="70%" src="https://dam-prod.media.mit.edu/thumb/2017/04/04/floral.jpg.1400x1400.jpg">
  </div>
</div>

+++
#### Illumination Aesthetics: Light as a Creative Material within Computational Design
###### Cesar Torres, Jasper O'Leary, Molly Nicholas, Eric Paulos
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    <i>Light as a first class creative material</i> has been largely ignored within the design of our electronic objects. Our work expands the illumination design space by treating light as a physical materials. We introduce a digital design tool that simulates and visualizes physical light interactions with a variety of materials for creating custom luminaires. We further develop a computational design and fabrication process for creating custom secondary optics elements (SOEs), which provides additional handles for users to physically shape and redirect light to compose, fill, and evenly diffuse planar and volumetric geometries.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>A novel and accessible luminaire design tool for use by non-expert electronic designers to visually design, simulate, and fabricate non-trivial illumination within physical objects.</li>
      <li>A computational design pipeline comprising the entire physical, electronic, and optical design of materials necessary to fabricate and realize the final desired luminaire.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025466">paper</a></li>
      <li><a href="https://youtu.be/tcaZyJqJElw">demo</a></li>
      <li><a href="http://www.hybrid-ecologies.org/projects/20-illumination-aesthetics">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/7dfd29c02f2f1a3484a6f07e1eddb9867f57d640/2-Figure2-1.png">
    <img width="100%" src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/7dfd29c02f2f1a3484a6f07e1eddb9867f57d640/9-Figure9-1.png">
  </div>
</div>

+++
#### ShareVR: Enabling Co-Located Experiences for Virtual Reality between HMD and Non-HMD Users
###### Jan Gugenheimer, Evgeny Stemasov, Julian Frommel, Enrico Rukzio
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    Current VR systems focus mainly on increasing the immersion and enjoyment for the user wearing the HMD (HMD user), resulting in all the bystanders (Non-HMD users) being excluded from the experience. We propose ShareVR, a proof-of-concept prototype enabling Non-HMD users to be part of the VR experience and interact with the HMD user and the virtual environment. We use a tracked display and a floor projection to visualize the virtual space for the Non-HMD user and potential bystanders.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>Concept, design and implementation of ShareVR - a proof-of-concept prototype for co-located asymmetric experiences in VR, based on the feedback of VR early adopters.</li>
      <li>Insignts from a user study, exploring the impact of ShareVR on enjoyment, presence and social interaction and showing its advantage compared to a baseline consisting of a gamepad and television.</li>
      <li>Exploration of the design space for co-located asymmetric VR experiences and implementation of three example applications, giving insights for designers of future asymmetric co-located VR experiences.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://dl.acm.org/citation.cfm?id=3025683">paper</a></li>
      <li><a href="https://youtu.be/cQxArK3Bu9M">short demo</a></li>
      <li><a href="https://youtu.be/Uc5fkTFMHr4">long demo</a></li>
      <li><a href="https://www.uni-ulm.de/in/mi/mi-forschung/uulm-hci/projects/sharevr-enabling-co-located-experiences-for-virtual-reality-between-hmd-and-non-hmd-users/">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="https://i.ytimg.com/vi/Uc5fkTFMHr4/maxresdefault.jpg">
    <img width="100%" src="https://i.ytimg.com/vi/cQxArK3Bu9M/maxresdefault.jpg">
  </div>
</div>

<!--
  arXiv 2017
-->
---
### arXiv 2017
+++
#### Large-scale, Fast and Accurate Shot Boundary Detection through Spatio-temporal Convolutional Neural Networks
###### Ahmed Hassanien, Mohamed Elgharib, Ahmed Selim, Sung-Ho Bae, Mohamed Hefeeda, Wojciech Matusik
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We present a SBD technique based on spatio-temporal Convolutional Neural Networks (CNN). We are the first to present a very large SBD dataset that allows deep neural networks techniques to be effectively applied.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>The first CNN SBD technique. We outperform dissolve gradual detection, generate competitive performance for sharp detections and produce significant improvement in wipes. In addition, we are up to 11 times faster than the state of the art.</li>
      <li>Introduction of a new very large SBD dataset for training an accurate CNN model. Our dataset contains 3.5 million frames of synthetic transitions and 70,000 frames of hard negative no-transitions.</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://cfg.mit.edu/sites/cfg.mit.edu/files/large_scale_shot_boundary_detection.pdf">paper</a></li>
      <li><a href="http://ds.qcri.org/projects/deepsbd/">project</a></li>
      <li><a href="https://github.com/melgharib/DSBD">code</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="">
    <img width="100%" src="">
    <img width="100%" src="">
  </div>
</div>


<!--
  CVPR 2016
-->
---
### CVPR 2016
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


<!--
  ECCV 2016
-->
---
### ECCV 2016
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

<!--
  ICCV 2015
-->
---
### ICCV 2015

+++
#### Learning Spatiotemporal Features with 3D Convolutional Networks
###### Du Tran, Lubomir Bourdev, Rob Fergus, Lorenzo Torresani, Manohar Paluri
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We propose a simple, yet effective approach for spatiotemporal feature learning using deep 3-dimentional convolution networks (3D ConvNets) trained on a large scale supervised dataset.<br>
    <u><b>Contribution</b></u><br>
    <ul>
      <li>3D ConvNets are more suitable for spatiotemporal feature learning compared to 2D ConvNets</li>
      <li>A homogeneous architecture with small 3x3x3 convolution kernels in all layers is among the best performing architectures for 3D ConvNets</li>
      <li>Our learned features, namely C3D (Convolutional 3D), with a simple linear classifier outperform state-of-the-art methods</li>
    </ul><br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://ieeexplore.ieee.org/document/7410867/">paper</a></li>
      <li><a href="http://vlg.cs.dartmouth.edu/c3d/">project</a></li>
      <li><a href="https://pdfs.semanticscholar.org/1c30/bb689a40a895bd089e55e0cad746e343d1e2.pdf">slide 1</a></li>
      <li><a href="https://pdfs.semanticscholar.org/62d2/a378c729c5e6e32631ccd0eadb30a7180aaf.pdf">slide 2</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="http://www.cs.dartmouth.edu/~dutran/images/c3d.jpg">
    <img width="100%" src="https://www.researchgate.net/profile/Tu_Phuong2/publication/319277488/figure/fig1/AS:544953893912576@1506938541233/2D-and-3D-convolution-operations-applied-to-multiple-frames-a-2D-convolution-results-in.png">
  </div>
</div>

---
### Database of Databse
+++
#### UCF101
###### Khurram Soomro, Amir Roshan Zamir, Mubarak Shah
<div class="container">
  <div class="col">
    UCF101 is an action recognition dataset of realistic action videos, collected from YouTube, having 101 action categories. The action categories can be divided into five types: 1) Human-Object Interaction 2) Body-Motion Only 3) Human-Human Interaction 4) Playing Musical Instruments 5) Sports. UCF101 contains 13,320 videos from 101 action categories.<br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="http://crcv.ucf.edu/data/UCF101.php">project</a></li>
      <li><a href="https://arxiv.org/abs/1212.0402">paper</a></li>
    </ul><br>
  </div>
  <div class="col">
  </div>
</div>

+++
#### Sports-1M
###### Andrej Karpathy, George Toderici, Sanketh Shetty, Thomas Leung, Rahul Sukthankar, Li Fei-Fei
<div class="container">
  <div class="col">
    Sports-1M dataset is licensed under Creative Commons 3.0 and contains 1,133,158 video URLs which have been annotated automatically with 487 Sports Labels using the YouTube Topics API.<br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://cs.stanford.edu/people/karpathy/deepvideo/">project</a></li>
      <li><a href="https://github.com/gtoderici/sports-1m-dataset/blob/wiki/ProjectHome.md">github</a></li>
    </ul><br>
  </div>
  <div class="col">
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
    <img width="100%" src="">
  </div>
</div>