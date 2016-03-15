Android开发
====================
>目前包括：
[开发篇](https://github.com/zhangquanit/android#开源类库)
[测试篇](https://github.com/zhangquanit/android#测试篇)
[工具篇](https://github.com/zhangquanit/android#工具篇)

#开源类库
##网络库

1、**HttpUrlConnection**<br>

2、**[volley](https://github.com/mcxiaoke/android-volley "volley")**<br>
Volley,它是android开发团队在2013年Google I/O大会上推出了一个新的网络通信框架
Volley可以说是把AsyncHttpClient和Universal-Image-Loader的优点集于了一身，既可以像AsyncHttpClient一样非常简单地进行HTTP通信，
也可以像Universal-Image-Loader一样轻松加载网络上的图片。除了简单易用之外，Volley在性能方面也进行了大幅度的调整，
它的设计目标就是非常适合去进行数据量不大，但通信频繁的网络操作，而对于大数据量的网络操作，比如说下载文件等，Volley的表现就会非常糟糕

3、**[retrofit](https://github.com/square/retrofit "retrofit")**<br>
Retrofit支持同步和异步两种方式，在使用时，需要将请求地址转换为接口，通过注解来指定请求方法，请求参数，请求头，返回值等信息。

4、**[okhttp](https://github.com/square/okhttp)**<br>
okhttp 是一个 Java 的 HTTP+SPDY 客户端开发包（类似HttpClient的角色），同时也支持 Android。需要Android 2.3以上。<br>
特点 <br>
OKHttp是Android版Http客户端。非常高效，支持SPDY、连接池、GZIP和 HTTP 缓存。<br>
默认情况下，OKHttp会自动处理常见的网络问题，像二次连接、SSL的握手问题。<br>
如果你的应用程序中集成了OKHttp，Retrofit默认会使用OKHttp处理其他网络层请求。<br>
从Android4.4开始HttpURLConnection的底层实现采用的是okHttp.<br>

**特别说明**<br>
android2.2之后不建议使用Http Client,包括基于HttpClient的开源网络库:<br>
1、**HttpClient**<br>
Apach提供的HttpClient

2、**[android-async-http](https://github.com/loopj/android-async-http)**<br>
特点
所以请求在子线程中完成，请求回调在调用该请求的线程中完成 <br>
使用线程池 <br>
使用RequestParams类封装请求参数 <br>
支持文件上传 <br>
持久化cookie到SharedPreferences，个人感觉这一点也是这个库的重要特点，可以很方便的完成一些模拟登录 <br>
支持json <br>
支持HTTP Basic Auth <br>

##事件总线
1、**[EventBus](https://github.com/greenrobot/EventBus)**

2、**[Otto](https://github.com/square/otto)**

  
##图片库

**[Universal-Image-Loader][1]**<br>


**[Volley][2]**<br>


参照：ImageRequest、ImageLoader、NetworkImageView

**[Fresco][3]**<br>


**[Picasso][4]**<br>


**[Glide][5]**<br>


**[DroidParts][6]** <br>

参照：ImageFetcher

**[UrlImageViewHelper][7]**<br>


**[AndroidQuery][8]** <br>
参照:ImageLoading

##依赖注入
 
**[AndroidAnntations][9]**<br>

**[Dagger][10]**<br>

**[Butterknife][11]**<br>

**[RoboGuice](https://github.com/roboguice/roboguice)**

##数据存储
目前ormLite和greenDao应该是最火的

**[greenDao](https://github.com/greenrobot/greenDAO)**

greenDAO is a light & fast ORM solution for Android that maps objects to SQLite databases.<br>
当性能很重要时（数据访问频繁），GreenDao是一个很快的解决方案，它能够支持数千条记录的CRUD每秒，和OrmLite相比，GreenDAO要快几乎4.5倍。<br>
GreenDAO小于100KB，所以对于应用程序APK的大小影响很小。<br>

**[ormlite](https://github.com/search?utf8=%E2%9C%93&q=ormlite)**

OrmLite 不是 Android 平台专用的ORM框架，它是Java ORM。支持JDBC连接，Spring以及Android平台。语法中广泛使用了注解（Annotation）。<br>

[LitePal](https://github.com/LitePalFramework/LitePal)

LitePal is an Open Source Android library that allows developers to use SQLite database extremely easy.

[realm](https://github.com/realm/realm-java)

Realm is a mobile database that runs directly inside phones, tablets or wearables. This repository holds the source code for the Java version of Realm, which currently runs only on Android.

[tray](https://github.com/grandcentrix/tray)

a SharedPreferences replacement for Android with multiprocess support

[Paper](https://github.com/pilgr/Paper)

Fast and simple data storage library for Android. <br>
Paper is a fast NoSQL data storage for Android that lets you save/restore Java objects by using efficient Kryo serialization and handling data structure changes automatically.

##响应式编程
[RxJava](https://github.com/ReactiveX/RxJava) <br>
参考 
[http://blog.csdn.net/lzyzsd/article/details/41833541](http://blog.csdn.net/lzyzsd/article/details/41833541)


[RxAndroid](https://github.com/ReactiveX/RxAndroid)

##日志输出
[orhanobut/logger](https://github.com/orhanobut/logger)

Simple, pretty and powerful logger for android <br>
Logger provides : <br>
- Thread information <br>
- Class information <br>
- Method information <br>
- Pretty-print for json content <br>
- Pretty-print for new line "\n"  <br>
- Clean output   <br>
- Jump to source  <br>


[liaohuqiu/android-CLog](https://github.com/liaohuqiu/android-CLog)

[ZhaoKaiQiang/KLog](https://github.com/ZhaoKaiQiang/KLog)

这是一个Android专用的LogCat工具，主要功能为打印行号、函数调用、Json解析、XML解析、点击跳转、Log信息保存等功能

[Debug](https://github.com/noties/Debug)

##JSON
[alibaba/fastjson](https://github.com/alibaba/fastjson)

[google/gson](https://github.com/google/gson)

[jackson](https://github.com/FasterXML/jackson)

[LoganSquare](https://github.com/bluelinelabs/LoganSquare)


##热修复
###热修复原理
[http://blog.csdn.net/lmj623565791/article/details/49883661](http://blog.csdn.net/lmj623565791/article/details/49883661)
 
1、安卓App热补丁动态修复技术介绍 <br>
[https://mp.weixin.qq.com/s?__biz=MzI1MTA1MzM2Nw==&mid=400118620&idx=1&sn=b4fdd5055731290eef12ad0d17f39d4a&scene=1&srcid=1106Imu9ZgwybID13e7y2nEi#wechat_redirect](https://mp.weixin.qq.com/s?__biz=MzI1MTA1MzM2Nw==&mid=400118620&idx=1&sn=b4fdd5055731290eef12ad0d17f39d4a&scene=1&srcid=1106Imu9ZgwybID13e7y2nEi#wechat_redirect)

2、Android dex分包方案 <br>
[http://my.oschina.net/853294317/blog/308583](http://my.oschina.net/853294317/blog/308583)

###热补丁动态修复开源框架
1、[AndFix](https://github.com/alibaba/AndFix) <br>


相关文档 <br>
[http://blog.csdn.net/qxs965266509/article/details/49802429](http://blog.csdn.net/qxs965266509/article/details/49802429)

2、[HotFix](https://github.com/dodola/HotFix) <br>


3、[DroidFix](https://github.com/bunnyblue/DroidFix) <br>


4、[Nuwa](https://github.com/jasonross/Nuwa)  <br>


##插件化开发
利用DexClassLoader动态加载本地apk


##Android公共类库

[xutils](https://github.com/wyouflf/xUtils3) 

[Trinea/android-common](https://github.com/Trinea/android-common) 

[litesuits/android-common](https://github.com/litesuits/android-common) 

[FastDev4Android](https://github.com/jiangqqlmj/FastDev4Android)

[AndBase](https://github.com/zhaoqp2010/andbase)

##Android或Java工具库

[essentials](https://github.com/greenrobot/essentials)

The Utility classes cover stream-based IO, files, strings, and date/time. There are also efficient hash map and hash set implementation for primitive long keys.

[okio](https://github.com/square/okio)

A modern I/O API for Java


#测试篇

##测试相关
1、[Testin](http://www.testin.cn/)<br>
免费移动App真机云测试平台

2、[百度移动APP测试服务](https://console.bce.baidu.com/mat/manualTest/home/tasklist)<br>
可免费提供自动化测试和人工测试<br>


3、[BugTags](https://bugtags.com/) <br>
新一代的、专为移动测试而生的缺陷发现及管理工具。


4、[腾讯Bugly](http://bugly.qq.com/?bref=sdkcn) <br>

腾讯Bugly，面向移动开发者提供最专业的Crash监控、崩溃分析等质量跟踪服务，为您修复用户的每一次Crash！

5、[testerhome](https://testerhome.com/)<br>
支付宝Monkey老师推荐的测试社区、里面有很多干货.


##崩溃统计平台
对APP的崩溃进行统计，CritterCism和Crashlytics有时候需要梯子，你懂的。
腾讯Bugly、金山Crasheye、Crittercism、Crashlytics

##应用性能管理APM

百度百科：http://baike.baidu.com/link?url=WTSG1fVrdrBChzvRZ3L23qjRCoZEX2a2v-0wdiCJGZph8C1OgMAI-fiwVqCfP0328lux8PTK1oc-6eBlZiVYna

应用性能管理（Application Performance Management）是一个比较新的网络管理方向，主要指对企业的关键业务应用进行监测、优化，
提高企业应用的可靠性和质量，保证用户得到良好的服务，降低IT总拥有成本(TCO)。使用全业务链的敏捷APM监控，可使一个企业的关键业务应用的性能更强大，
可以提高竞争力，并取得商业成功，因此，加强应用性能管理（APM）可以产生巨大商业利益。
国内外的APM有Compuware、iMaster、听云、New Relic、云智慧、OneAPM、AppDynamics等。

https://www.sdk.cn/datas?category_id=110207

1、[腾讯Bugly](http://bugly.qq.com/?bref=sdkcn) <br>


2、[听云APP](http://www.tingyun.com/tingyun_app.html) <br>


3、[百度APM](https://bce.baidu.com/product/apm.html) <br>


4、[Testin移动应用性能管理](http://crash.testin.cn/) <br>


5、[oneapm](http://www.oneapm.com/mi/android.html) <br>


6、[透视宝](http://www.toushibao.com/mobile.html) <br>


##APP内测分发
APP开发完成后，需要提供给别人使用测试。

1、[蒲公英](http://www.pgyer.com/) <br>


2、友盟渠道升级 <br>
打包成自己的测试渠道，在线升级

3、腾讯Bugly内测 <br>
[http://beta.qq.com/?f=sdk](http://beta.qq.com/?f=sdk) <br>
平台优势：
轻松安装：快速发布至QQ与微信直接下载安装，无需另外打开浏览器
访问控制：按QQ号验证用户身份，精确控制版本访问权限
极速下载：依托腾讯CDN实现全网覆盖，全球范围内用户均可高速下载

4、[FIR.IM](http://fir.im/)

##监控
1、移动应用错误监控 <br>
https://www.sdk.cn/datas?category_id=110209

2、性能监控 APM <br>
https://www.sdk.cn/datas?category_id=110207

##其他 
###性能检测检测工具
[LeakCanary](https://github.com/square/leakcanary) <br>
检测内存泄露,square出品，必属精品

[blockcanary](https://github.com/moduth/blockcanary)<br>
检测UI卡顿，阿里工程师出品

[DebugDrawer](https://github.com/palaima/DebugDrawer)<br>
帮你快速的在debug版本分析，诊断问题

[ANR-WatchDog](https://github.com/SalomonBrys/ANR-WatchDog)<br>
检查ANR问题的利器

[ViewServer](https://github.com/romainguy/ViewServer)<br>
当你用真机调试连不上Hierarchy Viewer，它可以帮助你完美解决问题

MAT 内存分析工具 <br>
即Memory Analysis Tools

观察DDMS中的heap <br>
查看堆的分配情况，来回切换页面，如果totalSize只增不减，则可能存在内存泄露<br>

TraceView 分析 <br>

StrictModle 

相关技术文章：<br>
[https://www.sdk.cn/news/2013](https://www.sdk.cn/news/2013) <br>
[http://ms.csdn.net/geek/51979](http://ms.csdn.net/geek/51979) <br>
[http://blog.csdn.net/u010687392/article/details/49909477](http://blog.csdn.net/u010687392/article/details/49909477) 

#工具篇
##MarkDown
[作业部落](www.zybuluo.com) 或 [马克飞象](https://maxiang.io/)  <br>
提供在线MarkDown在线编辑器，可用于编写技术文档之类的。<br>
桌面工具：MarkDown Pad

##图床
免费上传图片，生成外链. <br>
[http://postimg.org](http://postimg.org) <br>
[http://imageab.com/](http://imageab.com/) <br>
[http://droplr.com](http://droplr.com) <br>
[http://www.nieyou.com/img/](http://www.nieyou.com/img/) <br>
[http://www.mftp.info/](http://www.mftp.info/)<br>
[http://tietuku.com/upload](http://tietuku.com/upload) <br>

##团队协作办公

[Tower](https://tower.im/) 、
[teambition](https://www.teambition.com/) 、
Jira、
明道OA、
禅道、
                


  [1]: https://github.com/nostra13/Android-Universal-Image-Loader
  [2]: https://github.com/mcxiaoke/android-volley
  [3]: https://github.com/facebook/fresco
  [4]: https://github.com/square/picasso
  [5]: https://github.com/bumptech/glide
  [6]: https://github.com/yanchenko/droidparts
  [7]: https://github.com/koush/UrlImageViewHelper
  [8]: https://github.com/androidquery/androidquery
  [9]: http://androidannotations.org/
  [10]: https://github.com/square/dagger
  [11]: https://github.com/JakeWharton/butterknife