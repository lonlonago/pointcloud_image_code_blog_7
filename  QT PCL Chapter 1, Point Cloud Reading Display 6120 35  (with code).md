#  Configuration problem sorting 

version configuration 

PCLQT version configuration, download resources 

The chapter source code 

#  First, the core code 

##  1.1 Point cloud reading display 

Point cloud visualization 

##  1.2 Point cloud reading txt file 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
#  QT Settings 

##  2.1 New QT mainwindow 

![avatar]( 7248fbb7136c42c796542cd192c91cdb.png) 

##  2.2 Add relevant information to the pro file 

Add pcl dependency library information, the version I use is pcl 1.8.1 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
##  2.3 UI interface layout 

![avatar]( c84efe0b6413462ca2bd8baa42ee4dab.png) 

 Mainwindow.ui adds a widget widget, right-click to upgrade to QVTKWidget widget widget; to display the real-time properties and parameters of the point cloud, add two GroupBox widgets to the left of the QVTKWidget widget widget, and add textbrowser widgets to the groupbox respectively, with a grid layout; set the vertical layout of the two GroupBox widgets, and then lay them horizontally with QVTK, and set the ratio to 2:8. The final interface layout is as follows:  

![avatar]( 90ede8d954cc4e9a925cecf7ea62ff0f.png) 

 Run it to see the effect: Note that at this time, you need to add the relevant header files of vtk to the header file, otherwise an error will appear. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
##  2.4 Related code settings 

###  1. Add the basic header files of qt, some of which are used later, and are all added here. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
###  2. Add pcl related header files 

In order to facilitate the management of PCL related functions, directly create a pcl_function and pcl_function files in qt, and put the PCL header files and related functions here. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
###  3. Add relevant documents 

Add the pcl_function header file in mainwindow.h and under private in mainwindow.h: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
At the same time, you need to initialize the control in mainwindow.cpp, the code is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
###  4. The main function adds a menu bar 

1) The main function adds the header file contained in the create menu bar 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
2) Create the relevant code for the menu bar, and the code is still placed after the initialization function 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
![avatar]( 521c940a19b444a3b573cca6bb2b8527.png) 

 The running effect is as follows. There will be garbled characters in the place shown in the picture. At this time, add it to the header file. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
![avatar]( 9572ba00639a49918c1af0615686e182.png) 

 At this point, the running result is as follows:  

###  5. Add function functions 

At this time, the click read operation is invalid, so the signal and slot functions of qt need to be added. 

1) Add the slot function in the mainwindow.h file 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
2) Add the corresponding function implementation to the mainwindow.cpp file, which is mainly implemented to read pcd, ply, and txt format files. The code is as follows: The code for reading txt format is as described in 1.2 above: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
3) Create the signal and slot connection, and continue to add the slot function connection in the initialization function, as shown below. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
#  Effect display 

![avatar]( 13ea2b7b7ae248d5b73c0378ac41ea58.gif) 

 As depicted in the figure below, the final demonstration effect is as follows:  

#  IV. Other settings 

![avatar]( e7687255a147438884288bff89da3851.png) 

 In order to make the display interface more comfortable, set the display background rgb to gray, as shown in the figure, change mainwindw to PCL software and add the following code to main.cpp. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
![avatar]( 72f198c160b94d9996889de8f7f5ca98.png) 

 ![avatar]( a5533c45e42f4bc7a23deda20e561f93.png) 

 The effect is as follows, change the small icon in the upper left corner to your favorite icon 1) Create a new resource file  

![avatar]( ed3e5687c3124b588d39d6f80919221a.png) 

![avatar]( 90692a7ace2a4939b27536653963034f.png) 

  Then add the downloaded ico file to the resource file, qmake, build the following, and add code in main.cpp. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957375653
 ```  
![avatar]( 05cc9c9d9eb64b559cb331a6e33c986a.png) 

 The resulting icon is as follows: At this point, the reading function of qt + pcl has been implemented. 

