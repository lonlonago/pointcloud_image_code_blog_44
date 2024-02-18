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

