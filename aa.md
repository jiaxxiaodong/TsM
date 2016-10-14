### 堆和栈的特性

栈是先进后出.系统管理.
堆是程序员自己管理.

### 两个View传值
1.block 2.代理 3.通知 4.属性 5.全局变量 6.单例

### Runtime(运行时)

kvc和kvo都是运行时的方法,两者之间没有实质性的关系.
kvc 指的是字典转模型.
kvo 指的是观察者模式. 本质是通知的一种应用.

### Runloop(运行循环)

主线程里的runloop 是自动开启的
子线程的runloop 需要手动开启




### IOS 开发中数据持久性有哪几种

1.plist    2.偏好设置    3.归档    4.数据库/SQlite
5.coredata(本质就是数据库,是苹果对数据库的封装)

### App闪退的几种原因

0.违反ios系统规则
1.应用逻辑bug
2.内存暴涨
3.证书过期

### 核心动画有几种动画 (UI进阶 13天)

1.关键帧动画    2.组动画    3.转场动画    4基本动画 

### UIViewController的完整生命周期
 
-[ViewController initWithNibName:bundle:]；
-[ViewController init]；
-[ViewController loadView]；
-[ViewController viewDidLoad]；
-[ViewController viewWillDisappear:]；
-[ViewController viewWillAppear:]；
-[ViewController viewDidAppear:]；
-[ViewController viewDidDisappear:]；
1、 alloc                                创建对象，分配空间

2、init(initWithNibName) 初始化对象，初始化数据

3、loadView                         从nib载入视图 ，通常这一步不需要去干涉。除非你没有使用xib文件创建视图

4、viewDidLoad                 载入完成，可以进行自定义数据以及动态创建其他控件

5、viewWillAppear             视图将出现在屏幕之前，马上这个视图就会被展现在屏幕上了

6、viewDidAppear             视图已在屏幕上渲染完成

当一个视图被移除屏幕并且销毁的时候的执行顺序，这个顺序差不多和上面的相反

1、viewWillDisappear           视图将被从屏幕上移除之前执行

2、viewDidDisappear           视图已经被从屏幕上移除，用户看不到这个视图了

3、dealloc                               视图被销毁，此处需要对你在init和viewDidLoad中创建的对象进行释放

### XML解析的几种方式
1. SAX解析 占用内存较小
2. DOM解析 占用内存较大(苹果不支持使用DOM解析,如果使用就使用第三方框架)

### FMDB

一种数据库的第三方框架(新浪微博最后几天)

### 网络七层协议

1. 应用层     2.表示层     3.会话层   
4. 传输层    
5. 网络层
6. 数据链录层
7. 物理层

### 视频直播的原理

视频直播常用的两种协议
1. hls
2. rtmp

以hls为例:  
   推流: 数据采集/手机录像 -> 编码 -> 封装 -> 遵循hls协议上传服务器
   拉流: 遵循hls协议从服务器获取数据 -> 解封装 -> 解码 -> 播放

hls 编码格式是 H264/mpeg4
音频的编码格式 acc/Mp3

### 即时通讯

sdk 环信
XMPP 深入了解即时通信

### 响应者链 (UI进阶第十天 ppt)

### SDWebImage的原理

SDWebinage 用到多线程了 在子线程从网络下载图片,在主线程用imageView 显示图片

1. 先看内存有没有.如果没有在看沙盒有没有. 沙盒没有就网络下载
2. SDWebimage 对卡顿现象有一定优化 滑动的时候不下载,滑动结束在下载

### 内存管理
oc 在MRC情况下 用引用计数器retain release
   在ARC情况下 是用 强引用 若引用 strong weak
### 第三方登录 分享 

使用 友盟SDK

### 地图 

百度 SDK

### 项目中遇到的bug

看面试宝典

### 常见的Http 状态码有哪些?

http状态吗 ：302 是请求重定向。500以上是服务器错误。400以上是请求链接错误或者找不到服务器。200以上是正确。100以上是请求接受成功。

### Xcode 管理内存工具有几种
1. 静态内存管理
2. [instrument ](http://www.07net01.com/2015/11/1000712.html)

### ios常见的加密方式

1.base64 2.MD5

### MVC 和MVVM的区别

和网络有关的操作 单独分离出来放到ViewModel文件夹里
model 文件夹指写字典转模型

MVVM 
 Model View ViewModel
MVC
model view controller

### 从网络上获取数据是如何实现的

第三方框架 AFN 根据需求字典转转模型

### 需要处理大量的数据怎么办?

多线程.


### GCD死锁

看视频

### 单例

看视频 网络多线程第二天


