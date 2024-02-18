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

