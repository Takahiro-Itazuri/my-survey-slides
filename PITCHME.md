# Survey Slides
### Takahiro Itazuri (Waseda University)

---
@title[test slide]
## two column slide
@div[left-50]
Left Column
@divend
@div[right-50]
Right Column
@divend

---
### CVPR 2018
+++?include=slides/CVPR2018/A_Twofold_Siamese_Network_for_Real-Time_Object_Tracking.md
+++?include=slides/CVPR2018/Context-aware_Deep_Feature_Compression_for_High-speed_Visual_Tracking.md
+++?include=slides/CVPR2018/End-to-End_Flow_Correlaion_Tracking_with_Spatial-temporal_Attention.md
+++?include=slides/CVPR2018/Learning_Spatial-Aware_Regressions_for_Visual_Tracking.md
+++?include=slides/CVPR2018/Learning_Spatial-Temporal_Regularized_Correlation_Filters_for_Visual_Tracking.md
+++?include=slides/CVPR2018/VITAL.md

---
### CHI 2018
+++?include=slides/CHI2018/Agile_3D_Sketching_with_Air_Scaffolding.md
+++?include=slides/CHI2018/Data_Illustrator.md
+++?include=slides/CHI2018/Examining_Wikipedia_With_a_Broader_Lens.md
+++?include=slides/CHI2018/Expressive_Time_Series_Querying_with_Human-Drawn_Scale-Free_Sketching.md
+++?include=slides/CHI2018/Extending_Manual_Drawing_Practices_with_Artist-Centric_Programming_Tools.md
+++?include=slides/CHI2018/From_Her_Story_to_Our_Story.md
+++?include=slides/CHI2018/HARK_No_More.md
+++?include=slides/CHI2018/Hoarding_and_Minimalism.md
+++?include=slides/CHI2018/Pinpointing.md
+++?include=slides/CHI2018/Voice_Interfaces_in_Everyday_Life.md
+++?include=slides/CHI2018/Wall++.md

---
### CVPR 2017

+++
#### End-To-End Representation Learning for Correlation Filter Based Tracking
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
      <li><a href="http://openaccess.thecvf.com/content_cvpr_2017/html/Valmadre_End-To-End_Representation_Learning_CVPR_2017_paper.html">paper</a></li>
      <li><a href="https://github.com/bertinetto/cfnet">code</a></li>
      <li><a href="https://www.robots.ox.ac.uk/~luca/cfnet.html">project</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="">
    <img width="100%" src="">
    <img width="100%" src="">
  </div>
</div>

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
### CVPRW 2017
+++?include=slides/CVPRW2017/Automatic_Curation_of_Golf_Highlighting_using_Multimodal_Excitement_Features.md

---
### SIGGRAPH 2017
<!--+++?include=slides/SIGGRAPH2017/VNect.md-->

---
### CHI 2017
+++?include=slides/CHI2017/Designing_Gamified_Applications_that_Make_Safe_Driving_More_Engaging.md
+++?include=slides/CHI2017/Empowered_Participation.md
+++?include=slides/CHI2017/Explaining_the_Gap.md
+++?include=slides/CHI2017/Fingertip_Tactile_Devices.md
+++?include=slides/CHI2017/Illumination_Aesthetics.md
+++?include=slides/CHI2017/Kinecting_with_Orangutans.md
+++?include=slides/CHI2017/MakerWear.md
+++?include=slides/CHI2017/Modelling_Learning_of_New_Keyboard_Layouts.md
+++?include=slides/CHI2017/Organic_Primitives.md
+++?include=slides/CHI2017/ShareVR.md
+++?include=slides/CHI2017/Stories_from_Survivors.md
+++?include=slides/CHI2017/Supporting_Expressive_Procedural_Art_Creation.md
+++?include=slides/CHI2017/What_Can_Be_Predicted_from_Six_Seconds_of_Drivers_Glances.md

---
### arXiv 2017
+++?include=slides/arXiv2017/Survey_of_Visual_Question_Answering.md

---
### CVPR 2016
+++
<!--+++?include=slides/CVPR2016/Rethinking_the_Inception_Architecture_for_Computer_Vision.md-->
+++include=slides/CVPR2016/Visual7W.md

---
### ECCV 2016
<!--+++?include=slides/ECCV2016/Video_Summarization_with_Long_Short-term_Memory.md-->

---
### ECCVW 2016
<!--+++?include=slides/ECCVW2016/Fully-Convolutional_Siamese_Networks_for_Object_Tracking.md-->

<!--
  ICCV 2015
-->
---
### ICCV 2015

<!--+++?include=slides/ICCV2015/SRDCF.md-->
+++?include=slides/ICCV2015/Learning_Spatialtemporal_Features_with_3D_Convolutional_Networks.md
+++?iclude=slides/ICCV2015/VQA.md

---
### NIPS 2015
+++include=slides/NIPS2015/mQA.md <!-- Are you talking to a machine ? -->
+++include=slides/NIPS2015/COCO-QA.md <!-- Exploring Models and Data for Image Question Answering -->

---
### TPAMI 2015
<!--+++?include=slides/TPAMI2015/High-Speed_Tracking_with_Kernelized_Correlation_Filters.md-->

---
### NIPS 2014
+++include=sldies/NIPS2014/A_Multi-World_Approach_to_Question_Answering_about_Real-World_Scenes_based_on_Uncertain_Input.md
+++include=slides/NIPS2014/Generative_Adversarial_Nets.md

---
### CVPR 2010
<!--+++?include=slides/CVPR2010/Visual_Object_Tracking_using_Adaptive_Correlation_Filters.md-->

---
### Database of Databse
+++?include=slides/Database/Sports-1M.md
+++?include=slides/Database/UCF101.md
