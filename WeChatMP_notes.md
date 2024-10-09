# 微信小程序开发



查看官方文档⇨：[developers.weixin.qq.com/miniprogram/dev/framework/](https://developers.weixin.qq.com/miniprogram/dev/framework/)

| 属性                                                         | 类型    | 必填 | 描述               |
| ------------------------------------------------------------ | ------- | ---- | ------------------ |
| page                                                         | string  | 是   | 页面路径列表       |
| window                                                       | object  | 否   | 全局默认窗口表现   |
| tabBar                                                       | object  | 否   | 底部tab栏的表现    |
| networktimeout                                               | object  | 否   | 网络超时时间       |
| debug                                                        | boolean | 否   | 是否开启调试模式   |
| [functionalPages](https://developers.weixin.qq.com/miniprogram/dev/reference/configuration/app.html#functionalPages) | Boolean | 否   | 是否启用插件功能页 |

用法：

"window":{ 

 "backgroundTextStyle" : "light",

 }

tabBar:

| 属性             | 类型   | 必填 | 说明                                                         |
| ---------------- | ------ | ---- | ------------------------------------------------------------ |
| pagePath         | string | 是   | 页面路径，必须在 pages 中先定义                              |
| text             | string | 是   | tab 上按钮文字                                               |
| iconPath         | string | 否   | 图片路径，icon 大小限制为 40kb，建议尺寸为 81px * 81px，不支持网络图片。**当** **position** **为** **top** **时，不显示 icon。** |
| selectedIconPath | string | 否   | 选中时的图片路径，icon 大小限制为 40kb，建议尺寸为 81px * 81px，不支持网络图片。**当** **position** **为** **top** **时，不显示 icon。** |



#### display:flex; 弹性布局 

flex-direction:  row ;  横向布局  clumn 竖向布局

flex-wrap: wrap ;flex-wrap 属性规定flex容器是单行或者多行，同时横轴的方向决定了新行堆叠的方向。。



onLoad : function ( ) { }页面加载完执行的一个函数



命名函数

 例如:<button bindtap="函数名"></button>

函数名 : function ( ) { },  函数语句

< block > < /block > 无意义标签



***API 接口：***

  微信：地理位置、扫码、拨打电话、手机震动。



***路由：***

wx.switchTab : 跳转到 tabBar 页面，并关闭其他所有非 tabBar 页面。只能跳转到 Tabbar 页面

wx.reLaunch : 关闭所有页面，打开到应用内的某个页面。

wx.redirectTo : 关闭当前页面，跳转到应用内的某个页面。但是不允许跳转到 tabbar 页面。

wx.navigateTo : 保留当前页面，跳转到应用内的某个页面。但是不能跳到 tabbar 页面。使用 [wx.navigateBack](https://developers.weixin.qq.com/miniprogram/dev/api/route/wx.navigateBack.html) 可以返回到原页面。小程序中页面栈最多十层。

wx.navigateBack : 关闭当前页面，返回上一页面或多级页面。可通过 [getCurrentPages](https://developers.weixin.qq.com/miniprogram/dev/reference/api/getCurrentPages.html) 获取当前的页面栈，决定需要返回几层。



**微信开发者工具 快捷键：**

``` scss

ctrl + shift + alt + P 			//打开命令面板

```



**微信小程序 js 笔记**：
``` js

// 在 js 里引用图片地址 
require('图片路径')
//在最新版本已经不需要了

//全局定义在app.js里
globalData: {
    userInfo: { 
        name:"王康", 
        sex:"男",
        birthday:"2002-12-04",    
        address:"山东省临沂市平邑县" 
    },
        Cur:0,
}
//在其他js页面中使用
const app = getApp()
//定义一个常量  
Page({  
    data:{  
        name : ' ' ,  
        name1 : ' '
    },
    onLoad(option) {
        console.log(app.globalData) //打印 gobaldata 数据 
    },   
    functionName( ) {  
        // 函数内容   
    },
})
    

//父组件向子组件传值
    //父组件wxml中
    <component value="我是一个值"/>
    //子组件 子组件js中写 
    Component({ 
        //组件的属性列表   
        properties:{    
            value:{ 
                type:Number,  //组件传过来的值的属性   
            }
        }
    })
	// 直接可以用 value 这个变量 
    
    
//子组件向传父组件传值
//子组件
    //子组件wxml中 
    <view bindtap="vlaue"></view>
    //子组件js中 
        value(){   
            let value = '一个值'  //定义一个要传的值  
            this.triggerEvent('value', value)     //通过triggerEvent将参数传给父组件 
        }
    
//父组件
    //父组件wxml中 
    <component bind:value="value"/>
    //父组件js中 
    value(e) {
        console.log(e)  //可以打印出子组件穿过来的值 
    }
    
```



### 小程序中rpx与px

**pt与px：**

- pt称为逻辑分辨率
- pt大小与屏幕分辨率有关系，简单可以理解为长度与视觉单位
- px是指物理分辨率，与屏幕尺寸没有关系

**rpx：**rpx(responsive pixel): 可以根据屏幕宽度进行自适应。规定屏幕宽为750rpx。如在 iPhone6 上，屏幕宽度为375px，共有750个物理像素，则750rpx = 375px = 750物理像素，1rpx = 0.5px = 1物理像素。

| 设备         | rpx换算px (屏幕宽度/750) | px换算rpx (750/屏幕宽度) |
| :----------- | :----------------------- | :----------------------- |
| iPhone5      | 1rpx = 0.42px            | 1px = 2.34rpx            |
| iPhone6      | 1rpx = 0.5px             | 1px = 2rpx               |
| iPhone6 Plus | 1rpx = 0.552px           | 1px = 1.81rpx            |

以iphone6的物理像素750*1334为视觉稿设计，在小程序中使用rpx为单位

在ip6下 1px = 1rpx = 0.5pt

使用rpx为单位小程序会在不同分辨率下进行转换，而px则不会

建议小程序的设计稿以750 x 1334 的物理分辨率进行设计

有的时候文字部分不适合用rpx来表示