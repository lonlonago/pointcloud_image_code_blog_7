Continuing with the previous chapter, point cloud fixed sampling, this paper adds gridmin filtering, pcl-like :: Grid Minimum is to divide the three-dimensional point cloud into a grid in the X-Y plane, and then find the smallest z point cloud in each grid to represent the grid. If the grid does not have a point cloud, it will not generate a center point to represent the grid point cloud like pcl :: ApproximateVoxelGrid. 

#  First, the effect display 

![avatar]( 59a942941d1c4224abfa8348879206c4.gif) 

#  II. Core Code 

#  Third, QT display 

![avatar]( cf9ff8ea97d141a99ec92e05f7948c2f.png) 

 1. Create a new ui file. The process refers to the previous ones. They are all the same, and they are not introduced in detail here. Class name: Filter_gridmin. The ui layout is as follows, the name is set to Gridmin, and the size is 400 * 200.    

![avatar]( 99ec6e0c0e054728b9b62bc11f06d96c.png) 

  2. filter_gridmin and filter_gridmin file settings. Press the previous process, right-click the ok key on the ui interface, and go to the slot function. The code is as follows. H 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573757256
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573757256
 ```  
3, pcl_function and pcl_function file settings, you need to put the gridmin code implementation in this part, .h add header files and function declarations, .cpp file add function implementation. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573757256
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573757256
 ```  
4. The main function adds relevant header files, slot functions, menu bar actions, etc. For the specific implementation, see the following code: mainwindow.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573757256
 ```  
mainwindow.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573757256
 ```  
#  follow-up 

Qmake, build it, and at this point, the point cloud gridmin module has been added. The common downsampling filtering for point clouds has been completed, and point cloud denoising filters, such as statistical filtering and radius filtering, will be added later. 

