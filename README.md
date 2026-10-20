# 咕咕 · gu812

软件工程专业在读。把 AI Agent 当工程问题做：给预算、给取证规则、给失败时的兜底。

不太写躺在仓库里的 demo，写本机每天真的会跑的东西。

## 在跑的项目

| 项目 | 它是什么 | 用的是 |
|---|---|---|
| [**ai-radar**](https://github.com/gu812/ai-radar) | 每天 08:30 自动产出的 AI 日报：多角度检索、去重、双维度可信度标签，压成一张飞书卡片推到群里 | `pi` headless · DeepSeek Search API · `launchd` · 飞书 Card 2.0 · Shell |
| [**gu812.github.io**](https://gu812.github.io) | 个人博客。Hexo + Butterfly，主题做了改造，自托管思源宋体，首页 three.js 动效只在需要时加载 | Hexo · GitHub Actions · 主题改造 · 前端性能 |
| [**pi-config**](https://github.com/gu812/pi-config) | 可还原的 AI 编码环境：扩展、子代理、白名单式安装器，改之前先备份，凭据永不进仓库 | Python · Node.js · 配置工程 |

## 我做这些东西时在意什么

**Agent 的产出要能被核验。** ai-radar 里没有一句话能凭空出现：每条断言必须带真实 URL，标【一手】的行必须真的被 `fetch.sh` 抓过，零检索不算成功。报告尾部会写实测调用量，模型自述和实际跑了多少次对不上，一眼就能看见。

**配置要能恢复，凭据要能守住。** pi-config 的安装器只覆盖白名单文件，旧文件先落进 `~/.pi/backups/<时间>/`，`auth.json` 和真实 `models.json` 永不参与同步。备份仓库私有，也一样不存密码。

**失败要算清楚，不要假装没事。** 飞书推送挂了不判任务失败 —— 日报是主产出，推送失败记 WARN 写进日志，第二天还能看见发生了什么。

## 工具

`Shell` · `Python` · `TypeScript` · `JavaScript` · `Node.js` · `Hexo` · `Docker` · `GitHub Actions` · `飞书开放平台` · `macOS launchd`

## 找我

博客 <https://gu812.github.io>
