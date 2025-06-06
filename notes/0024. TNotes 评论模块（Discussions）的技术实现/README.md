# [0024. TNotes 评论模块（Discussions）的技术实现](https://github.com/Tdahuyou/TNotes.introduction/tree/main/notes/0024.%20TNotes%20%E8%AF%84%E8%AE%BA%E6%A8%A1%E5%9D%97%EF%BC%88Discussions%EF%BC%89%E7%9A%84%E6%8A%80%E6%9C%AF%E5%AE%9E%E7%8E%B0)

<!-- region:toc -->

- [1. 💭 TNotes 评论模块（Discussions）的技术实现](#1--tnotes-评论模块discussions的技术实现)

<!-- endregion:toc -->

## 1. 💭 TNotes 评论模块（Discussions）的技术实现

- 评论功能是基于 [Giscus](https://giscus.app/zh-CN) 实现的。
- Giscus 是基于 GitHub Discussions 的评论系统。
- 用户通过 GitHub 登录后可以发表评论，评论会同步到你指定的 GitHub Discussion 中。
- 优点：
  - 免费，易于集成。
  - 评论内容存储在 GitHub 对应仓库的 Discussions 中，不需要服务器。
  - 支持 Markdown，SEO 友好。
- 缺点：
  - 发布评论的前提是得有 GitHub 账号。
  - Giscus 提供的输入框不支持直接上传附件，如果要上传图片等 `📎 附件资源` 需要通过原生的 Discusstions 来发。
    - ![图 0](https://cdn.jsdelivr.net/gh/Tdahuyou/imgs@main/2025-06-02-19-11-51.png)
    - ![图 1](https://cdn.jsdelivr.net/gh/Tdahuyou/imgs@main/2025-06-02-19-12-01.png)
    - 在发布图片的时候，如果已经有了图片的超链接地址，那么可以直接采用 markdown 语法来发布。
- 集成步骤：
  1. 前往 [Giscus](https://giscus.app/) 配置页面。
  2. 填入你的 GitHub 仓库信息，选择是否使用 Discussions。
  3. 根据配置生成一段代码，将其添加到 VitePress 的 `themeConfig` 或自定义组件中。
  4. 发布后即可启用评论。
