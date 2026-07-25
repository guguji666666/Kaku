# 隐私

Kaku 没有账号，也不采集使用数据。这一页列出 App 可能发起的全部网络请求。

## 概要

Kaku 是一个本地 macOS 应用。没有 Kaku 账号，没有注册，项目方没有任何接收你数据的服务器，也没有使用统计或崩溃上报。你的终端内容、命令历史和文件不会因为 Kaku 而离开这台机器。下面列出的是 App 唯一会建立网络连接的几种情况。

## App 会发起的网络请求

- **更新检查。**Kaku 会定期向 `api.github.com/repos/tw93/Kaku/releases/latest` 询问是否有新版本，你同意更新时再从 GitHub 下载发布包。对 GitHub 来说这就是一次来自你 IP 的普通 HTTPS 请求。在 `~/.config/kaku/kaku.lua` 里设 `config.check_for_updates = false` 可以关掉，用 `config.check_for_updates_interval_seconds` 可以改频率。
- **AI 助手。**用 `kaku ai` 开启 Kaku Assistant 后，prompt 直接发往你配置的 OpenAI 兼容端点，用的是你自己填的 API key。Kaku 不做代理、不中转、不记录、不留存，也没有默认服务商：不配置的话助手是完全静默的。该服务商如何处理你的 prompt，由它自己的隐私政策决定，不由 Kaku 决定。
- **可选工具安装。**`kaku init` 在安装 Starship、Delta、Lazygit、Yazi 这类缺失的可选工具前会先询问。你同意后由 Homebrew 完成下载，Kaku 本身不下载任何东西。
- **除此之外没有别的。**Kaku 不发心跳、不发安装 ping、不发功能使用事件、不发错误报告。

## 本机存了什么

Kaku 的状态都放在 `~/.config/kaku/` 下，包括 `kaku.lua`（你的 Lua 配置）、`assistant.toml`（助手设置，含你填入的 API key）、shell 集成文件，以及 `Cmd + L` 和 `kaku chat` 用到的 AI 对话与记忆文件。这些都是归你的用户账户所有的普通本地文件，目录里的内容不会上传到任何地方。

`kaku reset` 会移除 Kaku 托管的 shell 和 tmux 集成、Kaku 托管的 git delta 默认值、部分 Kaku 状态，以及托管的主题块，托管块以外你自己写的 Lua 会保留。想彻底清干净，删掉 `~/.config/kaku/` 和 `/Applications/Kaku.app` 即可。

## 关于本站

kaku.fun 是静态站点。不设 cookie，不跑统计或追踪脚本，不嵌第三方组件，没有登录。也不从第三方 CDN 加载字体、脚本或图片，所有资源都来自本域名。站点托管在 Vercel，作为基础设施方，Vercel 会按常规保留服务器访问日志（IP、User-Agent、请求路径）用于运维。指向 GitHub、X 等站点的外链，适用对方自己的政策。

## 疑问与变更

Kaku 是 MIT 开源的，本页每一条说法都可以拿 [github.com/tw93/Kaku](https://github.com/tw93/Kaku) 的代码核对。如果发现对不上，那就是 bug，欢迎[提 issue](https://github.com/tw93/Kaku/issues)。本页的实质性变更会写进对应版本的发布说明里。

最后核对版本：Kaku v0.14.0。

---

Source: https://kaku.fun/zh/privacy
Site index for LLMs: https://kaku.fun/llms.txt
