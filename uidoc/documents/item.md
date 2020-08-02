
# item普通项组件

item组件支持几种类型：

![](https://s1.ax1x.com/2020/08/01/aGs71H.png)

* 左侧显示文字的纯文本类型
* 左边右边都是文字
* 左边右边文字+右边引导箭头
* 左边文字 右边是图片+引导箭头

这些分别对应：

*LTItemWidget*

|参数|含义|是否必传|备注|
|--|--|--|--|
|l|左边标题|false||
|lColor|左边标题颜色|false|默认文字主题色|
|tap|点击事件|false||


*LTRTItemWidget*

|参数|含义|是否必传|备注|
|--|--|--|--|
|l|左边标题|false||
|lColor|左边标题颜色|false|默认文字主题色|
|r|右边文字内容|false|默认文字副主题色||
|rColor|左边标题颜色|false|默认文字主题色|
|tap|点击事件|false||

*LTRTAItemWidget*

|参数|含义|是否必传|备注|
|--|--|--|--|
|l|左边标题|false||
|lColor|左边标题颜色|false|默认文字主题色|
|r|右边文字内容|false|默认文字副主题色||
|rColor|左边标题颜色|false|默认文字主题色|
|tap|点击事件|false||

*LTRIAItemWidget*

|参数|含义|是否必传|备注|
|--|--|--|--|
|l|左边标题|false||
|lColor|左边标题颜色|false|默认文字主题色|
|iconUrl|图片的uri|false|如果是http开头会加载网络图片，否则默认加载assets文件|
|tap|点击事件|false||