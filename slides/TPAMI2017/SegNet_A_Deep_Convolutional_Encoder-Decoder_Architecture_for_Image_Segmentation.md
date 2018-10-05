#### SegNet: A Deep Convolutional Encoder-Decoder Architecture for Image Segmentation
###### Vijay Badrinarayanan, Alex Kendall, Roberto Cipolla

@div[left]

__概要__<br>
Semantic Segmentationを行うEcoder-Decoder構造のCNN（SegNet）を提案した。SegNetのEncoderとDecoderは対称的な構造を取っており、DecoderのUpsamplingにおいて、対応するEncoderのMax Pooling層で選択されたピクセルのインデックス情報を用いる。この手法は、(1)より位置が正確で、(2)学習パラメータが少なく、(3)あらゆるEncoder-Decoder構造のネットワーク適用可能である。またSegNetはstate-of-the-artと同等の精度を出した。<br>
<br>
__手法・新規性__<br>
SegNetのEncoderはVGG16のFC層を除いたもので構成されており、DecoderはEncoderに対応するように対称的な構造を持っている。非常に類似した構造を持つネットワークとしてU-NetやDeconvNetが挙げられるが、U-NetではEncoderの特徴量を保持しておかなければいけなく、DeconvNetではUpsampling時にDeconvolutionを行うためパラメータ数が多くなってしまう。一方で、SegNetのDecoderのUpsamplingでは、それぞれのDecoderに対応するEncoderのMax Pooling層で選択されたインデックスに基づいて非線形のUpsamplingを行うため、省メモリであり、かつ学習パラメータも少なくすることができる。<br>

@divend

@div[right]

![](assets/img/SegNet_A_Deep_Convolutional_Encoder-Decoder_Architecture_for_Image_Segmentation.png =full)<br>
<br>

__リンク__<br>
・[論文](https://arxiv.org/pdf/1511.00561.pdf)<br>
・[プロジェクト](http://mi.eng.cam.ac.uk/projects/segnet/)<br>
・[ポスター](http://mi.eng.cam.ac.uk/projects/segnet/images/segnet_poster.png)
・[GitHub](https://github.com/alexgkendall/caffe-segnet)

@divend