#  First, the effect display 

![avatar]( 37b1a852c01447b1bbe917a3b44b5e1d.gif) 

#  II. Core Code 

The point cloud voxel filtering PCL is implemented as follows. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573813135
 ```  
#  III. QT Settings 

![avatar]( aa24dc15cf6e45cb9173381b8f350e70.png) 

 1, new dialog control, named Filter_voxel    

![avatar]( 1f11f087618143bcbe771990e6616085.png) 

 Add label and lineEidt widget, horizontal layout, then overall grid layout. The layout effect and style are shown in the figure below, dialog size: 400 * 200. Right-click ok, go to slot function 2, filter_voxel and filter_voxel .cpp to set .h file 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573813135
 ```  
.Cpp file 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573813135
 ```  
3, pcl_function voxel filtering function, the core code as shown in two, add the header file and function declaration in the pcl_function file, add the function implementation in the pcl_function. As follows: pcl_function 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573813135
 ```  
pcl_function.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573813135
 ```  
4. Add relevant code in mainwindow.h, and add relevant action in mainwindow.cpp to connect with the slot function. As follows: mainwindow.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573813135
 ```  
mainwindow.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573813135
 ```  
Qmake, build it. At this point, this section implements adding voxel filtering to the corresponding QT. See the above for specific effects. 

