# 仿网易严选小程序————简易版
- 在此声明本项目归网易所有， 只做学习所用， 请尊重原厂版权

- 本项目虽然引入了vant组件库 但是百分之九十以上还是使用的自定义组件（个人认为第一次做项目还是得自己多练练手才行） 

- 解构本项目实现功能
  - 首页功能介绍
  1. 自定义顶部导航 实现了滚动控制导航栏的功能栏变化
      细节1： 自定义导航数据和微信系统完全一致 数据精准   可以通过wx自身提供的api获取
      细节2： 功能栏显示为品牌图片时不提供跳转到搜索页面的功能   显示为搜索栏时提供跳转功能
      细节3： 功能栏的搜索栏并没有直接做成和主页主体的搜索栏的样式 而是做成其他页面需要的顶部搜索栏基础样式 
                目的是方便其他页面复用  主页页面可以通过对基础样式进一步修改达到和主页搜索栏一致
  2. 搜索栏轮播功能  自动轮播+跳转  跳转可以用 navgator标签来实现(小程序用该标签代替了a标签) 或者可以绑定点击事件 通过wx.navigateTo实现
      细节1：自动轮播时默认允许手动滑动轮播内容显然是不好的行为 所以这里使用 catchtouchmove定义一个事件来禁止该行为
  3. 图片滚动栏  在滚动栏下方 创造了一个滑块框  通过滚动图片来同步显示移动变化效果
      细节1： 数据驱动 跟随图片数据自动同步滑块长度  通过计算比例得到滑块滑动距离  不能把数据写死# wyyx
