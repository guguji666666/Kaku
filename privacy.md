# Privacy

Kaku has no account and collects no usage analytics. This page lists every network call the app can make.

## Summary

Kaku is a local macOS application. There is no Kaku account, no sign-up, no server operated by the project that receives your data, and no usage or crash analytics. Your terminal contents, command history, and files never leave your machine because of Kaku. Everything below describes the only situations in which the app opens a network connection.

## Network calls the app makes

- **Update check.** Kaku periodically asks `api.github.com/repos/tw93/Kaku/releases/latest` whether a newer version exists, and downloads the release archive from GitHub when you accept an update. GitHub sees the request as a normal HTTPS request from your IP address. Turn it off with `config.check_for_updates = false` in `~/.config/kaku/kaku.lua`, or change the frequency with `config.check_for_updates_interval_seconds`.
- **AI assistant.** When you enable Kaku Assistant with `kaku ai`, prompts go directly to the OpenAI-compatible endpoint you configured, using the API key you supplied. Kaku does not proxy, relay, log, or retain these requests, and there is no default provider: the assistant is inert until you configure one. What that provider does with your prompts is governed by its own privacy policy, not by Kaku.
- **Optional tool install.** `kaku init` asks before installing missing optional tools such as Starship, Delta, Lazygit, and Yazi. If you agree, Homebrew performs the download; Kaku itself fetches nothing.
- **Nothing else.** Kaku sends no heartbeat, no install ping, no feature usage events, and no error reports.

## What is stored on your machine

Kaku keeps its state under `~/.config/kaku/`. That includes `kaku.lua` (your Lua configuration), `assistant.toml` (assistant settings, including the API key you entered), shell integration files, and the AI chat conversation and memory files used by `Cmd + L` and `kaku chat`. These are plain local files owned by your user account. Nothing in this directory is uploaded anywhere.

Run `kaku reset` to remove Kaku-managed shell and tmux integration, Kaku-managed git delta defaults, selected Kaku state, and managed theme blocks. Lua you wrote yourself outside the managed blocks is preserved. To remove everything, delete `~/.config/kaku/` and `/Applications/Kaku.app`.

## This website

kaku.fun is a static site. It sets no cookies, runs no analytics or tracking scripts, embeds no third-party widgets, and has no login. It loads no fonts, scripts, or images from third-party CDNs; every asset comes from this domain. The site is hosted on Vercel, which keeps standard server request logs (IP address, user agent, requested path) for operational purposes as its infrastructure provider. Links out to GitHub, X, and other sites are governed by those sites' own policies.

## Questions and changes

Kaku is MIT licensed and fully open source, so every claim on this page can be checked against the code at [github.com/tw93/Kaku](https://github.com/tw93/Kaku). If you find a discrepancy, that is a bug: please [open an issue](https://github.com/tw93/Kaku/issues). Material changes to this page will be described in the release notes for the version they ship with.

Last reviewed for Kaku v0.14.0.

---

Source: https://kaku.fun/privacy
Site index for LLMs: https://kaku.fun/llms.txt
