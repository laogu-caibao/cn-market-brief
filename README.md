# 每日市场早报

`laogu-morning`

每日市场简报 skill：在交易日开盘前生成中文早报。

## 一键安装

```bash
npx skills add laogu-caibao/laogu-morning
```

仓库地址（点击复制）：

`https://github.com/laogu-caibao/laogu-morning`

**方式一：克隆**

```bash
git clone https://github.com/laogu-caibao/laogu-morning.git
```

**方式二：下载 ZIP**

https://github.com/laogu-caibao/laogu-morning/archive/refs/heads/main.zip

**导入使用**

- Claude Code / Muse：把仓库中的 `SKILL.md` 放到 `~/.claude/skills/laogu-morning/` 下即可调用。
- 豆包智能体 / Workbuddy 等：按各平台的 skill 上传流程导入 `SKILL.md`。
- 扣子 Coze：扣子编程 → 技能面板 → 创建技能 → 本地上传，上传本仓库打包的 zip（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；如页面要求 `.skill` 后缀，由扣子导入后自动生成，不要只改扩展名。
- Trae：设置 → 技能 → 上传技能，上传同上 zip；或手动放到 `~/.trae/skills/laogu-morning/`（项目级用 `.trae/skills/laogu-morning/`）。Trae 也支持 MCP：把 `uvx laogu-mcp` 配进 MCP 设置即可获得 16 个工具（skill 负责流程指导、MCP 负责工具调用）。
- 一次装好全部 16 个：用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)，`uvx laogu-mcp` 一键安装。
## 文件结构

- `SKILL.md` — 主流程（平台中立，定时能力由宿主平台提供）
- `references/sources.md` — 数据源：行情接口、外盘指数代码、公告与日历来源

## 输出结构

- 隔夜外盘：美股三大指数、中概、美元指数、离岸人民币、原油/黄金/铜
- 昨日A股：指数涨跌、成交额、领涨/领跌板块
- 今日看点：新股申购、限售解禁、分红除权除息、重要公告、宏观数据/事件
- 一句话前瞻：市场关注焦点（不做涨跌预测）

## 定时建议

- A股交易日 8:30 前推送
- 可与 `laogu-announcements` 联动，自动带入关注公司的最新公告

---
## English

**laogu-morning — Daily A-share morning brief.** Every trading morning, get a Chinese-language briefing: overnight US and global market moves, a recap of yesterday's A-share session, and today's watch points. One command install: `npx skills add laogu-caibao/laogu-morning`.

## FAQ

**Q：laogu-morning 有什么用？**
适合的场景：每个交易日早上要一份「隔夜发生了什么 + 今天看什么」的中文简报，不想自己翻外盘行情。

**Q：数据可靠吗？会荐股吗？**
数字必须来自可核验的公开来源（上市公司公告、交易所公开数据、公开网页），取不到就标「未核验」，绝不编造；只做结构化整理与解读，不构成投资建议。

**Q：怎么安装？支持哪些 AI 平台？**
```bash
npx skills add laogu-caibao/laogu-morning
```
平台中立 Markdown，Claude Code、Codex、豆包智能体、Workbuddy、扣子 Coze、Trae 等环境均可用；数据能力可用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)（`uvx laogu-mcp`）一次装齐。更多 skill 见[老谷拆财报组织主页](https://github.com/laogu-caibao)。
---

## 出品

**老谷拆财报** —— 以数据为刃，剖市场真相

- 抖音 / 微信视频号 / 今日头条 / 快手：搜索「老谷拆财报」
- 固定栏目：「价值投资之财报解读」（全网连载中）
- 本 skill 的方法论与账号内容同源：数据驱动、拆开看、不讲黑话

### 扫码关注

| 微信视频号 | 抖音 |
|---|---|
| ![视频号二维码](docs/qrcode-shipinhao.jpg) | ![抖音二维码](docs/qrcode-douyin.png) |
| 扫一扫，关注视频号 | 抖音号：gubaobao22 |

> 作者声明：个人观点，仅供参考，不构成投资建议。

