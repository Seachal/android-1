# Android知识整理

 - **网络库**

1、HttpUrlConnection<br>

2、volley<br>
Volley,它是android开发团队在2013年Google I/O大会上推出了一个新的网络通信框架
Volley可以说是把AsyncHttpClient和Universal-Image-Loader的优点集于了一身，既可以像AsyncHttpClient一样非常简单地进行HTTP通信，
也可以像Universal-Image-Loader一样轻松加载网络上的图片。除了简单易用之外，Volley在性能方面也进行了大幅度的调整，
它的设计目标就是非常适合去进行数据量不大，但通信频繁的网络操作，而对于大数据量的网络操作，比如说下载文件等，Volley的表现就会非常糟糕

3、retrofit<br>
Retrofit支持同步和异步两种方式，在使用时，需要将请求地址转换为接口，通过注解来指定请求方法，请求参数，请求头，返回值等信息。

4、okhttp<br>
okhttp 是一个 Java 的 HTTP+SPDY 客户端开发包（类似HttpClient的角色），同时也支持 Android。需要Android 2.3以上。
特点
OKHttp是Android版Http客户端。非常高效，支持SPDY、连接池、GZIP和 HTTP 缓存。
默认情况下，OKHttp会自动处理常见的网络问题，像二次连接、SSL的握手问题。
如果你的应用程序中集成了OKHttp，Retrofit默认会使用OKHttp处理其他网络层请求。
从Android4.4开始HttpURLConnection的底层实现采用的是okHttp.

**Android不推荐使用的基于HttpClient网络库**
android2.2之后不建议使用Http Client
1、HttpClient

2、android-async-http
特点
所以请求在子线程中完成，请求回调在调用该请求的线程中完成
使用线程池
使用RequestParams类封装请求参数
支持文件上传
持久化cookie到SharedPreferences，个人感觉这一点也是这个库的重要特点，可以很方便的完成一些模拟登录
支持json
支持HTTP Basic Auth
  
 
 - **网络图片加载库**

**[Universal-Image-Loader][1]**<br>
地址：https://github.com/nostra13/Android-Universal-Image-Loader

**[Volley][2]**<br>
地址：https://github.com/mcxiaoke/android-volley
参照：ImageRequest、ImageLoader、NetworkImageView

**[Fresco][3]**<br>
地址：https://github.com/facebook/fresco

**[Picasso][4]**<br>
地址：https://github.com/square/picasso

**[Glide][5]**<br>
地址：https://github.com/bumptech/glide

**[DroidParts][6]** <br>
地址：https://github.com/yanchenko/droidparts

参照：ImageFetcher
**[UrlImageViewHelper][7]**<br>
地址：https://github.com/koush/UrlImageViewHelper

**[AndroidQuery][8]** <br>
参照:ImageLoading

 - **注解开发**
**[AndroidAnntations][9]**<br>

**[Dagger][10]**<br>

**[Butterknife][11]**<br>

在此输入正文


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