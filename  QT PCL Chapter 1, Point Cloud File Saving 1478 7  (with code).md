Continuing with a chapter of qt + pcl point cloud reading, 1.1 point cloud reading display, today realizes the point cloud saving function of pcl. 

#  First, the core code 

In order to achieve fast saving and reading of point clouds, point cloud files are generally saved directly as binary files. For reference, point cloud reading and saving, this article saves them in PCDFileBinary and PLYFileBinary formats: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573733228
 ```  
#  QT Settings 

In the previous chapter, the saved menu bar has been created. Now you only need to add the slot function to save the point cloud. The code is as follows: 1) Add the slot function in the mainwindow.h file 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573733228
 ```  
2) Add a specific implementation in mainwindow.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573733228
 ```  
3) Add the connect connection to the initialization function, and at the same time, add the exit operation connect together 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573733228
 ```  
#  Effect display 

![avatar]( d133e25afa664cf5b493889ccb3c4a3f.gif) 

  So far, the save and exit functions of qt + pcl have also been implemented. 

