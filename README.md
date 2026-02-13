# alskai-dayflow

**WorkState Manager** - 让每一天都留下可复用的认知资产

![Version](https://img.shields.io/badge/version-1.0.1-green.svg)](https://github.com/Albert-Lsk/alskai-dayflow)
![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-purple.svg)](https://claude.com/claude-code)

---

## 🎯 核心价值

帮助多任务并行的知识工作者：
- 清晰启动每一天的工作
- 流畅切换不同任务
- 整理归档每日收获
- 持续跟踪未闭环事项
- **单一文档原则**：每天只生成一个WorkDay.md文件

**品牌标识**: ALSKai - 让我们一起用AI做点有趣的事🌿

---

## ✨ 特性

- 🌅 **工作日启动器** - 自动继承昨日Open Loops，智能检测沉寂任务
- 🌙 **工作日归档器** - 更新checkbox状态，汇总所有切换记录
- 🔄 **任务切换助手** - 存档当前进度，加载新任务上下文
- 📝 **单一文档原则** - 每天一个WorkDay.md，避免分散
- 📅 **Open Lops管理** - 沉寂≥7天自动警告，智能归档

---

## 🚀 快速开始

### 安装

将 `alskai-dayflow` 文件夹复制到你的 `.claude/skills/` 目录下：

```
.claude/
└── skills/
    └── alskai-dayflow/    ← 放这里
        ├── README.md
        ├── skill.md
        └── references/
            ├── document-template.md
            └── examples.md
```

重启 Claude Code，skill会自动加载。

---

## 💻 使用方法

### 三个命令，统一命名 `turn-me-*`

#### 1. `/turn-me-on` - 工作日启动器（早上使用）
- 获取当前真实日期（使用web_search）
- 创建DailyReview文件夹结构
- 检查是否已存在今天的文档
- 读取昨天的Open Loops（如果存在）
- 收集今日三大目标
- 生成今日WorkDay.md

#### 2. `/turn-me-off` - 工作日归档器（晚上使用）
- 获取当前真实日期
- 读取今天的WorkDay.md
- 收集每个任务的完成情况
- 更新所有checkbox状态
- 收集今日核心收获、新想法、未闭环事项
- 追加晚间归档内容
- 更新顶部状态标记为"已归档"

#### 3. `/turn-me-to` - 任务切换助手（工作中使用）
- 识别切换意图（从任务A→任务B）
- 存档当前任务进度（前进度、完成度、卡点）
- 生成新任务上下文（背景、材料、关键点）
- 将切换记录存储到WorkDay.md的任务切换暂存区

---

## 📂 文件组织

### 目录结构

```
DailyReview/
├── 2026-02-11/          ← 一天只有这一个文件
│   └── 2026-02-11-WorkDay.md  ← 所有信息全在里面
├── 2026-02-12/
└── ...
```

### WorkDay.md 文档结构

```
# 🌅 YYYY-MM-DD 工作日志

> 生成时间: HH:MM | 状态: 进行中

---

## 🎯 今日三大目标
- [ ] 目标1
- [ ] 目标2
- [ ] 目标3

---

## 🔄 从昨天继承的Open Loops

<!-- 从昨天继承，以下格式保持 -->
- [ ] **任务名称**
  - 上次出现: YYYY-MM-DD
  - 最后更新: YYYY-MM-DD
  - 今日计划: XXX

---

## 📝 今日待办事项

- [ ] 任务1
- [ ] 任务2
- [ ] 任务3

---

## 🌙 晚间归档

### 📈 今日核心收获
- 收获1
- 收获2
- 收获3

### 💡 新想法/新发现
- 想法1
- 想法2

### 🔗 未闭环事项（传递给明天）
- 未完成任务1
- 未完成任务2

---

## 🔄 今日任务切换暂存区

<!-- 由 /turn-me-to 自动追加，请勿手动编辑 -->

---

## 🧘 今日状态评分
⭐⭐⭐⭐ (4/5)

评价：XXX

---

### 📁 文档信息
本文档: `DailyReview/{DATE}/{DATE}-WorkDay.md`
归档时间: HH:MM
```

---

## ⚙️ 注意事项

1. **日期获取**: 必须使用web_search获取真实日期，不要依赖AI的内部时间
2. **路径处理**: 使用相对路径，确保在用户的工作目录下创建文件
3. **编码处理**: 所有文件使用UTF-8编码
4. **对话流程**: 保持简洁友好，避免繁琐的提问

---

## 🎨 开发路线图

- [x] v0.1.0 (MVP阶段)
  - [x] 三个基础命令
  - [x] 单一文档原则
  - [x] Open Lops管理
- [ ] v0.2.0 (优化阶段)
  - [ ] 沉寂提醒增强
  - [ ] 精力状态可视化
  - [ ] 周统计功能

---

## 📚 相关文档

- **模板文件**: `references/document-template.md`
- **使用示例**: `references/examples.md`

---

**ALSKai - 让我们一起用AI做点有趣的事🌿**

**版本**: 1.0.3 | **最后更新**: 2026-02-13
