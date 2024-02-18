   All data structures in Open3D are compatible with NumPy. The following tutorial uses NumPy to generate a variant of a synchronization function and visualizes the function using Open3D. First, an n × 3 matrix is generated. Each column is composed of, and the relationship with: In the code, refers to the normalized map in the interval [0,1]. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574485928
  ```  
#  First, from NumPy to open3d. PointCloud 

   The Vector3dVector function in Open3d can directly convert a NumPy matrix into point cloud data of type open3d. PointCloud.points. In this way, all similar data structures such as open3d. PointCloud.colors or open3d. PointCloud.normals can be directly assigned or modified using NumPy. The following code saves the point cloud in ply format for future use. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574485928
  ```  
#  Switch from open3d. PointCloud to NumPy 

   pcd_load points of Vector3dVector type can be directly converted to NumPy arrays via np.asarrays. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574485928
  ```  
##  1. Visualize the results 

 ![avatar]( 20200915194933328.png) 

##  2. Main functions 

 1. X = np.linspace (-3, 3, 100) np.linspace () Returns evenly spaced numbers within the specified interval. 

 2, mesh_x, mesh_y = np.meshgrid (x, x) meshgrid () generates grid point coordinate matrix. 

 3, xyz [:, 0] = np.reshape (mesh_x, -1) reshape (; -1) reshape () provides a new shape for the array without changing the array data. 

##  3. Reference link 

 Working with NumPy 

#  Generate random point clouds 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574485928
  ```  
#  IV. Display of results 

 ![avatar]( 15491aa57cec40139639caa3fca21887.png) 

