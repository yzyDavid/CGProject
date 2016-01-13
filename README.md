# CGProject
ZJU CG Project
2015 Winter

~~本来想做7舍，不知道咋的就成lovelive了~~
# 概述 #
简单室内场景三维建模，绘制了一个LoveLive主题的体育馆的室内场景。
体育馆内具有基本体素构成的箱子、球等物件。
体育馆模型由OBJ格式文件导入。其中OBJ文件的导入函数为组员自己编写。
体育馆及其中所有物体均具有材质与纹理。
存在具有NURBS曲面并能够对其进行平移旋转和缩放。
有光照功能，包括正常光、聚光灯以及手电筒三种模式，三种模式可以兼容。
可以在体育馆中漫游，有第一人称视角与自由漫游视角两种模式。
体育馆中的大屏幕上有LoveLive动画播放。
体育馆墙壁以及箱子、舞台有碰撞检测，大门处在关门时无法通过，按开门键后可以通过。

# 文件说明 #
TransObj.cpp是处理obj文件的代码。

CGProject文件夹内是本次实验的主要工程。
各种源代码在Code\CGProject\CGProject下，main.h为函数和变量的声明，main.cpp为函数实现，glm.cpp和glm.h是经过我们修改的glm库。
编译后的可执行文件为Code\CGProject\build\Debug\CGProject，为了方便测试，使用的图片、模型等均在此文件夹下。
Code\CGProject\build\Debug\model中为模型文件（obj和mtl）。
Code\CGProject\build\Debug\texture中为门和时钟的纹理文件。
Code\CGProject\build\Debug\tex_soreboku中为舞台的纹理文件。
Code\CGProject\build\Debug\video中为视频转换成的图片文件。
Code\CGProject\build\Debug也是截图保存的位置。

# 操作说明 
1.	视角变换操作
按键盘上的数字键2/3可以切换漫游视角/第一人称视角。
在漫游视角中，按d和a可以增减x方向上的坐标，按s和w可以增减y方向上的坐标，按x和z可以增减z方向上上的坐标。
在第一人称视角中，按a和d可以转动视角方向，按w和s可以前进或后退。
2.	大灯操作
按空格键开启或关闭大灯。
按0键更改大灯位置，按1键更改大灯颜色。
在更在大灯位置的情况下，按l和j可以增减主灯x坐标的值，按i和k可以增减主灯y坐标的值，按v和c可以增减主灯z坐标的值。
在更改大灯颜色的情况下，按l和j可以增减主灯R的值，按i和k可以增减主灯G的值，按v和c可以增减主灯B的值。
3.	手电筒操作
按4开启或关闭手电筒。
手电筒参数只能随着第一人称视角下摄像机移动而修改。拖动鼠标，人物转向和移动的时候会改变手电筒的参数。
4.	聚光灯操作
按5开启或关闭聚光灯。
按h和f可以增减聚光灯x坐标的值，按g和t可以增减聚光灯z坐标的值，按m和n可以增减聚光灯的光圈大小，按b可以切换聚光灯的颜色。
5.	曲面物体操作
按6显示或隐藏曲面物体。
按7可以开启或关闭物体缩放动作。
按8可以开启或关闭物体平移动作。
按9可以开启或关闭物体旋转动作。
6.	开门关门操作
按，键可以关门和开门。
7.	截图操作
按p键可以截图。
