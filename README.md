##开发神器 — 一些免费流畅的Android模拟器

10年我开始接触Android开发时候，手头上甚至没有一部低端的Android手机，那时候用的是Android SDK自带的AVD模拟器，相信任何Android开发者都对这货深恶痛绝。一直以来，Android开发都有以下的毛病：
 
 - AVD模拟器奇卡无比；
 - 使用USB数据线链接手机经常无法设别设备；
 - Log日志输出不全；

一直以来都想找一款能够顺畅运行APP的Android模拟器，以下就介绍几款比较给力的。


###大名鼎鼎的[Genymotion](https://www.genymotion.com/)

[Genymotion](https://www.genymotion.com/)是一款顺畅和容易（fast and easy-to-use）使用的Android模拟器，可以用来运行和调试你的APP。[Genymotion](https://www.genymotion.com/) 来自于[AndroVM](http://androvm.org/blog/) 这个开源项目，基于 x86 和 [VirtualBox](https://www.virtualbox.org/)，支持 OpenGL 加速，可以用于 `Mac/Win/Linux`。最近发布了新版，支持了 Android2.3/4.3，新增了拖拽安装 apk，移除了 Google 市场（后面提供解决方案）。另外增加了功能更丰富的[付费版](https://shop.genymotion.com/index.php?controller=order-opc)，个人可以继续使用免费版。

####特点

 1. 超级流畅；
 2. 支持拖拽安装APK；
 3. 有多种Android系统版本和设备类型供选择；
 4. 能模拟手机的旋转、充电情况、GPS数据等物理数据；

####如何使用

简单介绍下如何获取和使用 Genymotion：

 1. [下载](https://www.virtualbox.org/wiki/Downloads)并安装 VirtualBox(或者下载带有VirtualBox的Genymotion)； 
 2. [注册](https://www.genymotion.com/#!/auth/signin) Genymotion 帐号并登录； 
 3. 根据自己的系统[下载并安装](https://www.genymotion.com/#!/download) Genymotion；
 
启动Genymotion
![enter image description here](https://lh3.googleusercontent.com/66_K51N5wvvgXz91KyE2BP7tuDJsQjyjeYgN65uixqk=s600 )

添加设备
![enter image description here](https://lh3.googleusercontent.com/-0u3sa4q88cg/VUIeKQKeUqI/AAAAAAAAA78/Jap-h9C3aWA/s600/QQ%25E6%2588%25AA%25E5%259B%25BE20150430201856.jpg )

启动设备
![enter image description here](https://lh3.googleusercontent.com/-pjk8lBm2pqo/VUIffDXlDeI/AAAAAAAAA8Q/NaSSaBxDNOo/s600/000.gif )

免费版跟收费版功能的区别
![enter image description here](https://lh3.googleusercontent.com/-Xswg7RXC9dw/VUIgdIGFcUI/AAAAAAAAA8k/da5cAvJ70hs/s800/QQ%25E6%2588%25AA%25E5%259B%25BE20150430202656.jpg)

此外，Genymotion还提供了`Eclipse`和`Intellij Idea(Android Studio)`的插件，方便你从IDE启动模拟器，不过目前插件的功能也仅仅是用于启动模拟器。


当然Genymotion也不是万能的，它也有一些不足之处。

####Genymotion无法启动
`Window`版本的`Genymotion`与`VirtualBox`的链接经常出问题，Genymotion经常无法启动，并提示VirtualBox引擎出错，关于Genymotion安装以及启动过程中出现的问题，你可以参考[官方的帮助文档](https://www.genymotion.com/#!/support#faq)。

####Genymotion无法安装Google Play
前面说过，新版 Genymotion 移除了 Google 市场。实际上，对 ARM library 的支持也一并移除了：

>Both the “Google apps” and the “ARM library support” features are removed.

有的APP用到了ARM的SO库，安装这些 App 时，会报`「INSTALL_FAILED_CPU_ABI_INCOMPATIBLE」`错误，比如微信。[`xda 论坛`](http://forum.xda-developers.com/showthread.php?p=47502902)给出了一个解决方案，经验证确实好用。
安装 GApps（含 Google 市场）和 ARM Translation（提供 ARM 支持）的步骤：

 1. 下载 [ARM Translation Installer v1.1](http://forum.xda-developers.com/showthread.php?p=47502902#post47502902)； 
 2. 下载对应系统的 [GApps](http://forum.xda-developers.com/showthread.php?p=47502902#post47502902)； 
 3. 安装第 1步下载到的文件（直接把 zip 文件拖进虚拟机，不要解压），安装完关闭虚拟机再打开；
 4.  安装第 2 步下载到的文件（步骤同上）；

这样，Google Play 和其他 Google App 都有了，再安装微信等应用也不会报错了。（但是此方法并不是对所有的APP都管用， `Genymotion对使用了ARM的SO库的APP的支持确实不好`，希望以后能改进）。


###电脑上也可以玩Android游戏的[BlueStacks](http://www.bluestacks.net.cn/)
Android 第一個第三方的模拟器就是 `Bluestacks`，网络上也有許多介绍文章。最大优势是占用资源小，安装包用量大约是 182 MB 左右，同样有 Windows / Mac 版、内置Google Play 商店。
####如何使用
首先，xp用户需先安装[Windows Installer 4.5](http://www.pc6.com/softview/SoftView_451.html)和[.NET Framework 2.0 SP2](http://www.pc6.com/softview/SoftView_65398.html)，否则会提示出错，我们这里也提供了下载，如果电脑上已经安装过这些软件可以跳过此步。然后到官网[下载](http://www.bluestacks.net.cn/Download/)最新的安装包并安装。

安装

![enter image description here](https://lh3.googleusercontent.com/-KJO99RX-wIA/VUI0BN7WmNI/AAAAAAAAA9E/U0afkiEbw2I/s600/17648984_0800.png )

启动模拟器，搜索应用并安装

![enter image description here](https://lh3.googleusercontent.com/-1QzELPsE7Hc/VUI0ZxOGJzI/AAAAAAAAA9Y/q4o_ypE_5v0/s600/17649209_0800.png)

运行APP

![enter image description here](https://lh3.googleusercontent.com/-_OQOLUGTqpk/VUI0wxO2HTI/AAAAAAAAA9s/4X2O6D3axRI/s600/17650830_0800.png)

####不足之处
 `Bluestacks`相比`Genymotion`，不容易出现无法启动的问题，也支持ARM Library，但不足之处也是明显的：

 1. 流畅度不如`Genymotion`；
 2. 没有多种Android系统以及设备型号供选择；
 2. 最致命的，`Bluestacks`是为了游戏而不是为了开发而设计的，所以无法竖屏，不适合开发 ；

###最适合开发的Android模拟器[Droid4X](http://www.droid4x.cn/)
正如官网所介绍的，海马玩模拟器(Droid4X)是迄今为止在性能，兼容性和操控体验方面最好的安卓模拟器。通过Droid4X，用户可以在PC上享受百万移动应用和游戏带来的全新体验。

海马玩模拟器在Android内核和图形渲染方面取得了突破性的成果，在同等PC硬件配置下，整体性能超出其他同类产品50%以上。海马玩模拟器美解决了ARM程序在X86架构下的运行问题，兼容市面现有99%以上的应用和游戏。

`Droid4X`模拟器是利用`VirtualBox`为基础，支持滑动按键，自带ROOT权限，启动速度快等等。相信很多朋友使用传统安卓模拟器都会遇到各种各样的问题导致使用体验差。而这款海马玩安卓模拟器(DROID4X)不仅支持双显卡的电脑同时系统内自带资源库，让你完完全全感受原生安卓的独特魅力。使用海马玩安卓模拟器(DROID4X)能让你轻轻松松使用电脑的安卓客户端。

####特点

 1. 速度流畅，稍微不如Genymotion，但是比BlueStacks好很多；
 2. 支持横竖屏切换，支持摇动以及GPS数据模拟；
 3. 支持ARM Library，能够运行Google Play等Genymotion无法运行的APP；
 4. 支持手柄控制；
 5. 未来支持在IOS运行，也就是可以用IPHONE运行Android应用了，想想就怕；

####如何使用

 1. [下载](https://www.virtualbox.org/wiki/Downloads)并安装 VirtualBox；
 2. 下载并安装[Droid4X](http://www.droid4x.cn/)；

运行模拟器

![enter image description here](https://lh3.googleusercontent.com/DjrAtoUz-Zh6hTZ9GAzBKXPWer18hMphWBUTJJ8u-_c=s600)

设置竖屏

![enter image description here](https://lh3.googleusercontent.com/-1zJYm3AWydI/VUI5zi2X0mI/AAAAAAAAA-Y/DiZSTWjCaoo/s600/QQ%25E6%2588%25AA%25E5%259B%25BE20150430221611.jpg)

运行APP

![enter image description here](https://lh3.googleusercontent.com/-CaJXiFw7VfQ/VUI7VxLENiI/AAAAAAAAA-w/N5IXoTVpfzY/s600/0000.gif)

####不足之处
Droid4X可以说得上没什么可以挑剔的地方，非要说的话，就是流畅度稍微不如Genymotion，UI不如Genymotion“接地气”，更是为了游戏而设计的。此外，也不想Genymotion那样有众多Android系统版本可以选择，不过这些都是无关紧要的功能，毕竟我们不会用一个模拟器去作覆盖测试，是不？

###总结
从使用经验上来看，Droid4X确实是一款值得每个Android开发汪使用的模拟器，试想一下，每次完成Coding，轻轻按一下`Shift+F10`，或者使用“重大事件决策按钮”，如下图，

![enter image description here](https://lh3.googleusercontent.com/-j7I8DsniS0E/VUI96nrb25I/AAAAAAAAA_I/OzLOR28dgcE/s600/QQ%25E6%2588%25AA%25E5%259B%25BE20150430223512.jpg)

轻轻一按就将APP部署到模拟器上，再也不用为了AVD模拟器的卡顿而烦恼，再也不用担心不小心碰了一下USB数据线而导致APP部署失败，再也不用担心Logcat没有打印日志，开发过程是不是变得淋漓尽致？  其实，我一开始在寻找AVD的替代品，当找到Genymotion的时候是很感动的，不过为此还推荐给不少朋友使用，但是用久了，发现不支持ARM Libary就觉得不妥了，后面Genymotion启动经常失败更是觉得坑爹。

这次，朋友推荐我使用Droid4X，一开始我是拒绝的，不能说你使用我就使用是不，用过之后，才发现这货兼职是加了特技的，duang~的那么一下，APP就跑起来了。
