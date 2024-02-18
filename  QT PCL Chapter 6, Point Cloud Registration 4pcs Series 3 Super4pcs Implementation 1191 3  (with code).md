#  foreword 

According to the previous article Super4PCS method implementation, this section mainly integrates Super4PCS into QT software. 

#  First, the effect display 

![avatar]( 10b203b41c38408c9e6a23ba31e0adfd.gif) 

#  II. Core Code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573885988
 ```  
#  III. QT Settings 

![avatar]( e33e2187e2bf4b7c81bffbbf34eb0708.png) 

 1. Put the compiled code into pcl. As shown in the figure below, put the compiled super4pcs code in the previous link into the pcl source code. The operation is as follows: 1) Copy the gr and pcl folders in the include folder 2) Copy to the include/pcl-1.11 folder in the pcl folder, as shown in the figure below. 2) Create a new ui file, Register_s4pcs, and the layout is as follows: 3) register_s4pcs .h and register_s4pcs .cpp file settings 

.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573885988
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573885988
 ```  
4) pcl_function h and pcl_function cpp settings as follows: 

.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573885988
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573885988
 ```  
5) Mainwindow.h and mianwindow.cpp file settings 

.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573885988
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573885988
 ```  
Qmake, build it, and you can run it directly. At this point, point cloud super4pcs has been integrated into the software. 

