# Real-Time Human Detection using Relational Depth Similarity Features







 Human occlusions

 Complex backgrounds

 Real-time processing because of the use of the raster scanning while varying the window scale


 Divide depth image into local regions with cell of size 8*8 pixels
 Compute depth histograms from the depth information
 Normalize the histograms so that the total value of each depth histogram is 1

![equation1](https://raw.githubusercontent.com/stdcoutzyx/Blogs/master/papers/imgs/3-1.png)
 Compute the similarity of two depth histograms using equation below
















![equation1](https://raw.githubusercontent.com/stdcoutzyx/Blogs/master/papers/imgs/3-3.png)





	
![equation1](https://raw.githubusercontent.com/stdcoutzyx/Blogs/master/papers/imgs/3-5.png) 



 Define occlusion: any object region that is closer to the camera than the detection window

 Extraction of occlusion regions:


 Calculate the proportion of occlusion regions:


 Combine the rate OR into the Adaboost algorithm:





 Comparison of three feature extraction methods:





 Comparison of occlusion and non-occlusion adjustment feature extraction methods:



