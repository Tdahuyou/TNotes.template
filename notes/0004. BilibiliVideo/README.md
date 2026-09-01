# [0004. BilibiliVideo](https://github.com/tnotesjs/TNotes.docs/tree/main/notes/0004.%20BilibiliVideo)

<!-- region:toc -->

- [1. 本节内容](#1-本节内容)
- [2. 评价](#2-评价)
- [3. 如何嵌入 B 站视频呢？](#3-如何嵌入-b-站视频呢)
  - [3.1. 第一步：找到需要插入的视频](#31-第一步找到需要插入的视频)
  - [3.2. 第二步：获取需要插入视频的 BVID](#32-第二步获取需要插入视频的-bvid)
  - [3.3. 第三步：使用 `BilibiliVideo` 组件嵌入视频](#33-第三步使用-bilibilivideo-组件嵌入视频)
- [4. 引用](#4-引用)

<!-- endregion:toc -->

## 1. 本节内容

- `BilibiliVideo` 组件的使用说明

## 2. 评价

通过 `BilibiliVideo` 组件，可以实现在 TNotes 知识库笔记中嵌入 B 站视频。

用法非常简单，只需要获取到视频的 BVID 即可。

## 3. 如何嵌入 B 站视频呢？

### 3.1. 第一步：找到需要插入的视频

比如：https://www.bilibili.com/video/BV1QR4y1y7GG

### 3.2. 第二步：获取需要插入视频的 BVID

![img](https://cdn.jsdelivr.net/gh/tnotesjs/imgs@main/2025-10-03-21-59-57.png)

你可以在地址栏中看到 `BVID` --> `BV1QR4y1y7GG`

### 3.3. 第三步：使用 `BilibiliVideo` 组件嵌入视频

```md
<BilibiliVideo id="BV1QR4y1y7GG" />
```

最终渲染效果如下：

<BilibiliVideo id="BV1QR4y1y7GG" />

## 4. 引用

- [截图工具｜ snipaste 的使用分享][1]

[1]: https://www.bilibili.com/video/BV1QR4y1y7GG
