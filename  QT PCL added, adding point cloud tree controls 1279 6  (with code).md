#  foreword 

 1. Question: In the "QT PCL" column, many people have asked to add tree controls to the display interface, and the effect is as follows: 

 2. Solution: Take the above source code as an example and add tree controls. 

3. Main functions: 

 4. Result: Final source code: Add tree controls 

#  First, the effect display 

![avatar]( e04e7d05cabb440bab3b89a9483180ad.gif) 

#  Qt layout 

1. Control change, replace the control where the properties in the picture are located from textBrowser to treeView, as follows. 

![avatar]( 987fbf9a8b1d4e67a6e472a7151028d9.png) 

![avatar]( cc7a1b26290b427889ea9c428ef36c3e.png) 

#  III. Relevant codes 

The addition of tree controls in QT mainly refers to QtreeView related properties. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573731686
 ```  
As long as you make good use of the relevant properties of QtreeView, there should be no other difficulties in the future. There are two main points: 

1. When reading a point cloud, you need to display all point clouds. It is not necessary to display only a single point cloud at a time. Add the following to the reading place: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573731686
 ```  
![avatar]( 255839389dd64f489267267ddff5724a.png) 

 In this way, each time the point cloud is read, the status is as follows, and the checkbox is in a ticked state:  

2. How to change the parameters and display through the checkbox 

By setting the slot function in treeview, each time the information changes in treeView will be linked to the parameters and the displayed changes. The code is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573731686
 ```  
 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573731686
 ```  
Change the value of the cloud_index by whether it is currently checked. When cloud_index [i] == 0, it means not to display, and when cloud_index [i] == 1, it means to display. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573731686
 ```  
The code view_updata is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573731686
 ```  
