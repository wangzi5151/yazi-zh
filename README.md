> 🌏 **简体中文** | [English](https://github.com/sxyazi/yazi)
>
> 本仓库是 [sxyazi/yazi](https://github.com/sxyazi/yazi) 官方 README 的非官方简体中文翻译，仅供学习交流。
> 原项目采用 MIT 许可证，本翻译遵循相同许可证。翻译可能滞后于原文，请以[英文原版](https://github.com/sxyazi/yazi)为准。

<div align="center">
	<sup>特别鸣谢：</sup><br>

| <a href="https://go.warp.dev/yazi" target="_blank"><img alt="Warp sponsorship" width=350 src="https://github.com/warpdotdev/brand-assets/blob/main/Github/Sponsor/Warp-Github-LG-02.png"><br><b>Warp, built for coding with multiple AI agents</b><br><sup>Available for macOS, Linux and Windows</sup></a> |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

</div>

## Yazi - ⚡️ 极速终端文件管理器

Yazi（意为 "duck"，鸭子）是一款用 Rust 编写的终端文件管理器，基于非阻塞异步 I/O。它致力于提供高效、易用、可定制的文件管理体验。

💡 一篇讲解其内部原理的新文章：[为什么 Yazi 这么快？](https://yazi-rs.github.io/blog/why-is-yazi-fast)

- 🚀 **全异步支持**：所有 I/O 操作都是异步的，CPU 任务分散到多个线程执行，充分利用可用资源。
- 💪 **强大的异步任务调度与管理**：提供实时进度更新、任务取消和内部任务优先级分配。
- 🖼️ **内置多种图片协议支持**：同时集成了 Überzug++ 与 Chafa，覆盖几乎所有终端。
- 🌟 **内置代码高亮与图片解码**：配合预加载机制，大幅加快图片和普通文件的加载速度。
- 🔌 **并发插件系统**：UI 插件（可重写大部分界面）、功能插件、自定义预览器 / 预加载器 / 定位器 / 抓取器；只需几段 Lua 代码。
- ☁️ **虚拟文件系统**：远程文件管理、自定义 VFS 提供者、自定义搜索引擎。
- 📡 **数据分发服务**：基于客户端-服务器架构（无需额外的服务器进程），集成基于 Lua 的发布-订阅模型，实现跨实例通信与状态持久化。
- 📦 **包管理器**：一条命令安装插件和主题，保持更新，或锁定到指定版本。
- 🧰 与 ripgrep、fd、fzf、zoxide、[Rclone](https://github.com/yazi-rs/plugins/tree/main/rclone.yazi) 集成
- 💫 类 Vim 的输入 / 选择 / 确认 / 快捷键提示 / 通知组件，cd 路径自动补全
- 🏷️ 多标签页支持、跨目录选择、可滚动预览（视频、PDF、压缩包、代码、目录等）
- 🔄 批量重命名 / 创建、解压、Visual 模式、文件选择器、[Git 集成](https://github.com/yazi-rs/plugins/tree/main/git.yazi)、[挂载管理器](https://github.com/yazi-rs/plugins/tree/main/mount.yazi)
- 🎨 主题系统、鼠标支持、[拖放](https://yazi-rs.github.io/docs/dnd)、回收站、自定义布局、CSI u、OSC 52、CSI 2031
- ……还有更多！

https://github.com/sxyazi/yazi/assets/17523360/92ff23fa-0cd5-4f04-b387-894c12265cc7

## 项目状态

公开测试版，可作为日常主力使用。

Yazi 目前仍在快速开发中，可能会有破坏性变更，敬请留意。

## 文档

- 使用方法：https://yazi-rs.github.io/docs/installation
- 功能特性：https://yazi-rs.github.io/features

## 讨论

- Discord 服务器（主要使用英语）：https://discord.gg/qfADduSdJu
- Telegram 群组（主要使用中文）：https://t.me/yazi_rs

## 图片预览

| 平台                                                                     | 协议                               | 支持情况                           |
| ------------------------------------------------------------------------ | ---------------------------------- | ---------------------------------- |
| [kitty](https://github.com/kovidgoyal/kitty) (>= 0.28.0)                 | [Kitty unicode placeholders][kgp]  | ✅ 内置                            |
| [iTerm2](https://iterm2.com)                                             | [Inline images protocol][iip]      | ✅ 内置                            |
| [WezTerm](https://github.com/wez/wezterm)                                | [Inline images protocol][iip]      | ✅ 内置                            |
| [Konsole](https://invent.kde.org/utilities/konsole)                      | [Kitty old protocol][kgp-old]      | ✅ 内置                            |
| [foot](https://codeberg.org/dnkl/foot)                                   | [Sixel graphics format][sixel]     | ✅ 内置                            |
| [Ghostty](https://github.com/ghostty-org/ghostty)                        | [Kitty unicode placeholders][kgp]  | ✅ 内置                            |
| [Windows Terminal](https://github.com/microsoft/terminal) (>= v1.22.10352.0) | [Sixel graphics format][sixel] | ✅ 内置                            |
| [st with Sixel patch](https://github.com/bakkeby/st-flexipatch)          | [Sixel graphics format][sixel]     | ✅ 内置                            |
| [Warp](https://www.warp.dev) (仅 macOS/Linux)                            | [Inline images protocol][iip]      | ✅ 内置                            |
| [Tabby](https://github.com/Eugeny/tabby)                                 | [Inline images protocol][iip]      | ✅ 内置                            |
| [VSCode](https://github.com/microsoft/vscode)                            | [Inline images protocol][iip]      | ✅ 内置                            |
| [Rio](https://github.com/raphamorim/rio) (>= 0.3.9)                      | [Kitty unicode placeholders][kgp]  | ✅ 内置                            |
| [Black Box](https://gitlab.gnome.org/raggesilver/blackbox)               | [Sixel graphics format][sixel]     | ✅ 内置                            |
| [Bobcat](https://github.com/ismail-yilmaz/Bobcat)                        | [Sixel graphics format][sixel]     | ✅ 内置                            |
| X11 / Wayland                                                            | Window system protocol             | ☑️ 需要 [Überzug++][ueberzug]      |
| Fallback                                                                 | [ASCII art (Unicode block)][ascii-art] | ☑️ 需要 [Chafa][chafa] (>= 1.16.0) |

详见 https://yazi-rs.github.io/docs/image-preview。

<!-- Protocols -->

[kgp]: https://sw.kovidgoyal.net/kitty/graphics-protocol/#unicode-placeholders
[kgp-old]: https://github.com/sxyazi/yazi/blob/main/yazi-adapter/src/drivers/kgp_old.rs
[iip]: https://iterm2.com/documentation-images.html
[sixel]: https://www.vt100.net/docs/vt3xx-gp/chapter14.html
[ascii-art]: https://en.wikipedia.org/wiki/ASCII_art

<!-- Dependencies -->

[ueberzug]: https://github.com/jstkdng/ueberzugpp
[chafa]: https://hpjansson.org/chafa/

## 特别鸣谢

<img alt="RustRover logo" align="right" width="200" src="https://resources.jetbrains.com/storage/products/company/brand/logos/RustRover.svg">

感谢 RustRover 团队提供开源许可证，支持 Yazi 的维护工作。

活跃的代码贡献者可以联系 @sxyazi 获取许可证（如还有剩余名额）。

## 许可证

Yazi 采用 MIT 许可证。详情请查看原仓库的 [LICENSE](https://github.com/sxyazi/yazi/blob/main/LICENSE) 文件。
