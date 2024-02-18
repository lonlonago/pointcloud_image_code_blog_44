#  First, the principle of the algorithm 

##  1. Algorithm overview 

   Laser scanning usually produces point cloud datasets with uneven density. In addition, errors in measurement can also produce sparse outliers. At this time, the calculation of local point cloud characteristics (such as normal vector or curvature change rate at the sampling point) is complicated, which will lead to wrong values, which in turn will lead to later processing failures such as point cloud registration. Statistical filters are used to remove obvious outliers. Outliers are often introduced by measurement noise, which is characterized by sparse distribution in space. It can be understood as: each point expresses a certain amount of information. The denser the points in a certain area, the greater the amount of information may be. Noise information is useless information and the amount of information is small. Therefore, the information expressed by outliers can be ignored. Taking into account the characteristics of outliers, it is possible to define a point cloud that is less than a certain density, i.e. the point cloud is invalid. Calculate the average distance from each point to its nearest (set) point. Then the distance between points in the point cloud should form a Gaussian distribution. Given the mean and variance, points can be excluded. 

##  2. Calculation process 

   Statistical analysis of the neighborhood of each point assumes that the distances of the points in the point cloud constitute a Gaussian distribution, the shape of which is determined by the mean and standard deviation. Let the coordinates of the first point in the point cloud be, and the distance from that point to any point is: Calculate the mean of the distance between each point traversed to any point as follows: Standard deviation is:  

   Let the standard deviation multiple be that only input is required during the implementation of the algorithm, and two thresholds are required. When a point is close and the average distance of points is within the standard range, the point is retained, and if it is not within the range, it is defined as outlier deletion. 

 ![avatar]( 88e401e5602d43d19f3c796dfea6043d.png) 

##  3. References 

>  [1] R.B. Rusu, Z.C. Marton, N. Blodow, M. Dolha, and M. Beetz. Towards 3D Point Cloud Based Object Maps for Household Environments Robotics and Autonomous Systems Journal (Special Issue on Semantic Knowledge), 2008. [2] Han Dongsheng, Xu Maolin, Jin Yuanhang. Filtering and Accuracy Analysis of Multi-source Heterogeneous Point Cloud Registration Data [J]. Journal of Mapping Science and Technology, 2020, 37 (05): 503-508. 

##  4. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574419546
  ```  
   remove_statistical_outlier function computes the average distance from each point to all nearby points (assuming the result is a Gaussian distribution whose shape is determined by the mean and standard deviation), then points whose average distance is outside the standard range can be defined as outliers and removed from the data. It has two input parameters: 

##  5. Algorithm source code 

 Yes, you read that right!!! Open3D source code is C++. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574419546
  ```  
#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574419546
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( 20210227102738623.png) 

##  2. The filtered point cloud 

 ![avatar]( 20210227102731150.png) 

