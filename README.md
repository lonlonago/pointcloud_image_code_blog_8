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



--------------------------------------------------------------------------------

Continuing with the pass-through filtering in the previous chapter, this article adds conditional filtering. The function of conditional filtering is somewhat similar to that of pass filtering, and it also clips the axis. The effect is as follows: 

#  First, the effect display 

![avatar]( e460215d62f648e1a5e68bb03ef0c34c.gif) 

#  II. Core Code 

The core code is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573779202
 ```  
#  III. QT Settings 

![avatar]( 2cc36ed87d9c4c47819f0f447cf3c540.png) 

 1, ui settings 2, filter_condition h and cpp file settings as before 

3, pcl_function h and cpp documents as before 

4, mainwindow as before 

After qmake, it can be run after construction. At this point, the conditional filtering of qt is added. 

#  follow-up 

![avatar]( e45a7a2ac14c45f1a851b8585ab7b911.png) 

 Renderings, similar to passthrough, passthrough is preferred  

![avatar]( 7468afac19284c47bfa6e01830c9892e.png) 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the effect display 

![avatar]( cfc7d91795cf4ec1bbea442329946705.gif) 

#  II. Core Code 

The core code is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573727958
 ```  
#  Third, QT display 

![avatar]( eb5ca60e0c224f71841892110d7ff1dd.png) 

 1. UI layout, as follows. At this time, four parameters need to be passed, and the operation is as before.   

2, filter_guass and filter_guass settings, refer to the previous 3, pcl_function and pcl_function settings, as before. 4, mianwindow.h and mainwindow.cpp settings, as before. Mainwindow.h file 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573727958
 ```  
mainwindow.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573727958
 ```  
At this point, qmake, build it, and the radius filter has been added to the software filter module. 



--------------------------------------------------------------------------------

#  First, the effect display 

![avatar]( 849ce0f948b9428585d38f80860be7a8.gif) 

#  II. Core Code 

The implementation process of pass filtering in PCL is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573725794
 ```  
#  Third, qt settings 

1. UI layout, the new control here is shown in the figure below, radioButton. The main function is as a selection function. 

![avatar]( c41e18ddebaf4b11949c889646b8bc37.png) 

  2, filter_pt h and filter_pt cpp settings 

The settings are as follows, and radioButton should be set to select uniqueness, as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573725794
 ```  
 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573725794
 ```  
3. Set in the pcl_function, add the header file and function declaration required for filtering in .h, and add the core code in the .cpp file. As described in the previous chapter. 4. The settings of mainwindow.h and mainwindow.cpp are the same as those set in the previous sections. I will not introduce too much here. 

Qmake, just build it, and at this point, the point cloud pass-through filter module has been integrated into the software. 

#  follow-up 

![avatar]( c1b51d1ab68d4febb5d9864e112093f8.png) 

 The test results are as follows:  

![avatar]( 11079546784b426aa61368da72a118db.png) 



--------------------------------------------------------------------------------

#  First, the effect demonstration 

![avatar]( c736f3722ac24dbebf1e0e97c6a4c73f.gif) 

#  II. Core Code 

The projection filtering in PCL is implemented as follows, in which the four parameters have four coefficients of the spatial plane equation. 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573722082
 ```  
#  Third, qt settings 

![avatar]( f6654a19b92648fd82ee47ccb8f76ef0.png) 

 1, ui settings, the layout is as follows, in the ui can create a new dialog. 2, filter_proj and filter_proj file settings, as before, this is not related to the description. 3, pcl_function and pcl_function file settings. Cpp file will copy the above core code, .h file for the function declaration and header file. As before, without detailed description, 4, mainwindow.h and mainwindow.cpp file settings. H can refer to the previous chapter for details 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573722082
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573722082
 ```  
So far, qmake, build it, and the projection filter module has been integrated into the qt software. 

#  follow-up 

![avatar]( f2ab62fa785f4d3994fa3bb5c2225132.png) 

 Post-projection renderings.  



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

Reference link: ISS keypoint extraction 

#  First, the effect display 

![avatar]( c9987864edb24e8a8e4b61bdd4b4d1dd.gif) 

#  II. Core Code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573735654
 ```  
#  III. QT Settings 

Refer to the previous settings, just pass the required parameters of the ISS into the slot function. Refer to the UI layout in the Filtering section. 

#  IV. Run the code directly in vs 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573735654
 ```  


--------------------------------------------------------------------------------

Reference link: SIFT key point extraction 

#  First, the effect display 

![avatar]( bf97549e56e542dba6d5eb63a388e4dc.gif) 

#  II. Core Code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573758700
 ```  
#  III. QT Settings 

##   Reference Filtering Chapter 

1. UI layout 2, pcl_function settings 3, mainwindow settings 

#  IV. VS directly runs the code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573758700
 ```  


--------------------------------------------------------------------------------

#  First, the effect display 

![avatar]( 1ad442de43ae4b60bbbaeb63fdea9536.gif) 

#  II. Core Code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573730437
 ```  
#  III. QT Settings 

Refer to the previous chapter on filtering 

1, ui layout settings; 2, pcl_function settings 3, mianwindow settings 

#  IV. Run the code directly in VS 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573730437
 ```  


--------------------------------------------------------------------------------

![avatar]( e14a5e49e10a4b4f884739c61bfa9bce.png) 

#  code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573764095
 ```  
#  usage 

subsequent updates 



--------------------------------------------------------------------------------

#  foreword 

This section begins with the point cloud registration 4PCS series. The point cloud 4pcs series mainly includes FPCS, KFPCS, Super4PCS methods, etc. This paper realizes the FPCS method. 

#  First, the effect display 

![avatar]( 2d46422e9c3b460b8f787da9befb968d.gif) 

#  II. Core Code 

The core code is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095738437
 ```  
#  III. QT Settings 

1) UI settings, new Dialog_fpcs, the layout is as follows: 

![avatar]( 3f51b8d80a3b4a409f13743c82d609f0.png) 

2) Related Dialog_fpcs settings.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095738437
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095738437
 ```  
3) pcl_function settings 

.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095738437
 ```  
.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095738437
 ```  
4) mainwindow settings.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 20240203095738437
 ```  


--------------------------------------------------------------------------------

#  First, the effect display 

![avatar]( 46c17022b69e44bbb55c6c3ef8ef48fd.gif) 

#  II. Core Code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573825148
 ```  
#  III. QT Settings 

Refer to the previous article, Point Cloud 4pcs Registration Series 1 - 4pcs Implementation 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  foreword 

This article begins to explain the ICP series registration. The ICP series mainly includes point-to-point, point-to-face, face-to-face, etc. This section realizes the most basic point-to-point registration. The effects are as follows: 

#  First, the effect display 

![avatar]( 0e32468afe8d42d7b6b8d5fd7b971df3.gif) 

#  II. Core Code 

The core code is as follows: 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573818352
 ```  
#  III. QT Settings 

![avatar]( c0be100697c64eae8320828248090fa8.png) 

 1. UI: Dialog_icp settings  

2、 dialog_icp.h 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573818352
 ```  
dialog_icp.cpp 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573818352
 ```  
3, pcl_function settings: refer to the core code 

4. Mainwindow settings: refer to the previous text 



--------------------------------------------------------------------------------

#  First, the effect display 

![avatar]( abbb161c2826434ca2624f8ac5dd4a07.gif) 

#  QT Settings 

![avatar]( b9dac624cc3d48d291eea422cfa71f7b.png) 

 1) Layout design, if you think this layout is too ugly, you can add tree controls, please refer to the case for details: 

1, add tree control 

2. After adding the tree control, the registration operation is displayed as follows 

![avatar]( cda3b26ba280400891dbe3a2c69db828.gif) 

#  III. Core Code 

ICP Point-to-Point Operation 2 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573856662
 ```  
![avatar]( a55d2bf936934f82bfa27c8ceb569dad.png) 

over 



--------------------------------------------------------------------------------

#  First, the effect display 

![avatar]( 120ebe2b3fda41439ebc5126763fd256.gif) 

#  QT Settings 

Refer to ICP series 1 

#  III. Core Code 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573852727
 ```  
 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573852727
 ```  
其中` 1、 pcl_feature_normals_k 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573852727
 ```  
2、 pcl_base_cloudwithnormals 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573852727
 ```  
3、 Show3_clicked 

 ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309573852727
 ```  


--------------------------------------------------------------------------------

