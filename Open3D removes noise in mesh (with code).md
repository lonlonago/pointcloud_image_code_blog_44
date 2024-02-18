##  Function analysis 

   The results of various reconstruction algorithms (e.g. RGBD Integration does not have only one triangle mesh but multiple meshes. Some smaller parts (e.g. smaller than the main object) are due to noise and we will want to remove them. Open3d implements a connected component algorithm cluster_connected_triangles assigns each triangle to a connected triangle cluster, returns the index triangle_cluters of each triangle from the cluster, and the number of triangles in each cluster cluter_n_triangles and the surface area of the cluster cluster_area. The following code shows cluster_connected_triangles application and how to use it to remove false triangles. 

##  II. Complete code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574434637
  ```  
##  III. Display of results 

 ![avatar]( 2020120415233796.png) 

 Mesh containing noise Delete the mesh after small clusters Delete the mesh after large clusters  

