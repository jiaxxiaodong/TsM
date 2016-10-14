### 堆和栈的特性

栈是先进后出.系统管理.
堆是程序员自己管理.

### 两个View传值
1.block 2.代理 3.通知 4.属性 5.全局变量 6.单例

### Runtime(运行时)

kvc和kvo都是运行时的方法,两者之间没有实质性的关系.
kvc 指的是字典转模型.
kvo 指的是观察者模式. 本质是通知的一种应用.

### IOS 开发中数据持久性有哪几种

1.plist    2.偏好设置    3.归档    4.数据库/SQlite
5.coredata(本质就是数据库,是苹果对数据库的封装)

### App闪退的几种原因

1.代码逻辑性错误
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


