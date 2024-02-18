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

