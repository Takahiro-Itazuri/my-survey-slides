#### Context-aware Deep Feature Compression for High-speed Visual Tracking
###### Jongwon Choi, Hyung Jin Chang, Tobias Fischer, Sangdoo Yun, Kyuewang Lee, Jiyeoup Jeong, Yiannis Demiris, Jin Young Choi
<div class="container">
  <div class="col">
    <u><b>Abstract</b></u><br>
    We propose a new context-aware correlation filter based tracking framework to achieve high computational speed and state-of-the-art performance amoung real-time trackers. The major contribution to the high computational speed lies in the proposed deep feature compression that is achieved by a context-aware scheme utilizing multiple expert auto-encoders: a context in our framework refers to the coarse category of the tracking target according to appearance patterns. In the pre-training phase, one expert auto-encoder is trained per category. In the tracking phase, the best expert auto-encoder is selected for a given target, and only this auto-encoder is used. To achiece high tracking performance with the compressed feature map, we introduce extrinsic denoising process and a new orthogonality loss term for pre-train and fine-tuning of the expert auto-encoders.<br>
    <u><b>Links</b></u><br>
    <ul>
      <li><a href="https://arxiv.org/pdf/1803.10537.pdf">paper</a></li>
    </ul><br>
  </div>
  <div class="col">
    <img width="100%" src="http://pil.snu.ac.kr/upload/traca20180302120104318.PNG">
  </div>
</div>