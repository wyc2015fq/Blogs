# Face recognition using Histograms of Oriented Gradients

 Extract Hog descriptors from a regular grid.

 Fusion of HOG descriptors at different scales allows to capture important structure
 Dimensionality reduction is necessary to make the classification less prone to over-fitting.

 Eigenfaces( Principal Component Analysis)
 Gabor wavelets
 Local Binary Patterns
 Error-Correcting Output Codes
 Independent Component Analysis

 Scale-space extrema detection. (achieve scale invariance)
 Orientation assignment. (find the dominant gradient orientation)
 Descriptor extraction.

 In the 2008 paper, faces are previous normalized in scale and orientation, So the step for scale-space extrema detection were not necessary.
 A set of 25 facial landmarks were localizaed using Active Apperence Models(AAMs).
 Hog descriptors are extracted from the vicinity of each of these 25 landmarks.
 Using nearest neighbor and Enclidean distance to classify.

 Final error may crucially depend on the reliability of the landmark localizations, and the landmarks are not precisely due to occlusions, strong illuminations or pose changes.
 First normalize the face and then extract HOG features from a regular grid. The grid is formed by placing equal side patches around a first cell centered in the image, until the whole image is covered. 
 The paper hypothesize that a better result could be obtained by combining information from different patch sizes. And the paper considered a new fusion strategy that is the product combination of the classifiers at patch sizes.
 Several overlapping patches are used, so the final feature representation will be highly redundant, So dimensionality reduction is necessary.

 R individual classifications c_k (k=1,…,R), each one trained using Hog features with different patch sizes. Each classifier gives one input sample x_k a posterior probability vector:

![equation1](https://raw.githubusercontent.com/stdcoutzyx/Blogs/master/papers/imgs/4-1.png)

+ The product rule cosists of fusing the final decision as:


 Effect of the facial feature localization error on the final recognition performance. Large error on the localization of facial features leads to bad classification performance.
 Extracting regular grids and patch size combination

 [1]. Déniz O, Bueno G, Salido J, et al. Face recognition using histograms of oriented gradients[J]. Pattern Recognition Letters, 2011, 32(12): 1598-1603.