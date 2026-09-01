# [0010. Footprints](https://github.com/tnotesjs/TNotes.docs/tree/main/notes/0010.%20Footprints)

<!-- region:toc -->

- [1. 本节内容](#1-本节内容)
- [2. 足迹纪录组件如何使用？](#2-足迹纪录组件如何使用)

<!-- endregion:toc -->

## 1. 本节内容

这一节介绍 Footprints 组件的基本使用。

Footprints 组件是参考微信朋友圈的布局写的一个组件，基本就是个人的 TNotes.footprints 这个用于记录个人足迹的知识库在用。

由于微信 pyq 基本已经不再使用了（后续不确定啥时候才会再启用），目前（25.11）也已经关闭了有一两年了，因此做了这个组件，将所有个人朋友圈的动态搬运到了 TNotes.footprints 中。

## 2. 足迹纪录组件如何使用？

Footprints 是参照微信朋友圈的布局，自定义的一个用于记录个人动态的组件。用法其实很简单，使用 `::: footprints`  容器语法，后边儿跟个时间信息，表示这条记录发布的时间，然后就是文 + 图。

::: warning ⚠️ WARNING



:::

基本使用：

```md
::: footprints 2025-03-15 00:43

正在整理 TNotes.template 的功能文档

现在外边正下着小于雨 🌧️

不早了

写完这篇笔记就去睡觉了～

头发要紧

![](./assets/1.png)

![](./assets/2.png)

![](./assets/3.png)

![](./assets/4.jpg)

![](./assets/logo.png)

:::
```

最终渲染效果如下：

::: footprints 2025-03-15 00:43

正在整理 TNotes.template 的功能文档

现在外边正下着小于雨 🌧️

不早了

写完这篇笔记就去睡觉了～

头发要紧

![](./assets/1.png)

![](./assets/2.png)

![](./assets/3.png)

![](./assets/4.jpg)

![](./assets/logo.png)

:::
