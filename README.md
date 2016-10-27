# drip
安卓开发点滴记录
——安卓开发中的常用的库、view、widget以及一些知识总结

[View与Widget](#1) | [动画](#2) | [开发常用](#3) | [架构相关](#4) | [安卓Base封装](#5) | [直播技术](#6)
 
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
- [CircleImageView](https://github.com/hdodenhof/CircleImageView)（hdodenhof大神的，单纯的圆形IMageView，可以设置边框，目前还有一些限制）
- [RoundedImageView](https://github.com/vinc3m1/RoundedImageView)（椭圆或者圆角矩形皆可，可以设置边框）  
  
### 流程指示器StepView
- [StepView](https://github.com/baoyachi/StepView)（横向和竖直方向的流程显示，可以用于订单或者物流等需要不同状态的场景）
- [Android-StepsView](https://github.com/anton46/Android-StepsView)（单纯的横向流程，可以设置颜色）  

### RecyclerView、ListView、GridView的封装
- [EasyRecyclerView](https://github.com/Jude95/EasyRecyclerView)（包含上拉加载和下拉刷新、EmptyView、showProgress、showError）
  
======================================================================
<h2 id="2">动画</h2>

### 加载进度条LoadingView
- [AVLoadingIndicatorView](https://github.com/81813780/AVLoadingIndicatorView)（各式各样的ProgressBar）
- [NVActivityIndicatorView](https://github.com/ninjaprox/NVActivityIndicatorView)（各式各样的ProgressBar）
  
### 动画
- [recyclerview-animators](https://github.com/wasabeef/recyclerview-animators)（RecyclerView相关动画）
  
======================================================================
<h2 id="3">开发常用</h2>

### 底部的导航栏：
- [BottomNavigationView](https://developer.android.com/reference/android/support/design/widget/BottomNavigationView.html)（官方design25.0.0之后才有的，compile 'com.android.support:design:25.0.0'，不过Tab样式好像比较少）
- [BottomNavigation](https://github.com/Ashok-Varma/BottomNavigation)（3-5个Item，可以设置Badges圆形消息提示和提示的背景颜色）
- [PagerBottomTabStrip](https://github.com/tyzlmjj/PagerBottomTabStrip)（可以设置Badge圆形消息提示和提示的背景颜色）
- 除了上述直接使用的库之外，还可以自己实现  
1.RadioGroup+ViewPage+Fragment  
2.FragmentTabHost+Fragment  
3.利用TextView+ImageView实现（不推荐，太麻烦了）  

### ViewPager相关
- [PageIndicatorView](https://github.com/romandanylyk/PageIndicatorView)（An page indicator for Android ViewPager）

### 滑动关闭页面
- []()（）
- []()（）
- []()（）
- []()（）
- []()（）
- []()（）
- []()（）

  
=============================================================================
<h2 id="4">架构相关</h2>

### 应用MVP模式的实用项目
- [TLint](https://github.com/gzsll/TLint)（虎扑体育 基于Dagger2+RxJava+Retrofit开发，采用MVP模式）
- [Hot](https://github.com/zj-wukewei/Hot)（MVP+Rxjava+Retrofit，是个微信头条的分享）
- [LookLook](https://github.com/xinghongfei/LookLook)（新闻阅读app）
- [Beam](https://github.com/Jude95/Beam)（MVP开发框架）
- [TheMVP](https://github.com/kymjs/TheMVP)（kymjs的一个新型MVP设计）
  

================================================================================
<h2 id="5">安卓Base封装</h2>

### BaseProject封装
- [BaseProject](https://github.com/zzkong/BaseProject)（基本项目框架，项目采用MVP+RxJAVA+Okhttp+Retrofit+dagger2实现。项目中带有最基本的BaseActivity，BaseFragment封装）
- [KJFrameForAndroid](https://github.com/kymjs/KJFrameForAndroid)（kymjs的一个开发框架，包含Bitmap与Http操作）
  
### BaseAdapter封装（listview、RecyclerView、GridView）
- [AdapterDelegates](https://github.com/sockeqwe/AdapterDelegates)（好复杂，以后再看）
- [baseAdapter](https://github.com/hongyangAndroid/baseAdapter)（Android 万能的Adapter for ListView,RecyclerView,GridView等，支持多种Item类型的情况）
  
==============================================================================
<h2 id="6">直播技术</h2>

### 直播技术
- [SmarterStreaming](https://github.com/daniulive/SmarterStreaming)（跨平台视频采集、直播SDK（支持私有协议和RTMP推流，如Windows推流/android推流/iOS推流/Windows播放/android播放/iOS播放），公网毫秒级延迟，也许是国内最靠谱的视频直播推流、播放SDK之一，助您轻松实现类似于花椒、映客、斗鱼手机直播推送与播放）
- [PLDroidPlayer](https://github.com/pili-engineering/PLDroidPlayer)（ Android 平台的音视频播放器 SDK，可高度定制化和二次开发）
- [ijkplayer](https://github.com/Bilibili/ijkplayer)（Bilibili的Android/iOS video player ）
- [pili-ijkplayer](https://github.com/pili-engineering/pili-ijkplayer)(pili-engineering的Android/iOS video player)

### 弹幕
- [Barrage](https://github.com/OctavianLee/Barrage)（一个开源的b站直播间弹幕助手，主播可以获取直播间内弹幕信息且可以进行发送弹幕功能）
- [DanmakuFlameMaster](https://github.com/Bilibili/DanmakuFlameMaster)（Bilibili的Android开源弹幕引擎·烈焰弹幕使）
- [BarrageRenderer](https://github.com/unash/BarrageRenderer)（一个 iOS 上的开源弹幕渲染库）
- [HJDanmakuDemo](https://github.com/panghaijiao/HJDanmakuDemo)（iOS系统上弹幕源码实现）