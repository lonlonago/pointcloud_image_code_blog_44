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

