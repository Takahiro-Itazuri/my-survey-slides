#### Tracking Multiple Objects Outside the Line of Sight Using Speckle Imaging
###### Brandon M. Smith, Matthew O'Toole, Mohit Gupta

@div[left]

__概要__<br>
スペックル・イメージングを利用して見えていない（non-line-of-sight: NLOS）複数の物体を追跡する手法を提案した論文。安価なコストで角付近に存在する複数の物体を10マイクロメートル程度の精度で追跡可能にした。拡散反射する壁を通して間接的にしかセンシングできない環境において、スペックル・イメージングの方法と動きのモデルを提案した。<br>
<br>
__手法・新規性__<br>
スペックルとはコヒーレント光が荒い表面で反射した際に発生する高周波なノイズのような画像である。提案手法では、このスペックルの動きと実際の物体の動きの関係をモデル化することで、拡散反射する壁から得られる情報から物体追跡を行う。実際には参照画像とそこから物体が移動したことで得られた画像の相関を取り、ピークを得ることで、物体の移動量を得る。<br>

@divend

@div[right]

![](assets/img/Tracking_Multiple_Objects_Outside_the_Line_of_Sight_Using_Speckle_Imaging.png =full)<br>
<br>

__リンク__<br>
・[論文](http://openaccess.thecvf.com/content_cvpr_2018/papers/Smith_Tracking_Multiple_Objects_CVPR_2018_paper.pdf)<br>
・[デモ](https://youtu.be/FVHcNEipnLU)<br>

@divend