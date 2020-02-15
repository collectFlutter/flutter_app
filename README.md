![](https://github.com/shichunlei/flutter_app/blob/master/FlutterApp.png)

# FlutterApp
  FLutter各种项目学习文档,帮助你快速构建一个Flutter项目及功能点

## Android APK 下载地址

![](https://github.com/shichunlei/flutter_app/blob/master/1562927446.png)


`声明1：本项目仅供学习，如有侵权请联系本人进行删除。`

`声明2：本项目中部分功能页面是别人其他项目中的，但是本人并不是完全照抄原作者代码，再此也特别感谢原作者，部分参考别人页面的功能也已标注出原出处，如有侵犯原作者的地方请联系本人进行删除。`


## 联系我们
### QQ群：691819454

![](https://github.com/shichunlei/flutter_app/blob/master/screenshots/QQ图片20200121110501.png)
    
    手机号码：18601952581（微信同号）
    QQ：1558053958
    邮箱：1558053958@qq.com
    
    


## 本项目包括：

- 各种基本控件使用（Text、TextField、Icon、Image、ListView、GridView、Picker、Stepper、Dialog、Slider、Row、Appbar、SizeBox、BottomSheet、Chip、Dismissible、FlutterLogo、Check、Switch、TabBar、BottomNavigationBar、Sliver等）
- 自定义控件及使用
- 各种UI （豆瓣电影、tubi TV、追书神器、好奇心日报、每日一文、和天气、百姓生活、随机诗词、联系人、句子迷、朋友圈、有道精品课、高德地图应用demo等）


## 运行环境

```
[✓] Flutter (Channel beta, v1.12.13+hotfix.6, on Mac OS X 10.14.5 18F132, locale zh-Hans-CN)
    • Flutter version 1.12.13+hotfix.6 at /Users/14cells/Android/flutter
    • Framework revision 18cd7a3601 (8 days ago), 2019-12-11 06:35:39 -0800
    • Engine revision 2994f7e1e6
    • Dart version 2.7.0

[✓] Android toolchain - develop for Android devices (Android SDK version 29.0.2)
    • Android SDK at /Users/14cells/Android/SDK
    • Android NDK location not configured (optional; useful for native profiling support)
    • Platform android-29, build-tools 29.0.2
    • Java binary at: /Applications/Android Studio.app/Contents/jre/jdk/Contents/Home/bin/java
    • Java version OpenJDK Runtime Environment (build 1.8.0_202-release-1483-b49-5587405)
    • All Android licenses accepted.

[✓] Xcode - develop for iOS and macOS (Xcode 11.2.1)
    • Xcode at /Applications/Xcode.app/Contents/Developer
    • Xcode 11.2.1, Build version 11B500
    • CocoaPods version 1.8.4

[✓] Android Studio (version 3.5)
    • Android Studio at /Applications/Android Studio.app/Contents
    • Flutter plugin version 42.1.1
    • Dart plugin version 191.8593
    • Java version OpenJDK Runtime Environment (build 1.8.0_202-release-1483-b49-5587405)

[✓] Connected device (1 available)
    • MI 5X • 1c7664100104 • android-arm64 • Android 8.1.0 (API 27)
    • iPhone 11 Pro Max • B366D105-9EEC-47E4-A0CE-94C43E9ACD2D • ios • com.apple.CoreSimulator.SimRuntime.iOS-13-2 (simulator)
```

#### 注意事项


- 高德地图定位失败可能是key导致的，使用者可以自己到高德地图开发者平台申请一个key再次试一试。
- Multi Image Picker 插件 ios 配置见[Multi Image Picker 使用](https://sh1d0w.github.io/multi_image_picker/#/gettingstarted)


- 项目中某些接口为http url，Android 9.0/P和iOS禁止从非https网址加载，故需更改 App 的网络安全配置以允许此类连接

__Android__

在 res 下新增一个 xml 目录，创建[network_security_config.xml](https://github.com/shichunlei/flutter_app/blob/master/android/app/src/main/res/xml/network_security_config.xml)文件

```xml
<?xml version="1.0" encoding="utf-8"?>
<network-security-config>
    <base-config cleartextTrafficPermitted="true" />
</network-security-config>
```

在[AndroidManifest.xml](https://github.com/shichunlei/flutter_app/blob/master/android/app/src/main/AndroidManifest.xml)文件下的application标签增加以下属性

```xml
<application

 android:networkSecurityConfig="@xml/network_security_config"

/>
```

__iOS__

在[Info.plist](https://github.com/shichunlei/flutter_app/blob/master/ios/Runner/Info.plist)下编辑

```
<key>NSAppTransportSecurity</key>
<dict>
    <key>NSAllowsArbitraryLoads</key>
    <true/>
    <key>NSAllowsArbitraryLoadsInWebContent</key>
    <true/>
</dict>
```


## API接口

- [豆瓣电影API接口>>](https://github.com/shichunlei/-Api/blob/master/%E8%B1%86%E7%93%A3%E7%94%B5%E5%BD%B1.md)

- [每日一文API接口>>](https://github.com/shichunlei/-Api/blob/master/OneArticle.md)

- [天气接口>>](https://www.heweather.com/documents/api/)

- [免费接口API>>](https://blog.csdn.net/qq_35695041/article/details/83024632)

- [好奇心日报接口>>](https://github.com/pkuhonker/qdaily/blob/master/src/services/apiService.ts)

- [好奇心日报接口>>](https://github.com/Urwateryi/QDailyNews/blob/master/app/network/Api.js)

- [追书神器接口>>](https://github.com/shichunlei/-Api/blob/master/%E8%BF%BD%E4%B9%A6%E7%A5%9E%E5%99%A8.md)

- [NBA接口](https://documenter.getpostman.com/view/8783043/SW7Z4p87?version=latest#84a6d27c-8be1-46f4-869a-c1c533f35742)

## 运行截图



### 仿腾讯体育NBA板块


|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1181574224573_.pic.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1231574224580_.pic.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1241574224582_.pic.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1291574224590_.pic.jpg)|
| :--: | :--: | :--: | :--: |
|赛程|排名|球员数据排名|球队数据排名|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1441574933325_.pic.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1221574224579_.pic.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1191574224574_.pic.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1281574224588_.pic.jpg)|
|球队数据|球队阵容|球队赛程|球队简介|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1421574933322_.pic.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1431574933324_.pic.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1211574224577_.pic.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1271574224587_.pic.jpg)|
|球员数据|球员生涯数据|球员比赛数据|球员简介|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1261574224586_.pic.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1251574224584_.pic.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1201574224576_.pic.jpg)|![4]()|
|球员新闻|球队新闻|同位置球员|XXX|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1351574327761_.pic.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1341574327759_.pic.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1331574327758_.pic.jpg)|![4]()|
|比赛详情-比分|比赛详情-球队数据统计|比赛详情-球员数据统计|XXX|



### [基本控件（Widget）及一些自定义控件（Widget）](https://github.com/shichunlei/flutter_app/blob/master/BASE_WIDGETS.md)


### 登录注册


|![1](https://upload-images.jianshu.io/upload_images/2774805-9b6c8ce1ba399665)|![2](https://upload-images.jianshu.io/upload_images/2774805-d577152c80806d50)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/1031566790595_.pic.jpg)|![4](https://raw.githubusercontent.com/Tecode/flutter_widget/master/picture/login_video_demo.gif)|
| :--: | :--: | :--: | :--: |
|登录|注册|找回密码|视频背景登录|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-06-15-08-33-15-313.png)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-06-15-08-33-27-977.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-06-15-08-33-40-821.png)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-06-15-08-33-35-147.png)|
|密码登录|快速登录|注册|找回密码|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/911565856636_.pic.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/921565856637_.pic.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-23-14-13-43-501.png)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-23-14-13-37-978.png)|
|登录|注册|登录|注册|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-23-14-21-40-361.png)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-23-14-21-52-446.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-23-14-21-45-940.png)|![4](https://github.com/pedromassango/my_flutter_challenges/raw/master/screenshots/slidl.gif)|
|---|注册|登录|登录/注册|


### [追书神器](http://m.zhuishushenqi.com/)


|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-23-44-265.png)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-14-20-422.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-14-30-696.png)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-23-39-352.png)|
| :--: | :--: | :--: | :--: |
| 登录 | 选择性别 | 选择兴趣爱好 | 我的 |
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-02-20-410.png)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-02-41-880.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-11-35-08-371.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/)|
| 书架（空） | 书架 | 书城 | 分类 |
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-11-35-39-277.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-11-36-04-409.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-11-44-50-515.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-01-53-767.jpg)|
| 排行 | 书单 | 书单详情 | 漫画 |
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-11-45-32-615.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-00-42-510.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-01-09-236.png)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-01-30-229.png)|
| 书籍详情1 | 书籍详情2 | 目录1 | 目录2 |
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-01-17-515.png)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-01-22-846.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-03-15-178.png)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-08-30-12-02-57-508.jpg)|
| 阅读 | 阅读设置 | 搜索 | 搜索结果 |


### [豆瓣电影](https://github.com/Mayandev/morec)

|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-03-31-09-16-35-569.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-03-31-09-16-49-010.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-03-31-09-16-58-888.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-01-30-15-13-51-495.jpg)|
| :--: | :--: | :--: | :--: |
|豆瓣电影首页（banner、热映）|豆瓣电影首页（即将上映、榜单）|豆瓣电影首页（分类浏览）|电影（正在热播）|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-10-17-17-22-35-128.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-10-17-17-22-27-284.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-10-17-17-22-07-528.png)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-10-17-17-22-20-433.jpg)|
|筛选（宫格）|筛选（列表）|筛选（地区）|筛选（条件）|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-10-18-16-49-23-728.png)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-10-18-16-48-41-191.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-10-18-16-48-55-570.png)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-10-18-16-49-08-187.png)|
|年度榜单|年度榜单|年度榜单|年度榜单|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-01-30-15-14-45-013.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-03-05-16-52-35-366.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-03-31-09-25-22-636.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-01-30-15-14-03-080.jpg)|
|电影详情1|电影详情2|电影详情3|电影（TOP250）|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-03-31-09-28-47-225.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-03-31-09-30-31-617.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-03-05-16-52-22-895.png)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-03-05-16-52-48-129.jpg)|
|电影花絮|电影花絮（全屏）|电影剧照|电影（排行榜）|


### [tubi TV](https://tubitv.com/) 可以免费看电影的APP（纯英文）

|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-11-01-17-12-53-856.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-11-01-17-13-32-265.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-11-01-17-13-07-523.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-11-01-17-13-21-054.jpg)|
| :--: | :--: | :--: | :--: |
|首页|分类列表|详情|搜索|


### 天气

|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-01-30-15-11-34-612.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-09-17-47-40-026.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-09-17-47-47-861.png)|
| :--: | :--: | :--: |
|实况天气/空气质量指数|逐小时、7天天气预报|生活指数|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-10-14-11-24-061.png)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-01-30-15-11-23-860.png)|![3](https://github.com/shichunlei/flutter_jd_address_selector/raw/master/images/Screenshot_2019-06-15-15-26-30-164.png)|
|日出日落|城市列表|[仿京东地址选择器](https://github.com/shichunlei/flutter_jd_address_selector)|



#### [百姓生活](https://github.com/shenghy/flutter_shop)

|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-19-20-22-33-602.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-19-20-22-46-698.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-19-20-22-54-706.jpg)|
| :--: | :--: | :--: |
|首页|首页|首页|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-23-19-16-25-496.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-26-15-38-33-468.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-23-17-35-34-333.jpg)|
|分类|购物车|会员中心|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-27-13-34-29-867.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-27-13-34-49-927.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-27-13-35-02-190.jpg)|
|商品简介|详情|评论|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-06-16-14-37-38-179.png)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-06-16-14-38-45-247.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-06-16-14-37-56-225.png)|
|收货地址|地址|新增地址|


### [每日一文](https://github.com/chengww5217/one_article)

|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-22-18-01-34-664.png)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-22-17-05-37-975.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-04-22-17-52-45-864.png)|
| :--: | :--: | :--: |
|每日一文|每日一文|收藏|


### [音乐播放器]()

|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-01-30-15-11-44-611.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-06-16-26-58-467.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-06-16-26-48-807.png)|
| :--: | :--: | :--: |
|Music Player|Audio Player|Flutter Sound|


### 仿微信朋友圈布局

|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-10-15-18-34-444.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-10-15-18-46-454.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-10-19-55-24-181.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-10-19-56-19-726.jpg)|
| :--: | :--: | :--: | :--: |
|头部|九宫格|选择照片|发表编辑|


### [句子迷](http://www.cnjxn.com)


|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-14-12-04-59-955.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-14-12-04-52-007.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-14-12-04-23-471.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-09-14-12-04-38-116.png)|
| :--: | :--: | :--: | :--: |
|启动页|列表页|详情（内容）|详情（推荐）|



### [好奇心日报](http://www.qdaily.com/)


|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-19-07-643.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-19-15-587.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-21-14-965.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-21-26-333.jpg)|
| :--: | :--: | :--: | :--: |
|启动页|首页1|首页2|首页3|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-21-34-258.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-21-52-988.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-22-02-810.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-06-02-15-23-22-164.jpg)|
|Labs|我说/焦点小组|投票|你猜/你谁啊|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-22-21-692.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-22-27-412.png)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-22-44-753.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-51-53-283.jpg)|
|菜单1|菜单2|栏目列表|栏目详情|
|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-22-34-621.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-31-16-59-16-833.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-31-17-32-53-185.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/Screenshot_2019-05-30-09-22-12-550.jpg)|
|分类列表（设计）|新闻详情1|新闻详情2|评论|


### [有道精品课](https://ke.youdao.com/)


|![1](https://github.com/shichunlei/flutter_app/blob/master/screenshots/961566204857_.pic.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/screenshots/971566204858_.pic.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/screenshots/981566204860_.pic.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/screenshots/991566204861_.pic.jpg)|
| :--: | :--: | :--: | :--: |
|首页（广告）|首页（分类）|分类|详情（WebView）|



### [Flutter i18n 实现国际化](https://github.com/shichunlei/flutter_app/wiki/Flutter-i18n-%E5%AE%9E%E7%8E%B0%E5%9B%BD%E9%99%85%E5%8C%96)


## [使用到的或推荐的一些优秀的第三方插件](https://github.com/shichunlei/flutter_app/blob/master/third_pubs.md)



## 赞赏

如果您喜欢FlutterApp，或感觉FlutterApp帮助到了您，可以点右上角“Star”支持一下，您的支持就是我的动力，谢谢🙂

您也可以扫描下面的二维码，请作者喝杯咖啡☕️


- 先领个红包

|![1](https://github.com/shichunlei/flutter_app/blob/master/admire-for/781564454769_.pic.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/admire-for/811564454769_.pic.jpg)|
| :--: | :--: |


|![1](https://github.com/shichunlei/flutter_app/blob/master/admire-for/771564454769_.pic.jpg)|![2](https://github.com/shichunlei/flutter_app/blob/master/admire-for/801564454769_.pic.jpg)|![3](https://github.com/shichunlei/flutter_app/blob/master/admire-for/761564454769_.pic_hd.jpg)|![4](https://github.com/shichunlei/flutter_app/blob/master/admire-for/821564454769_.pic.jpg)|
| :--: | :--: | :--: | :--: |


## 特别鸣谢


- [simplezhli/flutter_deer](https://github.com/simplezhli/flutter_deer)
- [jsososo/QQMusicApi](https://github.com/jsososo/QQMusicApi)
- [huanxsd/flutter_shuqi](https://github.com/huanxsd/flutter_shuqi)
- [fluttercandies/NeteaseCloudMusic](https://github.com/fluttercandies/NeteaseCloudMusic)
- [ditclear/tiktok_gestures](https://github.com/ditclear/tiktok_gestures)
- [Mayandev/morec](https://github.com/Mayandev/morec)
- [chengww5217/one_article](https://github.com/chengww5217/one_article)
- [shenghy/flutter_shop](https://github.com/shenghy/flutter_shop)



## 许可证

[Apache 2.0](https://github.com/shichunlei/flutter_app/blob/master/LICENSE)
