# 关于 Kaku

一个开箱即用的快速 macOS 终端，为 AI 编码而生，由一个人在公开环境中开发。

## Kaku 是什么

Kaku 是基于 [WezTerm](https://wezterm.org) 深度定制的 macOS 原生终端，面向 AI 辅助的终端工作调优。它保留了上游的速度和完整 Lua 配置能力，把二进制体积压掉约 40%，并预置了一套有主张的默认值，让 App 装完即可用：JetBrains Mono、macOS 级字体渲染、跟随系统的深浅色主题、走原生 macOS 快捷键的标签页与分屏，以及已经配好的 Lazygit、Yazi、远程文件、z、补全和语法高亮。

名字取自日语 書く（kaku），意为"书写"，把想法落成形状。Kaku 属于同一作者的一个小家族：Kaku 写代码，[Waza](https://github.com/tw93/Waza)（技）练习惯，[Kami](https://github.com/tw93/Kami)（紙）做文档。

## 谁在做

Kaku 由独立开发者 Tw93 开发，他也是 [Pake](https://github.com/tw93/Pake) 和 [Mole](https://github.com/tw93/Mole) 的作者。开发全程公开在 GitHub 上：issue、PR、发布和路线图都能看到，源码 MIT 开源。Kaku 背后没有公司，没有销售，也没有企业版。支持渠道是 [GitHub Issues](https://github.com/tw93/Kaku/issues)，项目靠自愿的 [GitHub Sponsors](https://github.com/sponsors/tw93) 维持，而不是靠产品本身收费。

## Kaku 刻意不做什么

- **不是账号产品。**没有注册、没有登录、没有云端中转，装上就能用。
- **不做埋点。**Kaku 不采集使用数据，App 会发起的网络请求全部列在[隐私](https://kaku.fun/zh/privacy)页面。
- **不是 AI 服务。**内置助手只和你用 `kaku ai` 配好的 OpenAI 兼容端点通信，Kaku 不会把你的 prompt 经由自己的服务器转发。
- **暂不跨平台。**目前只支持 macOS，Windows 和 Linux 未支持，也不承诺时间表。
- **不收费。**Kaku 免费且 MIT 开源，没有付费档位，也没有用量限制。

## 怎么用这个站点

每个页面都有 markdown 孪生版本：在任意 URL 后面加 `.md`，或者请求头带 `Accept: text/markdown`，拿到的是去掉页面外壳的同一份正文。[llms.txt](https://kaku.fun/llms.txt) 是精简索引，[llms-full.txt](https://kaku.fun/llms-full.txt) 是给语言模型和答案引擎用的完整单文件说明。

可以从[文档](https://kaku.fun/zh/docs/)开始，用[路线图](https://kaku.fun/zh/roadmap)了解正在做什么，或者[联系我们](https://kaku.fun/zh/contact)。

---

Source: https://kaku.fun/zh/about
Site index for LLMs: https://kaku.fun/llms.txt
