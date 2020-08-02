# 底部弹出的对话框

分为三种：

1. 直接底部弹出，可以放置滑动控件进行嵌套滑动，dialog出现的位置为minheight，可以上拉的最大高度为maxheight
2. 直接底部弹出，单一的widget包裹。点击阴影处取消
3. 直接底部弹出，可以配置一个route规则，在dialog内部进行页面之间的跳转


这3种分别对应三个不同的函数：

**draggableBottomSheetDialog**

|参数|含义|是否必传|备注|
|--|--|--|--|
|context||true|
|builder|构造widget|true||

**bottomSheetDialog**

|参数|含义|是否必传|备注|
|--|--|--|--|
|context||true|
|builder|构造widget|true||
|barrierColor|阴影颜色|false|不需要的时候可以传transparent|

调用如下：
![](https://s1.ax1x.com/2020/08/02/atO6Zn.png)

**bottomSheetDialogWithRoute**

|参数|含义|是否必传|备注|
|--|--|--|--|
|context||true|
|routes|路由表|true||
|arguments|打开对话框的参数|false||

*注意*

这里路由表里面传入的`Widget` 需要构造一个单纯的 Widget, 不可以带有 `Scaffold`, 否则会破坏Dialog本身的背景
