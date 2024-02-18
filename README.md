#  First, the principle of the algorithm 

##  1. Fit a 3D circle 

   When a sphere intersects a plane, its line of intersection is a circle. Conversely, any circle in space can be expressed as the line of intersection of a sphere and a plane. Therefore, the Cartesian coordinate equation of the space circle can be obtained 

#  Code implementation 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574469261
  ```  
 Class Circle (): This class finds the parameters of the circle based on 3 random sampling points. Calculates the normal vector, center, and radius of the circle. 

##  2. Complete code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574469261
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574469261
  ```  
 ![avatar]( 831c5e4c63cd4d398115164ce625cba4.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   The core principle of the algorithm is still RANSAC fitting plane. For the specific theory, please refer to: Open3D uses RANSAC to split the plane. Just slightly modify the code to make it suitable for dividing multiple planes in point cloud data. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574420855
  ```  
#  III. Display of results 

 ![avatar]( 290d1175d99c444091883cf4bc14a2d4.png) 

#  IV. Test data 

 Link: https://pan.baidu.com/s/1xdCJ3KyouPCkl6cyKO4a0A Extraction code: ngea 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   The core principle of the algorithm is still RANSAC spherical fitting. For the specific theory, please refer to: Open3D - RANSAC three-dimensional point cloud spherical fitting. Just slightly modify the code to make it suitable for segmenting multiple spheres in point cloud data. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574466876
  ```  
#  III. Display of results 

 ![avatar]( 234103f6c04540379693eb275e2837bc.png) 

#  IV. Test data 

 Link: https://pan.baidu.com/s/1yJ9UEQVUJyn0V4515gWjEA Extraction code: f7ok 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Implementation process 

 ![avatar]( 20210323085455478.jpg) 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574426226
  ```  
##  3. Code analysis 

   Use RANSAC for global registration. In each RANSAC iteration, ransac_n random points are selected from the source point cloud, and their corresponding points in the target point cloud can be detected by querying the nearest neighbors in the 33-dimensional FPFH feature space. The pruning step requires the use of a fast pruning algorithm to weed out false matches early. The 3 pruning algorithms provided by Open3D are defined as follows: 

##  4. References 

>  [1] Choi S , Zhou Q Y , Koltun V . Robust reconstruction of indoor scenes[C]// IEEE Conference on Computer Vision & Pattern Recognition. IEEE, 2015. 

##  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574426226
  ```  
##  III. Display of results 

 ![avatar]( 20210112164255516.png) 

 The test data used in this paper: Open3D algorithm test data.rar RANSAC registration results ICP registration results   

#  IV. Reference link 

 [1] Global registration [2] Open3d学习计划——高级篇 3（点云全局配准） [3] Open3d之点云全局配准 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

 See: [1] Open3D least squares fitting space sphere [2] Open3D - RANSAC 3D point cloud spherical fitting 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574443621
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574443621
  ```  
 ![avatar]( 30e174e7a26e43a08a6f06c6d8a61476.png) 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the main function 

##  1. Read the point cloud 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
   Read the point cloud from the file. When the user does not fill in the extension of the point cloud, it will be automatically decoded; if it is filled in, it will attempt to decode the file according to the extension. 

 1. read_point_cloud used to read point cloud data. Open3D decodes files by file extension. Supported extensions are: pcd, ply, xyz, xyzrgb, xyzn, pts. By default, Open3D tries to infer the file type by file extension. 

##  2. Save the point cloud 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
   Save the point cloud to a local folder. 

##  3. Display point cloud 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
    Visualize point clouds. Use the mouse/trackpad to view geometric shapes from different angles. Press the H key to print out a complete list of keyboard commands for the GUI. 

##  4. Point cloud formats supported by Open3D 

 You can also read the specified file type, in which case the file extension is ignored. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
##  5. Output point cloud information 

##  Code implementation (including reading the TXT format) 

 1. Read common point clouds 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
 2. Read the point cloud in txt format 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
##  III. Display of results 

 ![avatar]( 20200826072947453.png) 

  Aircraft point cloud data in txt format  

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
##  Visualize two point clouds 

>  [Open3d] Visualization with open3d 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
##  Five, give random color to point clouds 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
 ![avatar]( 20201204172833240.png) 

##  Display the color of the point cloud itself 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574490325
  ```  
 ![avatar]( 20210129195623385.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Overview of the principle 

   First, the points are sorted according to the curvature value of the points, and the point with the smallest curvature value is selected as the initial seed point. The area where the initial seed point is located is the smoothest area. Growing from the smoothest area can reduce the total number of segmented segments and improve efficiency. 

##  2. Algorithm flow 

#  Code implementation 

 main.py 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574440910
  ```  
 regiongrowing.py 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574440910
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( 13366610d9ae40caae8558fd7150b880.png) 

##  2. Segmentation results 

 ![avatar]( b216885baec3454095eda2f5def5f777.png) 

##  3. Save the results 

 ![avatar]( 7cc96f9a0d17468b90efc1c86527d26d.png) 

#  IV. Experimental data 

 Link: https://pan.baidu.com/s/1Tvo91gN3rLCCZKM53I7_iQ Extraction code: l0zn 

#  V. Related Links 

 [1] Open3D(C++) 区域生长分割 [2] PCL 区域生长分割（C++详细过程版） [3] pclpy 点云区域生长分割 [4] python点云处理算法汇总(长期更新版) 



--------------------------------------------------------------------------------

#  First, the main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574499697
  ```  
>  Function Feature: Move unless finite point from PointCloud Args: remove_nan (bool, optional, default = True): Remove NaN value from PointCloud remove_infinite (bool, optional, default = True): Remove infinite value from PointCloud 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574499697
  ```  


--------------------------------------------------------------------------------

##  Function analysis 

   The results of various reconstruction algorithms (e.g. RGBD Integration does not have only one triangle mesh but multiple meshes. Some smaller parts (e.g. smaller than the main object) are due to noise and we will want to remove them. Open3d implements a connected component algorithm cluster_connected_triangles assigns each triangle to a connected triangle cluster, returns the index triangle_cluters of each triangle from the cluster, and the number of triangles in each cluster cluter_n_triangles and the surface area of the cluster cluster_area. The following code shows cluster_connected_triangles application and how to use it to remove false triangles. 

##  II. Complete code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574434637
  ```  
##  III. Display of results 

 ![avatar]( 2020120415233796.png) 

 Mesh containing noise Delete the mesh after small clusters Delete the mesh after large clusters  



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

 ![avatar]( 36d39749976043318b55738af0507f70.png) 

   As depicted in the figure, the blue is the overlapping area of the point cloud.  

>  If a point has more than one point within a certain distance threshold area, it is considered to have duplicate points. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574470823
  ```  
#  III. Display of results 

 ![avatar]( 18a4b29586df4c6e89f3d062fb4d1a30.png) 

 ![avatar]( 15d7c3860182422b9b605b1e1da658d3.png) 

 White is the overlapping point, red is the point after removing the overlap.  

#  CloudCompare 

 ![avatar]( 20210108213852922.gif) 



--------------------------------------------------------------------------------

#   1、RGBD images 

   Open3d provides image data structures. Supports a variety of functions, such as: read_image: Read images. write_image: Save images. filter_image: Image filtering. draw_geometries: Visualize images. Images in Open3d can be mutually converted with numpy. RGBDImage in Open3d consists of two images, RGBDImage.depth and RGBDImage.color. The process of generating RGBDImage from two images, RGBDImage.depth and RGBDImage.color. The process of registering two images to the same camera frame and ensuring the same resolution. The following tutorial describes how to read and use RGBD images from some well-known RGBD datasets. 

#  2、Redwood dataset 

   The default format of Open3d parsing depth images is the same as the storage format of Redwood data, namely: Depth is stored in a 16-bit single-channel image. Integer values represent depth, in millimeters. The following code implements RGBDImage.depth and RGBDImage.color two images generation RGBDImage. and outputs the relevant information of the RGBD image. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574452079
  ```  
 Function: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574452079
  ```  
 Implement the creation of an RGBDImage from a pair of color and depth images. The color image is converted to a grey release graph and stored as data of float type between [0, 1]. The depth image is also stored by float type and represents the depth value (unit: meters). The converted image can be presented as a numpy array and visualized by matplotlib. The following code implements the visualization of the color information and depth information of the RGBD image. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574452079
  ```  
 ![avatar]( 21d7fdbd9c7946dba8022f5563e76a3b.png) 

  Given a set of camera parameters, an RGBD image can be converted to a point cloud. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574452079
  ```  
   Here PinholeCameraIntrinsicParameters. PrimeSenseDefault is used as the default camera parameter, its image resolution is: 640x480, focal length (fx, fy) = (525.0, 525.0), optical center (cx, cy) = (319.5, 239.5). Use the identity matrix as the default external parameter. pcd.transform applies up and down flipping on the point cloud for better visualization purposes. 

#  3、SUN dataset 

   This section describes how to read and visualize RGBD images from the SUN dataset S.Song, S. Lichtenberg, and J. Xiao, SUN RGB-D: A RGB-D Scene Understanding Benchmark Suite, CVPR, 2015. The processing of Redwood data is almost identical to the previous section. The only difference is the use of create_rgbd_image_from_sun_format transformation functions to parse depth images from the SUN dataset. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574452079
  ```  
 ![avatar]( 98e69a4aedbe47cab04b0b0cc78887ec.png) 

#  4、NYU dataset 

   This section describes how to read and visualize RGBD images from the NYU dataset [Silberman2012]. This section is also almost identical to Redwood, with only two differences. First, NYU images are not in standard jpg or png format, so we need to use mpimg.imread to read a color image into a numpy array and convert it to an Open3d image. An additional helper function read_nyu_pgm is also required to read depth images from data in special big endian pgm format used by the NYU dataset. Second, create_rgbd_image_from_nyu_format conversion function is used to parse depth maps from the NYU dataset. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574452079
  ```  
 ![avatar]( e8e0e268cecb4f548552812074cfc763.png) 

#  TUM dataset 

   This section describes how to read and visualize RGBD images from the TUM dataset [Strum2012] _. This section is almost the same as the previous introduction to the Redwood dataset. The only difference is that the create_rgbd_image_from_tum_format function is used to parse the depth data from the TUM dataset. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574452079
  ```  
 ![avatar]( 30a616946c524fbb9819c95711b6c9eb.png) 



--------------------------------------------------------------------------------

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


--------------------------------------------------------------------------------

   The RGBD ranging method is to find camera movement between two consecutive pairs of RGBD images. The input is a pair of RGBImage instances, and the output is motion in the form of rigid body transformations. Open3D implements the paper F. Steinbrucker, J. Sturm, and D. Cremers, Real-time visual odometry from dense RGB-D images, In ICCV Workshops, 2011. and J. Park, Q. - Y. Zhou, and V. Koltun, Colored Point Cloud Registration Revisited, ICCV, 2017. Test Data: Open3D-RGBD Mileage Calculation Method Test Data.rar 

#  1. Read the camera internal reference 

   Many small data structures in Open3d can be read and written through JSON files. Including camera parameters, camera trajectories, pose diagrams, etc. We first read the camera internal parameters from the JSON file. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574437024
  ```  
#  2. Read RGBD images 

   This code block reads two pairs of RGBD images in Redwood format. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574437024
  ```  
>  Note: Open3D assumes that color and depth images are synchronized and registered in the same coordinate system. This can usually be achieved in RGBD cameras by turning on the synchronization and registration settings. 

#  3. Calculate mileage from a pair of RGBD images 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574437024
  ```  
   This code block calls two different RGBD testing methods. The first is from the paper F. Steinbrucker, J. Sturm, and D. Cremers, Real-time visual odometry from dense RGB-D images, In ICCV Workshops, 2011. The paper's approach is to minimize the color consistency of aligned images. The second algorithm is from the paper J. Park, Q. - Y. Zhou, and V. Koltun, Colored Point Cloud Registration Revisited, ICCV, 2017. In addition to color consistency, geometric constraints are also implemented. The two methods run at close speeds. But J. Park, Q. - Y. Zhou, and V. Koltun, Colored Point Cloud Registration Revisited, ICCV, 2017. It has higher accuracy in the benchmark dataset, so it is recommended. The main parameters of the OdometryOption () function are as follows: 

#  4. Visualize RGBD image pairs 

   Convert RGBD image pairs to point clouds and render them together. Note that the first (source) RGBD image is transformed by a transformation estimated by the range method. The two sets of point clouds after the change are aligned. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574437024
  ```  
 ![avatar]( 1367f30ed8914d8cbcc44027d0dd8afa.png) 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##   1. Overview of the principle 

   The Ball Rotation Algorithm (BPA) is a method of surface reconstruction related to alpha-shapes. Intuitively, imagine a three-dimensional sphere with a given radius and we place it on a point cloud. If it hits any 3 points (and it doesn't fall out of those 3 points), it creates a triangle. The algorithm then starts rotating from the edge of the existing triangle, creating another triangle every time it reaches 3 points and the ball doesn't fall out. 

##   2. Function analysis 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453896
  ```  
   Implemented the ball rotation algorithm proposed by F. Bernardini et al. (F. Bernardini et al., "The ball-pivoting algorithm for surface reconstruction", 1999. "). The implementation is also based on the algorithm outlined in Digne 2014 in" An Analysis and Implementation of a Parallel Ball Pivoting Algorithm ", 2014." Surface reconstruction is done by rolling a ball of a given radius on a point cloud, creating a triangle every time the ball touches three points. 

##   3. References 

>  [1] Bernardini F , Mittleman J . The ball-pivoting algorithm for surface reconstruction[J]. Visualization & Computer Graphics IEEE Transactions on, 1999, 5(4):349-359. [2] Ball pivoting 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574453896
  ```  
#  III. Display of results 

 ![avatar]( 20201202150015565.png) 

 Raw point cloud data, 3D point cloud model  



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

