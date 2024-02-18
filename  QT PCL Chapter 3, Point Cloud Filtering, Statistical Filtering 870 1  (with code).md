In the previous chapter, point cloud downsampling filtering, this section performs point cloud noise removal filtering and statistical filtering. Statistical filtering is the most commonly used noise removal filter. Its principle can be searched online, and its display effect is as follows. 

#  First, the effect display 

![avatar]( a090e9d066f64497950d0fd49e4fd262.gif) 

#  II. Core Code 

The core code is as follows, remember to add relevant header files. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573741767
 ```  
#  Third, qt settings 

![avatar]( dcc65498066b4ba9827c99eac83e1b4d.png) 

 1. UI layout is similar to the previous sections. Since two parameters need to be set in statistical filtering, the standard deviation coefficient is set to 1 in this paper, so only one transmission parameter is required. The layout is as follows: 2. filter_sor and filter_sor files are similar to the above chapters, and will not be repeated here. 3. pcl_function and pcl_function file to add the core code, remember to add the relevant header file. 4. Mainwindow.h and mainwindow.cpp files are not repeated here 

.H file 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573741767
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573741767
 ```  
So far, qmake, build it, and the point cloud statistical filtering module has been added to the software. 

#  follow-up 

![avatar]( 9894970d7f9740699dabc3acff34dfe4.png) 

 For statistical filtering, the renderings are as follows: Before statistical filtering:   

