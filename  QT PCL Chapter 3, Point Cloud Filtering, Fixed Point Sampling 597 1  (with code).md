In the previous chapter QT adds uniform sampling, this article continues to add fixed point sampling module to pcl_test software. Using random sampling, the point cloud is downsampled to a fixed point. The specific operations are as follows. 

#  First, the effect display 

![avatar]( a7973149daea4b5eb2001c2e61233637.gif) 

#  II. Core Code 

The functions in PCL are implemented as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573760214
 ```  
#  III. QT Settings 

![avatar]( 5b0e44f08edd4c158c7029589f196f9c.png) 

 1. Create a new UI interface. For the specific process, please refer to the previous articles. The class name is set to Filter_down. It can be seen from the above core code that there is only one data to interact with, so the UI final interface is as follows: The layout effect is as follows, the overall dialog size is set to 400 * 200, the name is set to fixed sampling 2, filter_down. H and filter_down. Cpp settings, right-click the ok key in the UI interface, go to the slot function, and enter the corresponding .cpp file. The part of the code is as follows: .h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573760214
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573760214
 ```  
3, pcl_function and pcl_function. Cpp to set .h requires the header file and declaration of the corresponding function 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573760214
 ```  
.Cpp function implementation 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573760214
 ```  
4. Add the relevant header file in mainwindow.h, and add the action and connect to the corresponding slot function of the menu bar in mainwindow.cpp. The details are as follows: .h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573760214
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573760214
 ```  
#  follow-up 

At this point, a fixed point sampling module has been added to the software pcl_test, and other point cloud filtering modules will be added later. 

