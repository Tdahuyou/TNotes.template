# [0013. Mindmap](https://github.com/tnotesjs/TNotes.docs/tree/main/notes/0013.%20Mindmap)

<!-- region:toc -->

- [1. 本节内容](#1-本节内容)
- [2. Mindmap 预览](#2-mindmap-预览)
- [3. 基本用法](#3-基本用法)
- [4. 设置根主题标题](#4-设置根主题标题)
  - [4.1. 围栏标题](#41-围栏标题)
  - [4.2. Markdown H1](#42-markdown-h1)
  - [4.3. 引用文件标题](#43-引用文件标题)
- [5. 控制默认展开层级](#5-控制默认展开层级)
- [6. 兼容旧写法](#6-兼容旧写法)
- [7. 相关链接](#7-相关链接)

<!-- endregion:toc -->

## 1. 本节内容

- 在 TNotes 笔记中使用 Mindmap 只读预览
- 设置根主题标题
- 控制默认展开层级
- 在脑图、大纲和源码视图之间切换

## 2. Mindmap 预览

TNotes 的 Mindmap 预览由 [`@tnotesjs/mindmap-core`][mindmap-core] 提供解析、数据模型和画布渲染能力，由 [`@tnotesjs/core`][core] 集成到 VitePress。

预览组件默认展示脑图视图，同时提供：

- **脑图**：支持平移、缩放、适应视口、折叠/展开、进入主题和打开链接。
- **大纲**：以只读树形大纲查看相同数据。
- **源码**：查看实际交给 `mindmap-core` 的规范化 Markdown。
- **主题同步**：亮色、暗色会自动跟随当前 VitePress 主题。

知识库中的预览是只读模式，不提供节点编辑、拖拽、删除、粘贴和格式修改。

## 3. 基本用法

推荐使用 `mindmap` 围栏，内容使用无序列表。没有 H1 时，组件会自动补充默认根主题 `root`。

输入：

<<< ./assets/1.md

输出：

```mindmap

- item1
- item2

```

## 4. 设置根主题标题

标题解析优先级为：

1. `mindmap` 围栏中的 `[title]`
2. `<<<` 文件引用后的 `[title]`
3. Markdown 内容中的 H1
4. 默认标题 `root`

### 4.1. 围栏标题

````md
```mindmap [项目架构]
- Web 应用
- VSCode 插件
- Core 预览
```
````

```mindmap [项目架构]
- Web 应用
- VSCode 插件
- Core 预览
```

### 4.2. Markdown H1

````md
```mindmap
# TNotes Mindmap

- mindmap-web
- mindmap-core
- mindmap-vscode
```
````

```mindmap
# TNotes Mindmap

- mindmap-web
- mindmap-core
- mindmap-vscode
```

### 4.3. 引用文件标题

使用 `<<< 文件路径 [title]` 导入外部 Markdown，并为导入内容指定根主题：

````md
```mindmap
<<< ./assets/2.md [学习计划]
```
````

```mindmap
<<< ./assets/2.md [学习计划]
```

如果引用中没有 `[title]`，则继续读取被导入文件中的 H1；文件也没有 H1 时使用 `root`。

## 5. 控制默认展开层级

围栏名称后的数字表示默认展示到第几级子节点，最小值为 `1`：

- `1`：展示根节点和一级子节点。
- `2`：展示根节点、一级子节点和二级子节点。
- `3`：继续展示到三级子节点，以此类推。

标题和层级可以组合使用，例如：

````md
```mindmap [学习计划] 1
<<< ./assets/2.md
```
````

一级展开：

```mindmap [学习计划] 1
<<< ./assets/2.md
```

二级展开：

```mindmap [学习计划] 2
<<< ./assets/2.md
```

## 6. 兼容旧写法

旧笔记无需立即迁移：

- 继续识别 `markmap` 围栏。
- 继续识别 `markmap 2`、`markmap {2}` 等旧层级写法。
- 继续识别 `<<< ./path/file.md` 文件引用。
- 旧内容中的 H2～H6 会按标题层级转换为嵌套主题。

新笔记统一推荐使用 `mindmap` 围栏。

## 7. 相关链接

- [`tnotesjs/mindmap-web`][mindmap-web]：可编辑的 Web 应用
- [`tnotesjs/mindmap-core`][mindmap-core]：Markdown 解析、数据模型与渲染引擎
- [`tnotesjs/core`][core]：TNotes/VitePress 集成层
- [Mindmap Web 在线版][mindmap-online]

[mindmap-web]: https://github.com/tnotesjs/mindmap-web
[mindmap-core]: https://github.com/tnotesjs/mindmap-core
[core]: https://github.com/tnotesjs/core
[mindmap-online]: https://tnotesjs.github.io/mindmap-web/
