# drip
安卓开发 点滴记录（欢迎star和watch）

Android开发工程师面试知识整理：  
<a href="Android_Interview.md" target="_blank">Android面试知识点整理</a>（整理中）  

安卓开发中的常用的库、view、widget以及一些知识总结  
[View与Widget](#1) | [动画](#2) | [开发常用](#3) | [架构相关](#4) | [安卓Base封装](#5) | [直播技术](#6) | [实用插件](#7) | [Java深入](#8) |  
 
<h2 id="1">View与Widget</h2>

### 带小红点的提示：BadgeView 
- [BadgeView](https://github.com/stefanjauker/BadgeView)（stefanjauker的,改颜色需要在BadgeView源码里面改） 
- [android-viewbadger](https://github.com/jgilfelt/android-viewbadger)（可以设置提示为数字或者文字，以及背景颜色）  
  
### 标签tagview
- [TAGView](https://github.com/Jude95/TAGView)（可以设置背景图片的形状和颜色，可以同时显示图片和文字）
- [android-tagview](https://github.com/kaedea/android-tagview)（Android-Cloud-TagView-Plus，除了能设置标签的样式外，还能监听标签的点击和删除事件）
- [TagCloudView](https://github.com/kingideayou/TagCloudView)（支持 SingleLine 模式的标签云效果）
- [TagView](https://github.com/Cutta/TagView)（纯文字彩色标签，可以监听标签被选择和删除时的状态，可以单击删除）
- [android-tagview](https://github.com/VEINHORN/android-tagview)（含有箭头的彩色标签）
- [AndroidTagView](https://github.com/whilu/AndroidTagView)（可以添加和删除tag，监听单击和长按）  
- [EasyTagDragView](https://github.com/wenhuaijun/EasyTagDragView)(仿网易新闻app下拉标签选择菜单，长按拖动排序，点击增删标签控件)  

### 圆形图片：CircleImageView
- [CircleImageView](https://github.com/hdodenhof/CircleImageView)（hdodenhof大神的，单纯的圆形ImageView，可以设置边框，目前还有一些限制）
- [RoundedImageView](https://github.com/vinc3m1/RoundedImageView)（椭圆或者圆角矩形皆可，可以设置边框）  
- [CircleImageView](https://github.com/zuoweitan/CircleImageView)（使用clippath实现的CircleImageView,没有Bitmap,没有锯齿，可以设置其他的ScaleType）
  
### 流程指示器StepView
- [StepView](https://github.com/baoyachi/StepView)（横向和竖直方向的流程显示，可以用于订单或者物流等需要不同状态的场景）
- [Android-StepsView](https://github.com/anton46/Android-StepsView)（单纯的横向流程，可以设置颜色）  
  
### 可以展开的TextView：ExpandableTextView
- [ExpandableTextView](https://github.com/Chen-Sir/ExpandableTextView)（可以展开和收起的TextView，用于多文字显示）
- [ExpandableTextView](https://github.com/Manabu-GT/ExpandableTextView)（需要包含TextView和ImageView，感觉没有上面的方便，不过适合自定义单击的图片及其位置）
  
### ToggleButton
- [TriStateToggleButton](https://github.com/BeppiMenozzi/TriStateToggleButton)（具有三种状态的切换开关，也可以只两种状态，包含动画属性）
- [RMSwitch](https://github.com/RiccardoMoro/RMSwitch)（Android 两状态或者三状态Switch 按钮，可以设置按钮的图片，多样式）
- [Android-SwitchIcon](https://github.com/zagum/Android-SwitchIcon)（在自身图标上通过颜色的改变来显示关闭和开启的两种状态的switch控件）
  
### 日历
- [LightCalendarView](https://github.com/recruit-mp/LightCalendarView)（简洁风格的日历 View）
- [OneCalendarView](https://github.com/MorochoRochaDarwin/OneCalendarView)（该日历组件还是相当新颖的）
- [material-calendarview](https://github.com/prolificinteractive/material-calendarview)（日历组件，感觉UI和效果基本上和一些手机上原装的日历差不多）
  
### RecyclerView、ListView、GridView的封装
- [EasyRecyclerView](https://github.com/Jude95/EasyRecyclerView)（包含上拉加载和下拉刷新、EmptyView、showProgress、showError）
- [侧滑RecyclerView](http://www.jianshu.com/p/af9f940d8d1c)（含侧滑的RecyclerView）
- [excelPanel](https://github.com/zhouchaoyuan/excelPanel)（二维的RecyclerView，像excel表格,自带监听）
  
### dialog
- [material-dialogs](https://github.com/afollestad/material-dialogs)（对dialog很好的封装，不过使用教程比较多，接入略微复杂点）
- [FlycoDialog_Master](https://github.com/H07000223/FlycoDialog_Master)（有material design的，有多item的，也有ActionSheetDialog从屏幕底端弹出的那种，风格清晰，自带弹出与关闭动画，不过依赖有点多）  
- [NiftyDialogEffects](https://github.com/sd6352051/NiftyDialogEffects)（弹出的时候有各种动画）
  
### 漂亮的弧形顶部布局效果
- [ArcLayout](https://github.com/florent37/ArcLayout)（漂亮的弧形顶部布局效果）
  
### MusicPlayerView
- [Material_MusicPlayerView](https://github.com/amineghabi/Material_MusicPlayerView)（material design的音乐播放器）

### 密码解锁LockView
- [PatternLockView](https://github.com/aritraroy/PatternLockView)（漂亮的九宫格解锁）
- [LolliPin](https://github.com/OrangeGangsters/LolliPin)（为应用程序提供pin密码，包含数字和指纹识别）

### 评分
- [SmileyRating](https://github.com/sujithkanna/SmileyRating)（通过笑脸表情的变化来打分，挺有意思的）

***
<h2 id="2">动画</h2>

### 加载进度条LoadingView
- [AVLoadingIndicatorView](https://github.com/81813780/AVLoadingIndicatorView)（各式各样的ProgressBar）
- [NVActivityIndicatorView](https://github.com/ninjaprox/NVActivityIndicatorView)（各式各样的ProgressBar）
- [NumberProgressBar](https://github.com/daimajia/NumberProgressBar)（daimajia大神的带数字的横向ProgressBar）
  
### 动画
- [recyclerview-animators](https://github.com/wasabeef/recyclerview-animators)（RecyclerView相关动画）
- [AndroidViewAnimations](https://github.com/daimajia/AndroidViewAnimations)（daimajia大神的，各种动画，nice）
- [AndroidSwipeLayout](https://github.com/daimajia/AndroidSwipeLayout)（listview和RecyclerView的滑动删除、收藏）
- [lottie-android](https://github.com/airbnb/lottie-android)（该库可以通过Adobe After Effects做出动画效果然后导出为json文件，利用LottieAnimationView可以在安卓中加载为动画效果，不受限于安卓平台，动画效果可以很多）
- [Grav](https://github.com/glomadrian/Grav)（Android 粒子动画效果——多粒子运动）
  
### Toolbar
- [JellyToolbar](https://github.com/Yalantis/JellyToolbar)（果冻效果的Toolbar）

### 下拉刷新
- [FireworkyPullToRefresh](https://github.com/Cleveroad/FireworkyPullToRefresh)（带有烟花效果的下来刷新，不过背景素材有点单调）

***
<h2 id="3">开发常用</h2>
  
### 导航栏：
- [FlycoTabLayout](https://github.com/H07000223/FlycoTabLayout)（顶端和底部的导航栏，nice！自带indicator，可以设置数字或者小红点的消息提示，tab样式丰富-圆角矩形）
- [BottomNavigationView](https://developer.android.com/reference/android/support/design/widget/BottomNavigationView.html)（官方design25.0.0之后才有的，compile 'com.android.support:design:25.0.0'，不过Tab样式好像比较少）
- [BottomNavigation](https://github.com/Ashok-Varma/BottomNavigation)（3-5个Item，可以设置Badges圆形消息提示和提示的背景颜色，包含隐藏动画）
- [PagerBottomTabStrip](https://github.com/tyzlmjj/PagerBottomTabStrip)（可以设置Badge圆形消息提示和提示的背景颜色）
- 除了上述直接使用的库之外，还可以自己实现  
1.TabLayout+ViewPager（5.0之后推出的）  
2.RadioGroup+ViewPager+Fragment  
3.FragmentTabHost+Fragment  
4.利用TextView+ImageView实现（不推荐，太麻烦了）  

### 抽屉
- [SlidingRootNav](https://github.com/yarolegovich/SlidingRootNav)（类似以前QQ的侧边抽屉，会改变大小的那种）
- [ArcNavigationView](https://github.com/rom4ek/ArcNavigationView)（一个有弯曲边缘效果的NavigationView控件，不过我个人觉得可能有点反人类，大家见仁见智吧）

### ViewPager相关
- [PageIndicatorView](https://github.com/romandanylyk/PageIndicatorView)（An page indicator for Android ViewPager）
- [PagerSlidingTabStrip](https://github.com/jpardogo/PagerSlidingTabStrip)（Material Design风格，感觉和TabLayout实现的差不多）
- [ViewPagerIndicator](https://github.com/JakeWharton/ViewPagerIndicator)（很久的了，我觉得官方新出的一些都比这个好）
- [UltraViewPager](https://github.com/alibaba/UltraViewPager)（UltraViewPager是一个封装多种特性的ViewPager，支持横向滑动／纵向滑动,支持一屏内显示多页,循环滚动,定时滚动和页面切换动效）

### CoordinatorTabLayout
- [CoordinatorTabLayout](https://github.com/hugeterry/CoordinatorTabLayout)（可以快速实现TabLayout和CoordinatorLayout的组合效果）

### 滑动关闭页面
- [SwipeBackLayout](https://github.com/ikew0ng/SwipeBackLayout)（从上下左右四个方向滑动关闭Activity，可以设置首页不滑动 setSwipeBackEnable(false)，不过activity需要设置透明主题）
- [SlideBackLayout](http://blog.csdn.net/meijian531161724/article/details/50763931)（不需要继承什么，只是初始化并bind）
- [SwipeBackHelper](https://github.com/Jude95/SwipeBackHelper)（Jude95的，在activity的生命周期中调用相应的方法，好像对图层渲染的压力小点，有机会研究下）
- [SwipeBack](https://github.com/liuguangqiang/SwipeBack)（liuguangqiang的，四个方向滑动关闭，不过xml根目录好像必须要是SwipeBackLayout ）
- [SwipeBack](https://github.com/sockeqwe/SwipeBack)（需要和ViewPager的滑动区分下）
- [SwipeBackFragment](https://github.com/YoKeyword/SwipeBackFragment)（滑动Fragment&Activity边缘可以返回）

### 多Fragment使用
- [Fragmentation](https://github.com/YoKeyword/Fragmentation)（为"单Activity ＋ 多Fragment","多模块Activity + 多Fragment"架构而生，大大简化使用过程，轻松解决各种复杂嵌套等问题，修复了官方Fragment库中存在的一些BUG）
  
### 图片选择器
- [MediaPickerInstagram](https://github.com/NodensN/MediaPickerInstagram)（Material风格的类似 Instagram 的图片选择器，包含图片选择、拍照、视频拍摄）
- [AwesomeImagePicker](https://github.com/myinnos/AwesomeImagePicker)（Material风格的图片选择器，包括图片和gif，能够多选）
- [Album](https://github.com/yanzhenjie/Album)（图片选择器，在底部可以选择文件夹）
- [boxing](https://github.com/Bilibili/boxing)（boxing是B站出品的一个多媒体选择器库，可以选择一张或者多张图片，提供预览和裁剪功能。同样支持gif图，选择视频和图像压缩功能。）
  
### 加载（过程、失败）
- [stateLayout](https://github.com/fingdo/stateLayout)（加载的替换layout，可以替换layout中的内容，类似于EmptyView之类的）
  
### 管理库
- [spruce-android](https://github.com/willowtreeapps/spruce-android)（动画管理库）
  
### 压缩
- [CompressHelper](https://github.com/nanchen2251/CompressHelper)（压缩文件，压缩图片，压缩后清晰度还不错）

### 指纹
- [FingerprintManager](https://github.com/JesusM/FingerprintManager)（安卓的指纹管理工具）

### 二维码
- [ZXing](https://github.com/zxing/zxing)（ZXing是由谷歌出品的对条码和二维码的解析工具，呗广泛使用）
- [PressScanCode](https://github.com/BolexLiu/PressScanCode)（一个长按扫描 View 上的二维码的工具库，类似于微信的长按识别二维码）

### 三维效果
- [Isometric](https://github.com/FabianTerhorst/Isometric)（能构建出三维图效果，但是对坐标的要求比较高，最好是有点基础的人使用）

### app shortcuts
- [shortbread](https://github.com/MatthiasRobbers/shortbread)（自Android 7.0后，用户可以长按桌面图标弹出快捷菜单，该库可以帮助开发者快速开发app shortcuts）
  
### 著名开源库
- [vlayout](https://github.com/alibaba/vlayout)（阿里巴巴开源的项目——VirtualLayout是一个针对RecyclerView的LayoutManager扩展, 主要提供一整套布局方案和布局间的组件复用的问题。说白了就是对复杂布局的解决方案）
- [atlas](http://atlas.taobao.org/index.html)（带你重返App开发的田园时代——其实就是为开发者解决繁杂的业务关系和一些迭代与集成问题，总之，挺厉害的）
- 数据库相关：[android-lite-orm](https://github.com/litesuits/android-lite-orm)、[ORMLite](http://ormlite.com/)、[sugar](https://github.com/satyan/sugar)、[greenDAO](http://greenrobot.org/greendao/documentation/)、[Realm](https://realm.io/)、[activeandroid](http://www.activeandroid.com/)、[LitePal](https://github.com/LitePalFramework/LitePal)

***
<h2 id="4">架构相关</h2>

### 应用MVP模式的实用项目
- [TLint](https://github.com/gzsll/TLint)（虎扑体育 基于Dagger2+RxJava+Retrofit开发，采用MVP模式）
- [Hot](https://github.com/zj-wukewei/Hot)（MVP+Rxjava+Retrofit，是个微信头条的分享）
- [LookLook](https://github.com/xinghongfei/LookLook)（新闻阅读app）
- [Beam](https://github.com/Jude95/Beam)（MVP开发框架）
- [TheMVP](https://github.com/kymjs/TheMVP)（kymjs的一个新型MVP设计）
- [Espresso](https://github.com/TonnyL/Espresso)（基于MVP架构和Material Design设计风格，采用RxJava2, Retrofit2, Realm and ZXing开发的快递查询App）
  
### 实战项目
- [bilibili-android-client](https://github.com/HotBitmapGG/bilibili-android-client)（非官方的bilibili客户端，抓去的ios的接口，整体封装不错，适合新入手的同学）

***
<h2 id="5">安卓Base封装</h2>

### BaseProject封装
- [BaseProject](https://github.com/zzkong/BaseProject)（基本项目框架，项目采用MVP+RxJAVA+Okhttp+Retrofit+dagger2实现。项目中带有最基本的BaseActivity，BaseFragment封装）
- [KJFrameForAndroid](https://github.com/kymjs/KJFrameForAndroid)（kymjs的一个开发框架，包含Bitmap与Http操作）
  
### BaseAdapter封装（listview、RecyclerView、GridView）
- [AdapterDelegates](https://github.com/sockeqwe/AdapterDelegates)（好复杂，以后再看）
- [baseAdapter](https://github.com/hongyangAndroid/baseAdapter)（Android 万能的Adapter for ListView,RecyclerView,GridView等，支持多种Item类型的情况）
  
***
<h2 id="6">直播技术</h2>

### 直播技术
- [SmarterStreaming](https://github.com/daniulive/SmarterStreaming)（跨平台视频采集、直播SDK（支持私有协议和RTMP推流，如Windows推流/android推流/iOS推流/Windows播放/android播放/iOS播放），公网毫秒级延迟，也许是国内最靠谱的视频直播推流、播放SDK之一，助您轻松实现类似于花椒、映客、斗鱼手机直播推送与播放）
- [PLDroidPlayer](https://github.com/pili-engineering/PLDroidPlayer)（ Android 平台的音视频播放器 SDK，可高度定制化和二次开发）
- [ijkplayer](https://github.com/Bilibili/ijkplayer)（Bilibili的Android/iOS video player ）
- [pili-ijkplayer](https://github.com/pili-engineering/pili-ijkplayer)(pili-engineering的Android/iOS video player)
- [PreviewSeekBar](https://github.com/rubensousa/PreviewSeekBar)（看视频时，拖动进度条可以预览当前帧的画面）

### 弹幕
- [Barrage](https://github.com/OctavianLee/Barrage)（一个开源的b站直播间弹幕助手，主播可以获取直播间内弹幕信息且可以进行发送弹幕功能）
- [DanmakuFlameMaster](https://github.com/Bilibili/DanmakuFlameMaster)（Bilibili的Android开源弹幕引擎·烈焰弹幕使）
- [BarrageRenderer](https://github.com/unash/BarrageRenderer)（一个 iOS 上的开源弹幕渲染库）
- [HJDanmakuDemo](https://github.com/panghaijiao/HJDanmakuDemo)（iOS系统上弹幕源码实现）
  
  
***
<h2 id="7">实用插件</h2>

### Android Studio插件
- [JRebel](https://zeroturnaround.com/software/jrebel-for-android/features/)（Android 高效开发调试神器 JRebel，效率比Instant Run高且稳定）
- [here-be-dragons](https://github.com/anupcowkur/here-be-dragons)（用注解把那些恶心的，或者有 Hack 功能的代码标注出来，每次调用时 IDE 都会提醒这个函数调用有潜在风险）
- [ButterKnife Zelezny](https://github.com/avast/android-butterknife-zelezny)（对应ButterKnife 的插件，方便开发者快速实例化view）

### 安全相关
- [condom](https://github.com/oasisfeng/condom)（一个超轻超薄的Android工具库，阻止三方SDK中常见的严重影响用户体验的『链式唤醒』行为。（对应用自身的功能无影响））

### 其它
- [AdaptiveTableLayout ](https://github.com/Cleveroad/AdaptiveTableLayout)（可以对CSV 文件加载和预览，行和列都可以拖拽）
- [LogUtils](http://www.jianshu.com/p/b806d014162c)（日志工具类）
- [AppMethodOrder](https://github.com/zjw-swun/AppMethodOrder)（能了解所有函数调用顺序的Android库，很牛逼的说）
- [awesome-ocr](https://github.com/wanghaisheng/awesome-ocr)（文字识别）
- [BlockCanaryEx](https://github.com/seiginonakama/BlockCanaryEx)（记录线程和每个线程函数执行时间，从而找到影响效率的地方）
  
***
<h2 id="8">java深入</h2>

### java深入
- [探索 Java 隐藏的开销](https://realm.io/cn/news/360andev-jake-wharton-java-hidden-costs-android/)
- [java反射](http://www.cnblogs.com/zhaoyanjun/p/6074887.html)
- [开源 Java 性能监控 （APM） 方案](https://github.com/naver/pinpoint)
  
***
<h2 id="9">Android深入</h2>
  
### Android深入
- [深入Android渲染机制](http://blog.csdn.net/ccj659/article/details/53219288)
- [java反射](http://www.cnblogs.com/zhaoyanjun/p/6074887.html)
