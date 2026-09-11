# Discord Community Toolkit Bot

这是一个基于 Python 和 discord.py 的 Discord 社区工具箱 Bot，面向社区运营、活动挑战、论坛监控、反馈收集、待办提醒和跨 Bot 管理联动场景。项目适合展示复杂 Slash Command 组织、交互式组件、SQLite 持久化、后台任务和社区自动化能力。

> 本仓库为脱敏公开版本，不包含任何真实服务器数据、Bot Token、数据库文件或日志。

## 功能概览

- 挑战/徽章系统：支持挑战面板、题库 JSON 导入、通关进度、冷却惩罚、徽章墙和毕业奖励。
- 面板管理：支持挑战入口、排行榜、徽章墙、毕业奖励等持久化交互面板。
- 社区管理：支持黑名单、挑战封禁、进度重置、权限授权和维护命令。
- 论坛监控：监听论坛新帖，自动回复、转发提醒、补发漏处理通知。
- 成员监控：统计新成员加入数量，达到阈值后通知管理频道。
- 反馈系统：支持匿名/实名反馈、白名单、频率限制和投递频道。
- 事件列表：支持个人/频道待办、排序、倒计时提醒和关键词触发展示。
- 跨 Bot 联动：支持处罚、黑名单等处理记录的同步和审计。

## 技术栈

- Python 3.10+
- discord.py 2.x
- SQLite / aiosqlite
- aiohttp / aiofiles
- pytz / psutil
- Discord View / Button / Select / Modal

## 目录结构

```text
.
├── cogs/           # 功能模块与 Slash Command
├── core/           # 数据库、模型、常量、缓存
├── utils/          # 权限、日志、备份、格式化工具
├── views/          # Discord UI 交互组件
├── bot.py          # 启动入口与 Cog 加载
├── config.example.json
└── requirements.txt
```

## 本地运行

1. 安装依赖：

```powershell
pip install -r requirements.txt
```

2. 复制配置模板：

```powershell
Copy-Item config.example.json config.json
```

3. 在 `config.json` 中填写自己的 Discord Bot Token 和开发者 ID。

4. 启动：

```powershell
python bot.py
```

## 配置说明

- `BOT_TOKEN`：Discord Bot Token，必填。
- `DEVELOPER_IDS`：开发者 Discord 用户 ID 列表，用于限制维护命令。
- `PREFIX`：文本命令前缀，默认 `!`。
- `PROXY`：可选代理配置。
- `AUTO_BLACKLIST_MONITOR`：跨 Bot 监听配置，公开模板中不包含真实 ID。
- `FEEDBACK`：反馈入口、频率限制和白名单设置。

## 隐私处理

- 不提交 `config.json`、数据库、日志、缓存、备份和真实导出文件。
- 不提交真实服务器名、用户 ID、频道 ID、身份组 ID、邀请链接或截图。

