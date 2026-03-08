# sts2_typing

适用于 [Slay the Spire 2](https://store.steampowered.com/app/646570/Slay_the_Spire_2/) 的多人联机**游戏内聊天 Mod**。  
实时发送消息、分享 Emoji 表情，并将卡牌、遗物、药水、能力直接以可交互链接的形式分享到聊天框。

---

## 功能特性

- **聊天面板覆盖层** — 简洁的聊天面板悬浮于屏幕角落，不操作时自动淡出，不影响游戏体验。
- **物品链接分享** — `Alt + 左键单击` 任意卡牌、遗物、药水或能力，即可在聊天中生成可点击的物品链接，悬停时展示完整提示框预览。
- **Emoji 面板** — 内置 18 个 Emoji 图标（由 [Lucide](https://lucide.dev) 提供），点击输入框中的按钮即可弹出选择器。
- **多人网络同步** — 消息通过游戏内置的可靠网络传输广播给所有已连接的玩家。
- **键盘优先操作** — 按 `Enter` 打开聊天，再按 `Enter` 发送，`Esc` 关闭。

---

## 操作方式

| 操作 | 快捷键 |
|---|---|
| 打开聊天框 | `Enter` |
| 发送消息 | `Enter` |
| 关闭聊天框 / 关闭 Emoji 选择器 | `Esc` |
| 分享当前悬停的物品 | `Alt + 左键单击` |
| 打开 Emoji 选择器 | 点击输入框内的 Emoji 按钮 |

---

## 安装方法

1. 从 [最新 Release](https://github.com/Shiroim/sts2_typing/releases/latest) 下载 `typing.zip`。
2. 将压缩包内容解压到 Slay the Spire 2 的 Mods 文件夹：
   ```
   <Steam库路径>/steamapps/common/Slay the Spire 2/Mods/
   ```
3. 启动游戏，在 Mod 菜单中启用本 Mod 即可。

---

## 从源码构建

**环境要求**

- [.NET SDK](https://dotnet.microsoft.com/download)（版本需与游戏目录中 `global.json` 一致）
- 支持 .NET 的 [Godot 4](https://godotengine.org/)
- 一份 Slay the Spire 2 游戏本体（编译时需要引用游戏程序集）

**构建步骤**

1. 将本仓库克隆到你的 STS2 Mod 工作目录。
2. 按需修改 `typing.csproj` 中的游戏路径引用。
3. 执行构建：
   ```bash
   dotnet build
   ```
4. 通过 Godot 导出，或将编译产物 `.pck` / `.dll` 手动复制到 Mods 文件夹。

---

## 物品链接格式

物品链接以 `{{type:id}}` 格式编码在消息文本中，渲染为带样式的可交互文字：

| Token | 示例 |
|---|---|
| 卡牌 | `{{card:MegaCrit.Sts2.Cards.Strike:0}}` |
| 药水 | `{{potion:MegaCrit.Sts2.Potions.FirePotion}}` |
| 遗物 | `{{relic:MegaCrit.Sts2.Relics.BurningBlood}}` |
| 能力 | 通过 Alt+单击 自动插入 |
| 目标生物 | 通过 Alt+单击 自动插入 |

---

## 开源协议

本项目基于 [MIT License](LICENSE) 开源。

图标来自 [Lucide](https://lucide.dev)，使用 ISC License 授权。  
Lucide 部分版权归 Cole Bemis 2013-2026 所有（源自 Feather，MIT 协议）。

---

*本 Mod 与 MegaCrit 官方无关，亦未获得官方背书。*
