# 机械女生，双非本985硕，目前学了C++基础知识，嵌入式或C++开发有希望吗还是转学Java更好?

作者：绿帽蝙蝠侠 链接：https://www.zhihu.com/question/623422508/answer/3227565506 来源：知乎 著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

搞[嵌入式](https://www.zhihu.com/search?q=嵌入式&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})，无非单片机和嵌入式Linux两个方向。

单片机用不到C++，只用C就够了，I2C、SPI、CAN等各种[通信协议](https://www.zhihu.com/search?q=通信协议&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})代码，每一步写法都是固定的，顺序变了就不正确了。完全死记硬背，跟默写课文一样，没编程基础也没关系，反正有没有基础，都是背。

因为[单片机](https://www.zhihu.com/search?q=单片机&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})的重点根本不在编程。而在于搞清楚各种[电子元件](https://www.zhihu.com/search?q=电子元件&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})的作用，并利用这些电子元件画出[原理图](https://www.zhihu.com/search?q=原理图&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})和PCB。

这需要学好[电子电路基础](https://www.zhihu.com/search?q=电子电路基础&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})，然后进行长期缓慢的积累，熟悉市面上各种型号、各种封装的电子元件。

只有先搞清楚每种元件的作用、性能与价格，区分它们的相同点与不同点，才能基于它们来设计电路。

硕士毕业啥岁数了？积累到能画PCB又啥岁数了？

如果要走单片机路线，个人建议重点放在电路本身，别把太多精力花在代码上。毕竟单片机绝大部分代码都是固定的。至少在理论上，任何固定代码，都可以一键生成。

就算今天不能生成，但万一哪天能了呢？

很多人担心自己的工作会被人工智能取代，对于单片机方向的所谓[嵌入式软件工程师](https://www.zhihu.com/search?q=嵌入式软件工程师&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})来说，这些担忧太早、太着急了。

因为生成固定代码，连人工智能都不需要。在汽车行业的Autosar上，今天已经有单片机[控制程序](https://www.zhihu.com/search?q=控制程序&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})的全自动生成方案了。

案板上躺着的还没开始慌，牧场里跑着的慌什么？

至于嵌入式Linux，分为[三大件](https://www.zhihu.com/search?q=三大件&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})。

Bootloader，通常是用U-Boot。

Kernel，也就是内核。

RootFiles，中文名叫[根文件系统](https://www.zhihu.com/search?q=根文件系统&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})。

无论其中哪一块，都包含C++代码，但这些代码不需要你写，而是[理查德](https://www.zhihu.com/search?q=理查德&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})·[斯托曼](https://www.zhihu.com/search?q=斯托曼&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})、[林纳斯·托瓦兹](https://www.zhihu.com/search?q=林纳斯·托瓦兹&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})等人的工作。

你要做的，是把它们的源码下载下来，进行一些自定义设置，然后用[交差编译器](https://www.zhihu.com/search?q=交差编译器&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})编译到ARM[开发板](https://www.zhihu.com/search?q=开发板&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})里。

而需要自己写的，是硬件驱动，也是C。

所以说，无论你走哪条路线，前期都只用C，用不到[C++](https://www.zhihu.com/search?q=C%2B%2B&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})。

那什么时候需要写C++？

只有三种情况，需要手写C++。

第一种情况，是做嵌入式UI，也就是QT，但这需要在完成源码编译，搞完驱动，[设备树](https://www.zhihu.com/search?q=设备树&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})，屏幕驱动之后才会涉及。另外呢，近几年有些新变化。目前[嵌入式方向](https://www.zhihu.com/search?q=嵌入式方向&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})有一个很火的[图形库](https://www.zhihu.com/search?q=图形库&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})，名叫LVGL，它有取代QT的趋势。最大的原因在于，LVGL是纯C图形库，不依赖C++。这样可以直接调用Linux本身的IO命令，因为Linux的IO接口也是纯C的。因此即便在UI方面，C++也可能会在未来几年逐渐被C取代。

第二种情况，是对接一些应用库，如OpenCV等，这也跟UI同理，都是要编译完三大件、写好驱动之后才涉及。

如果你能在嵌入式工作中做到这两步的话，某种程度上来说，你已经算高手了。

第三种情况，就是在Windows桌面上搞QT、OpenCV，这些不需要你懂Linux，也不需要交差编译，什么UBoot、内核、根文件系统，一样也不用学。但这跟嵌入式也没半点关系。

一般正常的单片机路线。

是先复习[物理电学](https://www.zhihu.com/search?q=物理电学&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})，就是中学那些[欧姆定律](https://www.zhihu.com/search?q=欧姆定律&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})，串联并联。接着学数电和模电，然后学C，搞单片机。

期间熟悉各种电容、电阻、Mos管、二极管、[三极管](https://www.zhihu.com/search?q=三极管&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})的规格，并学习用它们搭建电路。

然后学习焊接元件，画板子，其实就是电工那一套。

一般常见的[嵌入式Linux路线](https://www.zhihu.com/search?q=嵌入式Linux路线&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})。

需要先买开发板，主流是I.MX6ull，芯片以前是[飞思卡尔](https://www.zhihu.com/search?q=飞思卡尔&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})(摩托罗拉)的，现在是[恩智浦](https://www.zhihu.com/search?q=恩智浦&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})的。

这款芯片按照今天的标准，性能可谓非常垃圾，价格也不算便宜，但依然只推荐这款芯片。

因为当你遇到问题，上网搜索别人的例子，会发现十之八九都是以I.MX6ull举例说明的。初学不选它，包你后悔。

在我初学的时候，买的迅为的板子，质量没的说。被我虐待六七年，外设换了好几茬，蓝板子虐成了黑板子，怎么看都像个破烂。但各项功能依旧正常，稳如老狗。不植入广告宣传一下，我都觉得自己没良心。[只是不知道](https://www.zhihu.com/search?q=只是不知道&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})迅为公司今天还活着没有。。。

现在最常见的是[正点原子](https://www.zhihu.com/search?q=正点原子&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})阿尔法系列的板子。或者B站有个叫[韦东山](https://www.zhihu.com/search?q=韦东山&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})的UP主，自己打板子在淘宝卖，口碑也很好。

总之，无论谁家的板子，只要是基于[I.MX6ull](https://www.zhihu.com/search?q=I.MX6ull&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})的开发板就行，都能相互兼容，教程也通用。我六七年前买的时候，全套带液晶屏七百出头，今天差不多还是这价。不仅没降价，可能还涨了。

只要把这块板子玩明白，以后换成任何板子都能直接上手。

前期学习Linux基础，TFTP、NFS通信，搭建[交叉编译环境](https://www.zhihu.com/search?q=交叉编译环境&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})。

然后学习在开发板上编译三大件，学习编写驱动。Linux驱动粗分有三种，细分有五种。

分别是[字符设备](https://www.zhihu.com/search?q=字符设备&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})、[块设备](https://www.zhihu.com/search?q=块设备&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})、[网络设备](https://www.zhihu.com/search?q=网络设备&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})。

细分之下，又有杂项设备和[虚拟设备](https://www.zhihu.com/search?q=虚拟设备&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A3227565506})。

每种都很重要，全要学，也全是用C。

把这些都学完之后，你才能在开发板上编程来控制硬件。

等把全部功能开发完成，设备调试一切正常之后，可以给控制功能加个UI界面。到这一步，才会用到C++。

总之吧，嵌入式有路线差异。有些路线，你永远用不到C++。

至于能用到C++的路线，当你能用到它的时候，你早已经是高手了。

如果你还不是嵌入式高手，却已经开始写C++了，说明你还是比较适合专心搞机械。