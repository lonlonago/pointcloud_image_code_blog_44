In many scenarios we want to generate dense 3D geometries, such as triangular meshes. However, we can only obtain unstructured point cloud data from multi-view stereo algorithms and depth sensors. We need to use surface reconstruction algorithms to obtain triangular meshes from unstructured inputs. Open3d implements existing algorithms in the literature: 

##  Alpha shapes 

 ![avatar]( gif.latex) 

 The alpha shape [Edelsbrunner1983] is a generalization of convex hulls. As introduced here, alpha shapes can be intuitively understood as the following: Imagine a huge ice cream containing chocolate chunks, which are points. With a spherical ice cream scoop, all parts of the ice cream can be dug out without touching the chocolate chunks, and even some holes can be dug inside (such as some parts that cannot be reached by moving the spoon externally.) We end up with an object bounded by caps, arcs, and points (not necessarily convex). If we draw all the round faces into triangles and line segments, we can visually describe the alpha shape of the point. 

 Open3D implements the algorithm with an interface create_from_point_cloud_alpha_shape which contains a weight parameter alpha. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574445206
  ```  
 ![avatar]( 20201209140601371.png) 

>  alpha-0.030 

 ![avatar]( 20201209140622947.png) 

  This algorithm is implemented based on the convex hull algorithm for point clouds. If we want to compute multiple alpha shapes from a given point cloud, we only need to compute the convex hull once and pass it to the create_from_point_cloud_alpha_shape, which saves some computation. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574445206
  ```  
>  alpha=0.500 

 ![avatar]( 20201209141045199.png) 

>  alpha=0.136 

 ![avatar]( 20201209141057885.png) 

>  alpha=0.037 

 ![avatar]( 20201209141112621.png) 

>  alpha=0.010 

 ![avatar]( 20201209141126197.png) 

##  Bowling method 

 A surface reconstruction algorithm related to alpha shape is the ball pivoting algorithm (BPA). Intuitively, we imagine a 3D ball of a given radius and place it on the point cloud data. If the ball hits three points (and doesn't return to those three points), then we create a triangle. After that, our ball starts rolling along the sides of the existing triangle, creating a triangle every time it hits three points that are not repeated. Open3d implements this algorithm in the interface create_from_point_cloud_ball_pivoting. The algorithm has an accepted list parameter radii, which creates several independent balls of different radii, which then start rolling on the point cloud. 

>  Attention: This algorithm requires the point cloud to contain normal parameters. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574445206
  ```  
 ![avatar]( 2020120914195053.png) 

 ![avatar]( 20201209141950122.png) 

##  Poisson surface reconstruction 

 The surface reconstruction algorithm produces unsmooth results because the points of the point cloud are also the vertices of the three-piece mesh. No modification is required. The Poisson surface reconstruction algorithm [Kazhdan 2006] solves the problem of regular optimization so that smooth surfaces can be produced. 

 Open3d implements the algorithm interface create_from_point_cloud_poisson, which is basically an encapsulation of the code interface implemented by Kazhdan. This interface has an important parameter depth, which defines the depth of the octree used for reconstruction. A higher depth value means that the mesh has high detail. 

>  Note: This algorithm requires the point cloud to contain normal information. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574445206
  ```  
>  downloading eagle pcl geometry::PointCloud with 796825 points. 

 ![avatar]( 20201209151016741.png) 

>  run Poisson surface reconstruction geometry::TriangleMesh with 563112 points and 1126072 triangles. 

 ![avatar]( 20201209151030334.png) 

  Poisson surface reconstruction will also create triangles in a low-density point cloud, and even infer some regions (such as the edge of the base output above). The function create_from_point_cloud_poisson also has a second returned value densities to represent the density of each vertex. A low-density value means that this vertex is only supported by a small number of points from the input point cloud. 

 In the code below we visualize the density of the 3D shape by pseudo-color. Purple indicates low density and yellow indicates high density. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574445206
  ```  
>  visualize densities 

 ![avatar]( 20201209151859956.png) 

  We can filter out the vertices and triangles with lower support by density values. In the code below we remove all vertices with density values lower than 0.01-0.010.01 and the triangles it connects. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574445206
  ```  
>  remove low density vertices geometry::TriangleMesh with 557480 points and 1113214 triangles. 

 ![avatar]( 20201209152159312.png) 

##  normal estimation 

 In the example above, we assume that the normals of the point clouds face outward. However, not all point clouds already have associated normals. Open3D can be used to estimate the point cloud normals using a point cloud normal with a Estimate_Normals that fits the plane of each 3D point to derive the normals. However, the estimated normals may not always agree. orient_normals_consistent_tangent_plane propagate the normal direction using a minimum spanning tree. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574445206
  ```  
 ![avatar]( 20210128212400799.png) 

 ![avatar]( 20210128212419528.png) 

