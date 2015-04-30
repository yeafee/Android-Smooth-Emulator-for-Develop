
##开发神器 — 稳定流畅的Android模拟器

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
