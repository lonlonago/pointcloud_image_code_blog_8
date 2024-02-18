This article continues with the previous chapter, adding point cloud voxel filtering in qt, and continuing to add approximate voxel filtering in the software. 

#  First, the effect display 

![avatar]( 3de07471920746f7bbc50f676d39e6eb.gif) 

 The approximate voxel effect is shown as follows:  

#  II. Core Code 

Point cloud approximate_voxel_grid principle There are many on the Internet, roughly through the center point of each voxel grid to approximate the point in the voxel, not in detail here, the specific implementation code is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573720789
 ```  
#  III. QT Settings 

![avatar]( e8e7206c553b48f5b1fa3ea986e14c1a.png) 

 1. UI interface settings. UI interface refers to the point cloud voxel sampling settings in the previous chapter. The new class name is Filter_avoxel. The final UI interface and layout are as follows. Right-click into the slot function through the UI interface ok. Then add the corresponding signal in filter_avoxel and filter_avoxel. Cpp.   

2. filter_avoxel and filter_avoxel cpp documents are as follows: .h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573720789
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573720789
 ```  
3, function function implementation, refer to the core code, respectively, add the following code in pcl_function and pcl_function 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573720789
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573720789
 ```  
4. Mainwindow.h and mainwindow.cpp increase the correlation action and signal slot connection. Pass the parameters input in the dialog back to the correlation function, the specific implementation is as follows: .h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573720789
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573720789
 ```  
To program qmake, build it, so far completed the approximate voxel function implementation. 

