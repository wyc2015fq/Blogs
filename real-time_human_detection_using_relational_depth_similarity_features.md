# Real-Time Human Detection using Relational Depth Similarity Features







 Human occlusions

 Complex backgrounds

 Real-time processing because of the use of the raster scanning while varying the window scale


 Divide depth image into local regions with cell of size 8*8 pixels
 Compute depth histograms from the depth information
 Normalize the histograms so that the total value of each depth histogram is 1

 Compute the similarity of two depth histograms using equation below




















 Comparison of three feature extraction methods:





 Comparison of occlusion and non-occlusion adjustment feature extraction methods:



