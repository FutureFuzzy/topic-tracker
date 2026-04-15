# topic-tracker

> 自媒体爆款选题追踪 Skill - 支持多平台 AI 助手

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 📌 简介

一款基于**多维评分体系**的选题追踪工具，帮助自媒体创作者快速生成跨平台（小红书、B站、公众号、抖音）的爆款选题建议和标题优化方案。

**核心能力**：
- 🔥 联网获取热点数据
- 📊 多维评分筛选优质选题
- 📝 分平台差异化标题生成

---

## 🛠️ 支持的平台

### ✅ WorkBuddy（开箱即用）

**使用方法**：
1. 克隆本仓库
2. 复制 `skill-workbuddy/` 目录到 `~/.workbuddy/skills/`
3. 重命名为 `topic-tracker`
4. 在 WorkBuddy 中直接说「帮我找XX领域选题」即可

---

### ✅ Claude Code

**使用方法**：
1. 克隆本仓库
2. 复制 `skill-workbuddy/SKILL.md` 到 `~/.claude/skills/topic-tracker/SKILL.md`
3. 重启 Claude Code，说出需求即可触发

> 注：Claude Code 的 Skill 格式与 WorkBuddy 高度兼容，核心 Prompt 可直接复用。

---

### 🔄 Coze（扣子）平台

Coze 使用**工作流 + Bot** 架构，不能直接导入 SKILL.md。

**使用方法**：
1. 复制 `skill-coze/prompt.md` 中的系统提示词
2. 在 Coze 创建 Bot，将提示词粘贴到「角色设定」中
3. 配置联网搜索插件
4. 参考 `skill-coze/workflow.md` 设计工作流

---

### 🔄 其他 AI 助手

核心内容（评分体系、Prompt 模板）是**通用的**，你可以：

1. 参考 `prompt-templates.md` 提取核心逻辑
2. 根据目标平台的 Skill 格式进行调整
3. 移植 `SCORING.md` 中的评分维度和权重

---

## 📂 目录结构

```
topic-tracker/
├── README.md              # 本文件
├── LICENSE                # MIT 开源协议
│
├── skill-workbuddy/       # WorkBuddy 版本（主版本）
│   └── SKILL.md           # 完整 Skill 文件
│
├── skill-claude/          # Claude Code 版本
│   └── SKILL.md           # 适配 Claude Code 格式
│
├── skill-coze/            # Coze/扣子 版本
│   ├── prompt.md          # 系统提示词（直接复制使用）
│   └── workflow.md        # 工作流设计参考
│
├── docs/
│   ├── SCORING.md         # 评分体系详细文档
│   └── PLATFORM_RULES.md   # 各平台规则详解
│
└── assets/
    └── preview.md          # 效果预览
```

---

## 🎯 核心评分体系

```
爆款指数 = 热度分×30% + 平台适配分×25% + 竞争度分×20% + 情绪共鸣分×15% + 变现潜力分×10%
```

### 各维度权重

| 维度 | 权重 | 说明 |
|-----|------|------|
| 热度分 | 30% | 搜索/讨论量 |
| 平台适配分 | 25% | 与平台用户偏好契合度 |
| 竞争度分 | 20% | 内容饱和度（越低越好） |
| 情绪共鸣分 | 15% | 引发共情能力 |
| 变现潜力分 | 10% | 商业价值 |

---

## 📖 使用示例

### 输入
```
领域：AI工具
时间范围：近一周
```

### 输出
```
## 📌 领域：AI工具 | 时间范围：近一周

### 🔥 热点事件摘要
- GPT-6 发布倒计时
- 阿里千问登顶全球调用榜
- Google Gemma 4 开源

### 💡 选题池

#### 选题1：GPT-6要来了？普通人现在入局AI还来得及吗
- **爆款指数**：9.1/10
- **适合平台**：小红书、公众号、抖音

**📕 小红书标题**：
1. GPT-6快来了！现在学AI还来得及吗？🔥
2. 打工人必看｜AI浪潮下，普通人的生存指南

...（更多见 SKILL.md）
```

---

## 🤝 贡献

欢迎提交 Issue 和 PR！

如果你适配到了其他平台，欢迎提交 `skill-[平台名]/` 目录。

---

## 📄 License

MIT License - 详见 [LICENSE](LICENSE) 文件

---

> Made with ❤️ by [芝麻糊]
