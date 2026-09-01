# [0010. Footprints](https://github.com/tnotesjs/TNotes.docs/tree/main/notes/0010.%20Footprints)

<!-- region:toc -->

- [1. 本节内容](#1-本节内容)
- [2. 评价](#2-评价)
- [3. 足迹纪录组件如何使用？](#3-足迹纪录组件如何使用)

<!-- endregion:toc -->

## 1. 本节内容

- Footprints 组件的基本使用

## 2. 评价

Footprints 组件是参考微信朋友圈的布局写的一个组件，基本就是个人在用。

由于微信 pyq 基本已经不再使用了（后续不确定啥时候才会再启用），目前（25.11）也已经关闭了有一两年了，因此做了这个组件，将所有个人朋友圈的动态搬运到了 TNotes.footprints 中。

## 3. 足迹纪录组件如何使用？

参照微信朋友圈的布局，自定义的一个用于记录个人动态的组件。

从 `@tnotesjs/core@0.8.0` 起，使用 `::: footprints` 容器语法（不再支持旧的 `<Footprints>` Vue 标签）。

基本使用：

```md
🗓 3-15

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

🗓 3-15

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
