# Survey Slides
### Takahiro Itazuri (Waseda University)

<!--
  CHI 2018
-->
---
### CHI 2018

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
    <img width="100%" src="http://web.media.mit.edu/~jacobsj/images/dynamic_brushes/dynamic_brushes.003.png">
  </div>
</div>

+++
#### Voice Interfaces in Everyday Life
###### Martin Porcheron, Joel E. Fischer, Stuart Reeves, Sarah Sharples
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

+++
#### Data Illustrator: Augumenting Vector Design Tools with Lazy Data Binding for Expressive Visualization Authoring
###### Zhicheng Liu, John Thompson, Alan Wilson, Mira Dontcheva, James Delorey, Sam Grigg, Bernard Kerr, John Stasko
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
    We present a qualitative study of the digital privacy and security motivations, practices, and challenges of a specific population facing higher levels of risk in their daily lives: survivors of intimate partner abuse (IPA). Results of our study were used to develop a framewor organizing suvivor technology practices and challenges into three-phases of intimate partner abuse: physical control, escape, and life apart.<br>
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
    <img width="100%" src="">
    <img width="100%" src="">
    <img width="100%" src="">
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