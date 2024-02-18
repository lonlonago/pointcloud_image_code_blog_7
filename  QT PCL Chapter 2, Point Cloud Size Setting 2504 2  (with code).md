The next chapter, the color setting of the point cloud, this article continues to add the point cloud size setting operation in QT, in order to facilitate the viewing of the point cloud display effect. 

#  First, the effect display 

![avatar]( c382b7a3121b4a698bd47d321b89cca7.gif) 

#  II. Core Code 

Its main function is still the code in PCL: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573897087
 ```  
#  III. QT Settings 

![avatar]( 217e29ec049c48aa93c2346db8a148f7.png) 

 3.1 Add the dialog module. The process is similar to the previous sections. The final effect of setting the relevant ui is as follows. The control information and layout are as follows:  

3.2 view_slider h and view_slider cpp documents are as follows 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573897087
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573897087
 ```  
3.3 Establish a slot function connection 

.H file is added as follows 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573897087
 ```  
.Cpp implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573897087
 ```  
Slot function join action 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573897087
 ```  
After qmake and build, you can set the size of the point cloud point. 

