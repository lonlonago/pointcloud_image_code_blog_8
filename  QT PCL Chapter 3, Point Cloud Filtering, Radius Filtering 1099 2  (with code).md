#  First, the effect display 

![avatar]( b30476b48b574981948e387ed25dea80.gif) 

#  II. Core Code 

The point cloud radius filter pcl is implemented as follows, remember to add relevant header files. It is mainly to remove less than a few points within a fixed search range. Generally, discontinuous points and edge points are removed. For noise flying points, it can also be well eliminated. The core code is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573771241
 ```  
#  Third, qt settings 

![avatar]( 67aadfd868684fbb941b3b51e0a7ba57.png) 

 1. UI settings, it can be seen from the core code that there are two parameters in the point cloud radius filter that need to be passed, namely, the search radius has the number of searches. For specific settings, refer to the previous chapter, and the final layout is as follows: 2. filter_radius and filter_radius settings. Since there is one more transmission parameter in the radius filter, just add label and lineedit to the ui interface. Do not repeat 3, pcl_function and pcl_function. Cpp file setting.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573771241
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573771241
 ```  
4. Mainwindow.h and mainwindow.cpp files, because this paragraph of work is repeated with the previous introduction, the following chapters are basically skipped. 

Mainwindow.h file 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573771241
 ```  
Mainwindow.cpp file 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573771241
 ```  
At this point, qmake, build it, and the radius filter has been added to the software filter module. 

#  follow-up 

![avatar]( c550a4120c044e28a859816a69c81729.png) 

 Before radius filtering  

![avatar]( bd7e777d18864164bab0cea959e7a53e.png) 

 After radius filtering, it is obvious that a lot of noise and edge points are eliminated. 

