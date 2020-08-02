# 样式基本

theme 设置参照 figma 上的这个稿子

[theme](https://www.figma.com/file/yJ3PFv9EDH2LLok9ZTcWy0/Share-Kit-Moblie?node-id=567%3A22)

字体文件使用


![](https://s1.ax1x.com/2020/07/25/aSS3Dg.png)

其中 L M R 分别对应字重

# Theme

APP 的theme 命名规则和 figma 上稿子上的样式一至。

目前只提供了  default 一套 theme的颜色方案
```dart
FTheme.normal().themeAppLighter()
```

这样就可以获取某个颜色的值。

theme的配色方案放在  `theme_config.dart` 中，为一个配置对象：

![](https://s1.ax1x.com/2020/07/26/aSzexK.png)

详情见 [theme文档](./theme.md)


# 基础 UI 组件

### NormalPressWidget

**点击有按下颜色的通用组件**

*构造参数*

|参数名|含义|是否必传|
| ---| ---|---|
|onTap|点击回调|true|
|builder|UI构造|true|
|onLongPress|长按回调|false|
|color|组件本身的背景色|false|

### FHorizontalDivider & FVerticalDivider

横向或者竖向的分割线，分别需要设置宽度和高度

### 按钮

分为主要和次要

* PrimaryButton
* SecondaryButton


![](https://s1.ax1x.com/2020/08/01/a3rIzR.png)

支持：

* 设置宽高
* 设置标题
* 设置点击和长按的回调
* 设置是否disable
* 设置防抖时间，默认 1秒 内不会再响应重复点击

```dart
PrimaryButton(title: '主色按钮',
              height: 40,
              disable: !primaryEnable,
              width: MediaQuery.of(context).size.width*2/3,
              onPress: () {
                debugPrint('this is PrimaryButton');
              },

            ),
```



### AppBar

通用的固定样式 appbar

```
newCommonAppBar(BuildContext context, String title);
newCommonNotUpAppBar(BuildContext context, String title)// 不带返回按钮的
newActionAppBar(String title, List<Widget> actions) 后面带icon的
```

### 边距 Space

固定高度为 8

*SpaceWidget*