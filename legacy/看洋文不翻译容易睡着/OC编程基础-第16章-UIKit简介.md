####第16章 UIKit简介
到目前为止，我们学习了如何为OS X平台（即Mac操作系统）编写应用程序。不过关于Mac系统的开发先告一段落，现在我们来看看，如何为iOS平台编写应用程序。Mac应用程序使用的是AppKi框架，而iOS应用程序使用的是UIkit框架，它包含了所有的UI组件和构成iOS应用程序的资源。
iOS没有命令行使用权，所有我们无法向在OS X上一样创建命令行工具程序。我们这次要重构在第16章为OS X平台写的CaseTool程序，你甚至不需要iOS设备就可以做这个联系，只需要有附带了iOS SDK的Xcode应用就可以。从Mac AppStore上获取的Xcode会默认安装iOS SDK。
请记住iOS在以下方面与OS X不同：
1.没有shell和控制台
2.应用程序在Mac电脑的模拟器中运行
3.无法支持一些无UI界面的API
4.大部分程序员都认为开发iOS应用更加轻松
完成后应用看起来会和之前的CaseTool酷似，功能也相同。
先打开Xcode，创建新的project
选择新的Single View Application图标，意思就是这个应用程序只显示一个视图。这种类型的应用程序非常简单，用户界面也很简单。
以下是其他的模板的简单介绍
Master_Detail应用程序用一个导航控制器和一个表视图来显示项目列表以及项目的详细信息
OpenGL Game可以用来创建打发时间的游戏
Page-Based能帮你创建一个类似书本的应用程序，它拥有翻页的效果（只支持iPad）
Tabbed用来创建多视图应用程序，就像你平常在iPhone上见到的底部有一个标签栏并且每一个表钱都与一个视图有关联的那种应用程序。
Utility应用程序模板拥有一个主视图，与Single View Application中的想死，但还是多出一个翻转视图。
Empty应用程序是一个高级选项，如果没有合适的模板，或是你非常了解如何构建你的应用程序，那么你可以选择使用这个模板
选择好Single View App里擦提哦你之后，点击Next，需啊哟输入程序的名称：CaseTool
确保Use Storyboard和Include Unit Tests复选框没有被选中，而Use Automatic Reference Counting复选框要被选中。在Device Family下拉列表中，选择Universal，它意味着应用程序可以同时运行在iPhone iPod touch和ipad上。选完所有内容之后，点击Next按钮进入下一个界面，选择在哪一个目录中存储项目。
创建完项目之后，Xcode会打开它并将其展示出来
浏览一下，我们有了应用程序委托文件，此外还有另一个类和两个nib文件，分被用于iphone和ipad的。（如果没有选择universal，那么就只有一个nib文件）
我们来研究一下，应用程序委托头文件，首先是我们的老朋友#import，
这次我们使用的是UIKit框架而不是AppKit框架，所以iOS界面元素都是以UI为前缀的。
####16.2 小结
为了能让程序能在模拟器里运行，尽管Xcode帮了很多忙，但是我们还是要做不功。开发iOS应用程序需要用到大量的API，显然，我们学到的还只是一些皮毛哦。
本章介绍了如何在应用程序中使用属兔控制器以及iOS是如何管理试图内存的。孩讨论了与iOS有关的类，讲解了iOS与OSX的异同。
假如你打算开发iOS应用程序并且还想要学习更多的内容，可以参考《iOS 5基础教程》。
现在你可以更深入地学习Cocoa的知识和创建项目了。下一章将探讨Cocoa的存储以及加载文件的特性。
