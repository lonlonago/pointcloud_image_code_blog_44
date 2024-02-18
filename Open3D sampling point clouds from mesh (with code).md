#  First, uniform sampling 

   Open3D includes the ability to extract point clouds from triangular meshes. The easiest way is to sample_points_uniformly extract points uniformly from a 3D surface based on the triangular area. Parameters number_of_points define the number of points sampled from the triangular surface. 

##  sample code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957441175
  ```  
 ![avatar]( 20201203203210459.png) 

  uniform sampling result  

#  Second, Poisson sampling 

   Uniform sampling can obtain point clusters on the surface. Poisson disk sampling can make the sampling points evenly distributed. sample_points_poisson_disk implemented this function. Therefore, the algorithm starts with a sampled point cloud and removes points to meet the sampling criteria. This algorithm supports the selection of two initial point clouds. 

 1. Default parameter init_factor: First, sample the point cloud evenly from the grid by init_factor x number_of_points, and then eliminate it. 2. Provide a point cloud data directly to the sample_points_poisson_disk function, and then eliminate the point cloud. 

##  sample code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957441175
  ```  
 ![avatar]( 20201203203823286.png) 

#  CloudCompare 

 ![avatar]( 20201229090900935.gif) 

