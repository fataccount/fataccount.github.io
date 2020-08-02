# 样式搭建

样式在[https://www.figma.com/file/yJ3PFv9EDH2LLok9ZTcWy0/Share-Kit-Moblie?node-id=567%3A22](https://www.figma.com/file/yJ3PFv9EDH2LLok9ZTcWy0/Share-Kit-Moblie?node-id=567%3A22)<br />

<a name="6vjUM"></a>
## App颜色

<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/153347/1595673149624-ac0d2821-bcf9-4966-814b-c618803482b5.png#align=left&display=inline&height=337&margin=%5Bobject%20Object%5D&name=image.png&originHeight=674&originWidth=1254&size=66630&status=done&style=none&width=627)<br />
<br />状态颜色<br />
<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/153347/1595673184018-0c862d1f-cf20-40a2-9c0c-f4e900a7a22e.png#align=left&display=inline&height=485&margin=%5Bobject%20Object%5D&name=image.png&originHeight=970&originWidth=1712&size=191883&status=done&style=none&width=856)<br />
<br />透明度颜色<br />
<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/153347/1595673199151-b864f3b7-d51f-4448-8b46-ed22fd475281.png#align=left&display=inline&height=224&margin=%5Bobject%20Object%5D&name=image.png&originHeight=448&originWidth=866&size=27961&status=done&style=none&width=433)<br />
<br />![image.png](https://cdn.nlark.com/yuque/0/2020/png/153347/1595673210422-1249d1ab-3835-4b98-bb59-ba041019bafa.png#align=left&display=inline&height=326&margin=%5Bobject%20Object%5D&name=image.png&originHeight=652&originWidth=1824&size=64856&status=done&style=none&width=912)

字体颜色

![image.png](https://cdn.nlark.com/yuque/0/2020/png/153347/1595673225807-a6447873-0d12-41b4-ba48-a5abf6ecff3e.png#align=left&display=inline&height=233&margin=%5Bobject%20Object%5D&name=image.png&originHeight=466&originWidth=1654&size=44319&status=done&style=none&width=827)

<a name="dbxRU"></a>
## 实现方案


![image.png](https://cdn.nlark.com/yuque/0/2020/png/153347/1595693607266-71e5c052-678a-4953-984b-f8911ff4adda.png#align=left&display=inline&height=462&margin=%5Bobject%20Object%5D&name=image.png&originHeight=924&originWidth=1458&size=78258&status=done&style=none&width=729)

颜色配置全部放在一个配置文件的对象里面：

上面设计稿中每一部分的字段都会在enum 中配置，从enum的扩展方法中根据名字获取当前theme的颜色。

外层暴露一个 `FTheme` 对象，里面存储当前 theme 方案的名称（目前只有一套默认的 default）。

