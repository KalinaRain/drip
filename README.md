# drip
安卓开发点滴记录
——安卓开发中的常用的库、view、widget以及一些知识总结

## 组件 
 
### 带小红点的提示：BadgeView 
- [BadgeView](https://github.com/stefanjauker/BadgeView)（stefanjauker的,改颜色需要在BadgeView源码里面改） 
- [android-viewbadger](https://github.com/jgilfelt/android-viewbadger)（可以设置提示为数字或者文字，以及背景颜色）  
  
### 圆形图片：CircleImageView
- [CircleImageView](https://github.com/hdodenhof/CircleImageView)（hdodenhof大神的，单纯的圆形IMageView，可以设置边框，目前还有一些限制）
- [RoundedImageView](https://github.com/vinc3m1/RoundedImageView)（椭圆或者圆角矩形皆可，可以设置边框）  
  
### 底部的导航栏：
- [BottomNavigationView](https://developer.android.com/reference/android/support/design/widget/BottomNavigationView.html)（官方design25.0.0之后才有的，compile 'com.android.support:design:25.0.0'，不过Tab样式好像比较少）
- [BottomNavigation](https://github.com/Ashok-Varma/BottomNavigation)（3-5个Item，可以设置Badges圆形消息提示和提示的背景颜色）
- [PagerBottomTabStrip](https://github.com/tyzlmjj/PagerBottomTabStrip)（可以设置Badge圆形消息提示和提示的背景颜色）
- 除了上述直接使用的库之外，还可以自己实现  
1.RadioGroup+ViewPage+Fragment  
2.FragmentTabHost+Fragment  
3.利用TextView+ImageView实现（不推荐，太麻烦了）  

### 滑动关闭页面

### BaseAdapter封装（listview、RecyclerView、GridView）
- [AdapterDelegates](https://github.com/sockeqwe/AdapterDelegates)（好复杂，以后再看）
- [baseAdapter](https://github.com/hongyangAndroid/baseAdapter)（Android 万能的Adapter for ListView,RecyclerView,GridView等，支持多种Item类型的情况）

### BaseProject封装

### 动画
- [recyclerview-animators](https://github.com/wasabeef/recyclerview-animators)（RecyclerView相关动画）

### 直播技术

### 弹幕
- [Barrage](https://github.com/OctavianLee/Barrage)（一个开源的b站直播间弹幕助手，主播可以获取直播间内弹幕信息且可以进行发送弹幕功能）
- [BarrageRenderer](https://github.com/unash/BarrageRenderer)（一个 iOS 上的开源弹幕渲染库）
- [DanmakuFlameMaster](https://github.com/Bilibili/DanmakuFlameMaster)（Bilibili的Android开源弹幕引擎·烈焰弹幕使）

### 加载动画LoadingView
- [AVLoadingIndicatorView](https://github.com/81813780/AVLoadingIndicatorView)（各式各样的ProgressBar）
- [NVActivityIndicatorView](https://github.com/ninjaprox/NVActivityIndicatorView)（各式各样的ProgressBar）

### 应用MVP模式的实用项目
- [TLint](https://github.com/gzsll/TLint)（虎扑体育 基于Dagger2+RxJava+Retrofit开发，采用MVP模式）
- [Hot](https://github.com/zj-wukewei/Hot)（MVP+Rxjava+Retrofit，是个微信头条的分享）