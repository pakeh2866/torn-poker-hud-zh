# Torn Poker HUD 玩家画像与教练 · 中文汉化版

[Torn Poker HUD - Player Profiler & Coach](https://greasyfork.org/scripts/569933) 的简体中文汉化版。

德扑对手自动分析与实战提示：VPIP、PFR、AFq、WTSD 等指标，每个座位挂徽章，附针对性剥削建议与自我改进路径。

> 本仓库**只做文案翻译**：未修改任何功能逻辑、未增删任何功能、未收集任何数据。

---

## 安装

1. 先安装 [Tampermonkey](https://www.tampermonkey.net/)（油猴脚本管理器）
2. 点下面任一链接安装（Tampermonkey 会自动弹出安装框）：

   - **国内推荐** · jsDelivr 镜像（CDN 加速，下载快） → [`torn-poker-hud-zh.user.js`](https://cdn.jsdelivr.net/gh/pakeh2866/torn-poker-hud-zh@main/torn-poker-hud-zh.user.js)
   - **直连 GitHub** → [`torn-poker-hud-zh.user.js`](https://raw.githubusercontent.com/pakeh2866/torn-poker-hud-zh/main/torn-poker-hud-zh.user.js)

3. 安装后打开 Torn 的 Hold'em 页面即生效。脚本内置 `@updateURL`，以后有新版本 Tampermonkey 会自动提示更新。

---

## ⚠️ 使用前必读

**不要与原版同时启用。** 两个脚本共用同一套存储（`tornPokerHUD_v1`、备注库、IndexedDB），同时开启会互相覆盖统计，行为不可预期。

**但切换过来不会丢数据。** 汉化版刻意沿用了原版的全部存储键，所以从原版换到汉化版，你已有的手牌记录、对手备注、自定义设置会**直接继承**，不用从头积累。卸载原版 → 装汉化版即可。

**上游更新后本版可能滞后。** 本次汉化基于 v6.12（2026-09-10）。原脚本迭代较频繁，新版原版发布后我会跟进，但中间会有一段时间的窗口。

---

## 术语约定

汉化不是逐词替换，核心指标缩写一律保留英文，街名和牌理术语按中文德扑圈的习惯用词：

| 原文 | 译法 |
| --- | --- |
| preflop / flop / turn / river | 翻前 / 翻牌 / 转牌 / 河牌 |
| showdown | 摊牌 |
| leak | 漏洞 |
| open (raise) | 开池 |
| marginal hand | 边缘牌 |
| wet board | 湿润牌面 |
| tight-aggressive / loose-aggressive | 紧凶型 / 松凶型 |
| calling station | 跟注站 |
| VPIP / PFR / AFq / C-bet / 3-bet / WWSF | 原样保留 |

---

## 汉化进度与对照报告

**在线查看** → <https://pakeh2866.github.io/torn-poker-hud-zh/i18n-report.html>

仓库里也保留了源文件 [`i18n-report.html`](i18n-report.html)，逐行列出每一处「英文原文 → 中文译文」：

- 已汉化对照 **2573** 处（长句 1460 / 短标签/术语 1111）
- 涉及 136 个代码区块
- 仍待汉化 1015 处

报告是单文件 HTML（数据内嵌、无外部依赖），**下载后双击用浏览器打开**即可，不需要服务器。左侧按代码区块导航，支持按行号/关键字搜索、按类型筛选、导出 TSV。

> 报告中的行号有两套：黑色的 `L12345` 是英文原版行号，灰色的 `→12347` 是汉化版行号（汉化版在脚本元数据区多了 2 行）。

---

## 已知差异

- 脚本元数据区（`// ==UserScript==` 块）与原版不同：改了 `@name`、`@namespace`，新增了中文描述与 `@translator`，补上了指向本仓库的 `@updateURL` / `@downloadURL`。这些是发布所必需，不影响运行。
- 原文里的英文缩写、代码标识符、枚举值一律未动，避免影响脚本内部判断。

---

## 许可与署名

- 原脚本：**Torn Poker HUD - Player Profiler & Coach** © [HopesG](https://greasyfork.org/scripts/569933)，以 MIT 许可发布
- 汉化：[pakeh2866](https://github.com/pakeh2866)
- 本项目同样以 [MIT](LICENSE) 许可发布，原始版权声明已保留在脚本头部

本项目与 Torn 官方及原脚本作者均无隶属关系。

---

## English

Chinese (Simplified) translation of [Torn Poker HUD - Player Profiler & Coach](https://greasyfork.org/scripts/569933) by HopesG (MIT).

**Translation only** — no features added or removed, no data collected, no logic modified. Install Tampermonkey, then open [`torn-poker-hud-zh.user.js`](https://raw.githubusercontent.com/pakeh2866/torn-poker-hud-zh/main/torn-poker-hud-zh.user.js).

Do **not** run this alongside the original script — they share the same storage keys and will overwrite each other's stats. Switching from the original to this version keeps all existing hand history and notes.
