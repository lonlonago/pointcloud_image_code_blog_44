   Open3D implements a scalable RGBD image ensemble algorithm based on techniques presented in [Curless 1996] and [Newcombe2011]. To support large scenes, a hierarchical hash structure introduced in Integrater in ElasticReconstruction is used. 

#   1、Read trajectory from .log file 

   The following example uses the read_trajectory function to read the camera track from a .log file. The contents stored in the .log file are shown below. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957442564
  ```  
   The detailed implementation of the function for reading the track is as follows: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957442564
  ```  
   The calling method is: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957442564
  ```  
#   2、TSDF volume integration 

   Open3d provides two types of TSDF spaces: UniformTSDFVolume and ScalableTSDFVolume. The latter is recommended because of the use of a multi-layered structure to support large-scale scenarios. The ScalableTSDFVolume function has the following parameters: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957442564
  ```  
 ![avatar]( 406797c685cc4593a73cca115de1cf37.png) 

#   3、Extract a mesh 

   Mesh mesh extraction using a moving cube algorithm. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957442564
  ```  
 ![avatar]( ef7710b5991948e7837ea29f6afe4a4b.png) 

>  Note: A TSDF space is like a weighted average filter in 3D space. If more frames are integrated, the space produces a smoother mesh. See Make Fragments for more examples. 

#   4. Complete code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957442564
  ```  
