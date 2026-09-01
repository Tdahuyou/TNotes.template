# [0012. Mermaid](https://github.com/tnotesjs/TNotes.docs/tree/main/notes/0012.%20Mermaid)

<!-- region:toc -->

- [1. 本节内容](#1-本节内容)
- [2. mermaid 组件如何使用？](#2-mermaid-组件如何使用)
- [3. 引用](#3-引用)

<!-- endregion:toc -->

## 1. 本节内容

本节是 Mermaid 组件的基本使用，vitepress 默认是不带有 mermaid 支持的，但是又经常有绘制图表的需求，因此集成了 mermaid 功能。

## 2. mermaid 组件如何使用？

和 [mermaid][1] 要求的语法一致。

输入：

````md
```mermaid
flowchart LR
  Start --> Stop
```
````

输出：

```mermaid
flowchart LR
  Start --> Stop
```

会在鼠标悬停在图表上时，显示相关控制按钮：

![image](https://cdn.jsdelivr.net/gh/tnotesjs/imgs-2026@main/26-09-01-16-03-34.png)

## 3. 引用

- [mermaid.org 官方文档][1]

[1]: https://mermaid.js.org/
