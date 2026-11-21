# WorkFlowBench

<p align="center">
  <img src="assets/flownote-logo.svg" width="110" alt="WorkFlowBench logo">
</p>

<p align="center">
  <b>我的个人 AI 工作台</b> · 运行在 Obsidian 里 · 桌面端与移动端通用
</p>

> **一句话定位**：打开就是我的首页，随手捕获、每日计划、项目推进、知识资产统计、AI 对话与技能工作流，都在同一个空间里完成。把"把一条想法向前推一步"的摩擦做到最小。
>
> 🧩 本项目由我（Max）基于 [FLOWnote](https://github.com/1095327780/FLOWnote)（MIT，原作者 阿浩learn / AHao）深度定制而来。核心引擎与内置技能归原作者所有，此处为我的个人品牌与工作台定制版本。

---

## 目录

- [为什么做这个工作台](#为什么做这个工作台)
- [它解决什么问题](#它解决什么问题)
- [核心能力](#核心能力)
- [内置技能清单](#内置技能清单)
- [安装与启用](#安装与启用)
- [配置我的 AI 服务](#配置我的-ai-服务)
- [日常工作流](#日常工作流)
- [界面预览](#界面预览)
- [在线预览](#在线预览)
- [技术说明](#技术说明)
- [定制与构建](#定制与构建)
- [致谢与许可](#致谢与许可)

---

## 为什么做这个工作台

大多数笔记系统都在同一个地方崩掉：想法积压的速度永远快过处理它的速度，几周后超过 70% 的笔记再也没被打开。

WorkFlowBench 押的是一件很朴素的事 —— **只要把"把一条想法向前推一步"这件事的摩擦做到足够小，我就会日复一日地做下去。**

它是我在原 FLOWnote 基础上，按自己的使用习惯和工作流改造出来的个人工作台：换了品牌、理顺了文案、打通了构建，让它真正成为"我的"工具，而不是一个通用插件。

---

## 它解决什么问题

FLOW 笔记法的四步闭环，WorkFlowBench 用内置技能把每一步的机械动作自动化：

```
捕获  →  加工  →  连接  →  输出
 F        L        O        W
 ↓        ↓        ↓        ↓
日记     永久     领域     项目
想法     笔记     页面     产出
```

- **F · 捕获（Feed）** —— 白天一键扔进今日日记，不挑文件夹、不纠结标签。
- **L · 加工（Lift）** —— 把碎想法淬炼成永久笔记：原子化、断言式标题、AI 协助找关联。
- **O · 连接（Organize）** —— "领域页"就是我的工作桌，做哪件事就摊开哪张桌子。
- **W · 输出（Work）** —— 项目自动落地为结构化目录，配合每日/每周/每月/每年复盘把闭环跑起来。

---

## 核心能力

### 🏠 首页工作台

- 今日状态、今日日记创建状态、今日聚焦
- 今日待办读取与原文复选框同步（勾选后直接改 Markdown）
- 快捷动作：规划今天、快速捕获、每日回顾、新建项目、打开主页文档
- 项目进展、知识资产统计、年度记录热力图
- 桌面端、小窗口、移动端响应式布局

### 🤖 AI 工作区

- 会话侧栏与历史持久化，流式回复、重试、取消
- 内置直连 API 模式：读写、搜索、每日笔记、任务、标签、反链、属性、文件移动、目录创建
- 可选 OpenCode 桥接模式（给习惯旧工作流的用户保留）
- 连接诊断：服务商、可执行文件路径、启动方式、失败定位

### ⚡ 移动端快速捕获

- 一键捕获到每日笔记；iOS 快捷指令把文本直接送入工作台
- 可选 AI 文本清理（口语转记录）、链接解析与降级保留原文
- 已处理 iOS 键盘遮挡兜底

### 🔒 本地优先 · 隐私可控

- 数据留在我自己的笔记库；可选直连或桥接，不依赖任何托管服务
- 第三方 API Key 由我自己配置，按服务商计费

---

## 内置技能清单

插件内置的 `bundled-skills/` 会在启动时自动同步到笔记库技能目录（默认 `.opencode/skills`）：

| 技能 | 作用 |
|---|---|
| `ah` | 统一入口：菜单 + 意图路由 |
| `ah-note` | 创建今日日记并初始化计划 |
| `ah-capture` | 低摩擦记录想法到每日笔记 |
| `ah-inbox` | 批量整理想法并分流（卡片/任务/已处理） |
| `ah-read` | 阅读划线整理与文献笔记处理 |
| `ah-card` | 洞见转永久笔记并推荐知识链接 |
| `ah-think` | 思维模型工具箱（费曼、第一性原理、逆向等） |
| `ah-review` | 每日回顾与反思流程 |
| `ah-week` | 周回顾（统计 + 残留想法处理） |
| `ah-month` | 月回顾与策略复盘 |
| `ah-year` | 年回顾与年度策略 |
| `ah-project` | 项目结构自动创建 |
| `ah-archive` | 项目归档与经验提炼 |
| `ah-index` | 知识库 AI 索引维护 |
| `ah-memory` | 跨技能记忆与进度状态规范 |
| `ah-init` | 初始化/修复库结构与模板 |
| `ah-legacy` | 旧版笔记与结构迁移 |
| `defuddle` / `json-canvas` / `obsidian-bases` / `obsidian-cli` / `obsidian-markdown` | Obsidian 相关辅助技能 |

> 内置技能由插件自动维护，不可在设置里编辑/删除；你自己的自定义技能可自由新增、导入与编辑。

---

## 安装与启用

### 方式一：直接安装我打包好的 release（推荐）

```text
<你的笔记库>/.obsidian/plugins/flownote/
  ├─ main.js          ← release/main.js
  ├─ manifest.json    ← release/manifest.json
  └─ styles.css       ← release/styles.css
```

然后：Obsidian → 设置 → 社区插件 → 启用 **WorkFlowBench**。

### 方式二：从源码安装（BRAT / 开发模式）

```bash
git clone https://github.com/MaxEGG88/FLOWnote.git
cd FLOWnote
npm install
npm run build          # 产出 release/ 目录
```

把 `release/` 下三个文件放到插件目录即可。

### 使用前提

- Obsidian v1.5.0+
- 使用内置 AI 工作流时，配置一个支持的服务商 API Key（或自定义 OpenAI 兼容接口）

---

## 配置我的 AI 服务

1. 打开 Obsidian → 设置 → 社区插件 → WorkFlowBench 设置。
2. 选择运行方式：
   - **内置直连 API（默认）**：填入服务商 API Key / 自定义 OpenAI 兼容接口即可，无需外部运行时。
   - **OpenCode 桥接（可选）**：保留给习惯旧工作流的场景，需本机安装 OpenCode。
3. 选择模型，保存即可。

> 模型、密钥等配置保存在 Obsidian 插件数据中，不会写进笔记库正文。

---

## 日常工作流

| 场景 | 怎么做 |
|---|---|
| 早上开工 | 打开首页 → 看今日聚焦与待办 → 点「规划今天」让 AI 给行动清单 |
| 随手记想法 | 手机快捷指令 / 桌面快速捕获 → 先进今日日记 |
| 整理笔记 | 用 `ah-inbox` 分流 → `ah-card` 把洞见做成永久笔记 |
| 推进项目 | 首页项目卡看进度 → `ah-project` 建结构 → 定期 `ah-review` |
| _periodic 复盘 | `ah-week` / `ah-month` / `ah-year` 三层复盘，闭环跑起来 |

---

## 界面预览

| 界面 | 截图 |
|---|---|
| 首页工作台 | ![首页工作台](assets/screenshots/home-dashboard.png) |
| AI 聊天工作区 | ![聊天工作区](assets/screenshots/chat-workspace.png) |
| iOS 快捷指令配置 | ![iOS 快捷指令](assets/screenshots/ios-shortcut-setup.png) |

---

## 在线预览

本机局域网静态站提供了产品介绍页 + 可交互原型（模拟界面，非真实插件）：

- **展示页 + 原型入口**：`http://192.168.1.200:8090/20261121-workflowbench/`
- **直接打开交互原型**：`http://192.168.1.200:8090/20261121-workflowbench/demo.html`

> 说明：预览站仅用于展示界面与交互概念，真实功能需在 Obsidian 中安装插件并使用你自己的 AI 配置。

---

## 技术说明

| 项 | 值 |
|---|---|
| 插件 ID | `flownote`（保留原 ID 以确保升级路径兼容） |
| 显示名称 | WorkFlowBench |
| 当前版本 | 0.6.1 |
| 最低 Obsidian | 1.5.0 |
| 运行平台 | 桌面端 + 移动端（isDesktopOnly: false） |
| 主要技术 | JavaScript / CommonJS，esbuild 打包，内置 `@opencode-ai/sdk` |
| 内置技能 | 22 项（16 个 ah-* + 6 个 Obsidian 辅助） |
| 默认技能目录 | `.opencode/skills` |
| 许可 | MIT（继承原项目） |

---

## 定制与构建

本项目已针对个人使用做过如下定制：

- 品牌显示名、logo 描述、首页 eyebrow、header 标题、多语言 UI 文案统一为 **WorkFlowBench**
- 保留原作者署名、MIT 许可与出处致谢（合规要求）
- 修复原项目 57 个中文模板文件的 `#Uxxxx` 编码文件名，构建守卫通过
- 对外可见的 UI 文案已品牌化；AI 内部 system prompt 与技能内容保留原样（避免改变 AI 行为）

重新构建：

```bash
npm install
npm run build      # check → sdk-vendor → build-release
npm run release:check   # 完整发布前检查（可选）
```

构建产物在 `release/`，含 `main.js`、`manifest.json`、`styles.css`。

---

## 致谢与许可

- 本项目基于 **[FLOWnote](https://github.com/1095327780/FLOWnote)** 定制，原作者 **阿浩learn / AHao**，采用 **MIT License**。
- 核心引擎、内置技能与原始设计归原作者所有；本仓库的定制部分（品牌、文案、构建修复）同样遵循 MIT。
- 感谢原项目致谢的 [OpenCode](https://github.com/anomalyco/opencode) 与 [Claudian](https://github.com/YishenTu/claudian)。

---

<p align="center">WorkFlowBench · 我的个人 AI 工作台 · Made by Max</p>
