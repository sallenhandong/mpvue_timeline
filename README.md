# sa_timeline

## 预览图
![sa_timeClass_Number](https://github.com/sallenhandong/mpvue_timeline/blob/master/1550732585(1).jpg)
![sa_timeClass_Dot](https://github.com/sallenhandong/mpvue_timeline/blob/master/1550732605(1).jpg)


## Feature
* 引入即用
* 根据需求在自定义颜色即可
## How to use?
 listArr: [
        {
          title: "setp 1",
          content: "开始记录今天的生活",
          id:'0',
          isSelect:'1'
        },
        {
          title: "setp 2",
          content: "Know that I will live in my heart 深知我者才久居我心。",
          id:'1',
           isSelect:'0'
        },{
          title: "setp 3",
          content: "To the time to life, rather than to life in time to the time to life, rather than to life in time.给时光以生命，而不是给生命以时光。",
          id:'2',
           isSelect:'0'
        },{
          title: "setp 4",
          content: "Whatever is worth doing is worth doing well.任何值得做的，就把它做好。",
          id:'2',
           isSelect:'0'
        },{
          title: "setp 5",
          content: "You may be out of my sight, but never out of my mind.你也许已走出我的视线，但从未走出我的思念。",
          id:'2',
           isSelect:'0'
        }
      ]
```
     <div v-for="(item, index) in listArr" :key="index">
            <timeLine :obj='item' :index='index' :maxLength='listArr.length' :saClass="'sa_timeClass_Dot'"></timeLine>
        </div>
```

> A Mpvue project

## Build Setup

``` bash
# 初始化项目
vue init mpvue/mpvue-quickstart myproject
cd myproject

# 安装依赖
yarn

# 开发时构建
npm dev

# 打包构建
npm build

# 指定平台的开发时构建(微信、百度、头条、支付宝)
npm dev:wx
npm dev:swan
npm dev:tt
npm dev:my

# 指定平台的打包构建
npm build:wx
npm build:swan
npm build:tt
npm build:my

# 生成 bundle 分析报告
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
