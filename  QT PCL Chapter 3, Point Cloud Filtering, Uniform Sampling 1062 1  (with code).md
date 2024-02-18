Following on from the previous section on approximate voxel sampling, this section continues to add uniform sampling to QT. 

#  First, the effect display 

![avatar]( a99172829d9546f9b6605594d8700364.gif) 

#  II. Core Code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957386630
 ```  
#  III. QT Settings 

![avatar]( 689f8cb6dbec49a19610c1db131149e5.png) 

 1, a new dialog window, for passing parameters, as shown in the figure, first in the forms part of the right-click, new file, we named Filter_uiform. 2, ui interface layout, through the above core code can be seen, uniform sampling required to pass only one parameter, we set the ui interface as follows, its layout is also as follows, the window size is set to 400 * 200, the window name is set to uniform sampling. Right click ok to go to the slot function. 3, filter_uniform and filter_uniform .cpp file setting code.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957386630
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957386630
 ```  
4. Realization of functions in pcl_function: You need to add the corresponding header file in pcl_function, and add the corresponding function implementation.h in .cpp. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957386630
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957386630
 ```  
5. Add corresponding menu bars and actions to the main function 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957386630
 ```  
6, the action is connected to the slot function, the slot function is implemented as follows: mainwindow.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957386630
 ```  
mainwindow.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957386630
 ```  
Qmake, build it, and then add the uniform sampling filter function to QT. 

