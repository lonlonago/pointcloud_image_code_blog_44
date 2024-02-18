#  The loss function 

##  1. About ICP 

   The ICP algorithm is designed to estimate rigid transformations that, given a prior transformation, best align the source point cloud with the target point cloud. The outlier filtering phase of ICP is strongly associated with error minimization. The former reduces the impact of erroneous data associations, while the latter finds solutions that respect the constraints of the previous phase. In the context of ICP, the two phases can be summarized as estimating rigid transformations by minimizing the objective function (1). Where is the cost function. The error function is the proportional distance between matching points, where and, which is equivalent to the simplified version of the Mahalanobis distance, the scale is consistent across all dimensions. For the original version of ICP, the value of is set to 1. 

   The double summation of Equation 3 is expensive to compute, and is usually approximated using a subset of pairs, using the nearest neighbor of each. To simplify the notation, use the representation to minimize the error of each corresponding pair of points, which is the index of this subset. Since it is non-convex, it must be solved iteratively in a manner similar to iterative reweighted least squares (IRLS) by decomposing into weight and squared error terms to minimize, 

   In each iteration, the previous transformation is assigned to the last estimated transformation until it converges.

##  2, loss function 

 ![avatar]( 20210716210413402.png) 

   In summary, the so-called robust loss function of the ICP algorithm of various optimization improvements, the essence of which is to improve the expression of formula (3). Figure 1 shows a list of commonly used outlier culling functions, with a dedicated column highlighting their implementation.  

##  3. Open3D implementation 

   At present, the improved ICP algorithm optimized by the robust kernel function only provides an implementation interface for PointToPlane ICP. registration_icp can be called with the parameter TransformationEstimationPointToPlane (loss). Inside the TransformationEstimationPointToPlane (loss), a weighted residual and Jacobian matrix of the point-to-plane ICP target are calculated according to the provided robust kernel. Where loss is a given loss function (also known as the robust kernel function), which has the following forms: CauchyLoss, GMLoss, HuberLoss, L1Loss, L2Loss, TukeyLoss. Here, taking the L2Loss function as an example, the calling method is given: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574422787
  ```  
   I will explain the algorithm principles and implementation methods of each function one by one in the follow-up blog. 

#  Code implementation 

 This code only uses the L2Loss function as an example. Note: Although the code of the Open3D point-to-surface ICP registration algorithm is similar, the principle is very different. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574422787
  ```  
#  III. Display of results 

 ![avatar]( 20210716212536516.png) 

