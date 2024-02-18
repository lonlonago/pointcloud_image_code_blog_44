#  First, the principle of the algorithm 

##  1. Algorithm overview 

   The core of the Raycasting model is to emit an optical fiber from each screen pixel and then pass it through the entire body of data. 

##  2. Implementation process 

   The new RaycastingScene class in Open3D-0.14.1 provides basic ray casting functionality. 

###  2.1 Initialization 

 The first step is to initialize one or more triangulation models 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
   add_triangles (): Returns the ID of the added geometric shape. This ID can be used to identify which mesh was hit by the ray. 

###  2.2 Casting rays 

   The second step generates the ray, which is a 6-latitude vector defined by the origin and direction. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
   The result contains information about possible intersections with geometric shapes in the scene. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
   As can be seen from t_hit and geometry_ids, the first ray did hit the grid, but the second ray did not. 

###  2.3 Creating images 

 Create a scene with multiple objects 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
   RaycastingScene allows light rays to be organized with any number of front dimensions. For example, an array of shapes [h, w, 6] can be generated to organize rays to create an image. This class also provides helper functions for creating rays for pinhole cameras. The following creates a ray tensor of shape [240, 320, 6]. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
   The output tensor maintains the shape of the ray, allowing you to visualize the distance hit directly with matplotlib to obtain a depth map. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
 ![avatar]( 70caca4ced134c06a6703b7f6626c422.png) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
 ![avatar]( 8fc1f146b2874c53a04ffa10a85bcb46.png) 

 Further, other results can be plotted to visualize the original normals  

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
 ![avatar]( a24a9f8f9fc04b8eb4d23f7d2e9a896e.png) 

#  II. Complete code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453186
  ```  
#  III. Display of results 

##  1. Depth map 

 ![avatar]( 462289e101294b96a8dd711a722b05e3.png) 

##  2. The original normal 

 ![avatar]( 61e3d114aa3e42308e3f325b7d5fb216.png) 

##  3. Other characteristics 

 ![avatar]( 8403e26f922b49b39b53507239d23ac5.png) 

