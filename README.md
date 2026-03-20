# Google Family Bucket Skill

> Google 全家桶 Claude Prompt 完全手册

## 📋 概览

- **覆盖服务**: Gmail · Calendar · Drive · Docs · Sheets · Slides · Tasks · Forms · Chat · Contacts
- **适用场景**: 桌面端 · 移动端 · 跨工具集成
- **提示词总数**: 60+
- **最后更新**: 2026-03-20

## 📁 项目结构

```
google-skill/
├── SKILL.md                 # Skill 配置文件
├── README.md                # 项目说明
├── prompts/                 # 提示词库
│   ├── gmail/              # Gmail 邮件管理
│   ├── calendar/           # Google Calendar 日历
│   ├── drive/              # Google Drive 云存储
│   ├── docs/               # Google Docs 文档
│   ├── sheets/             # Google Sheets 表格
│   ├── slides/             # Google Slides 演示
│   ├── tasks/              # Google Tasks 任务
│   ├── forms/              # Google Forms 表单
│   ├── chat/               # Google Chat 消息
│   ├── contacts/           # Google Contacts 联系人
│   └── integration/        # 跨工具集成工作流
├── scripts/                 # 脚本工具
└── config/                  # 配置文件
```

## 🚀 快速开始

### 使用方法

1. 浏览 `prompts/` 目录找到对应服务的提示词
2. 复制需要的提示词模板
3. 替换 `[括号内]` 的参数为你的实际内容
4. 发送给 Claude 执行

### 示例

**查看今日邮件:**
```
帮我查看今天收到的所有邮件，按发件人和主题列成清单，标注【需回复 / 知晓即可 / 可忽略】。
```

**创建日历事件:**
```
帮我新建日历事件：
标题：项目评审会议
时间：2026-03-25 14:00–15:30
地点：会议室 A / Google Meet
参会人：team @example.com
提醒：提前 30 分钟
备注：准备 Q2 进度报告
```

## 💡 使用原则

| 原则 | 说明 |
|------|------|
| 执行前确认 | 涉及发送、创建、修改的操作需先确认 |
| 添加"请先让我确认" | 对于提交或发布类操作 |
| 明确指定范围 | 搜索类提示注明时间范围和关键词 |
| 复杂工作流分步执行 | 拆分为多个提示词 |
| 优先草稿模式 | 邮件/文档先生成草稿而非直接提交 |

## 📱 移动端技巧

- 使用短句提示减少输入
- 使用"用两行字告诉我"控制输出长度
- 语音输入 → Claude 润色 → 发送，减少打字

## 🔗 集成工作流

### 晨间智能简报
综合 Calendar、Tasks、Gmail 生成今日工作简报

### 完整会议流程
- 会前：Calendar + Gmail + Drive 背景调研
- 会后：Docs 纪要 + Tasks 行动项 + Calendar 后续会议

### 项目管理
- 周报生成：Calendar + Tasks + Sheets 数据汇总
- 任务拆解：自动创建 Tasks + Calendar 时间规划 + Docs 模板

### 邮件 × 日历
- 邮件中的会议邀请自动转为日程
- 明日日程提醒邮件草稿

### 个人生活
- 周末规划
- 旅行准备清单
- 每日收尾检查

## ⚙️ 服务连接状态

| 服务 | 状态 |
|------|------|
| Gmail | ✅ 已连接 |
| Google Calendar | ✅ 已连接 |
| Google Drive | ⬜ 需在设置中启用 |
| Google Tasks | ⬜ 需要 MCP 配置扩展 |
| Google Docs | ⬜ 需要 MCP 配置扩展 |
| Google Sheets | ⬜ 需要 MCP 配置扩展 |
| Google Slides | ⬜ 需要 MCP 配置扩展 |

## 📄 许可证

CC BY-NC-SA 4.0

## 🙏 致谢

- 原作者：某方
- 生成模型：Claude Sonnet 4.6
- 整理日期：2026-03-20
