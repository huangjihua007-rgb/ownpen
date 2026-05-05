# OwnPen — 亲笔写的 项目记忆

## 基本信息

- **英文名**: OwnPen
- **中文名**: AI去痕迹改写
- **Slug**: `ownpen`
- **当前源码版本**: `SKILL.md` = v1.4.0
- **Tagline EN**: "Make it sound like YOU wrote it."
- **Tagline CN**: "让领导看不出是AI写的"
- **Author**: huangjihua007-rgb
- **Category**: productivity
- **Tags**: writing, chinese, humanizer, ai-detection, rewriting, ownpen

---

## 产品定位

中文去AI化 + 平台风格化写作工具。不是翻译英文 humanizer，而是中文原生规则改写。

**核心卖点**：改完原文格式一字不动，只换掉机器味。

**当前交互结构**：
1. **模式1（改写）**：选场景 → 粘文字 → 直接出改写结果
2. **模式2（诊断）**：粘文字 → 完整诊断报告（致命 / 明显 / 轻微三级）

---

## 核心原则（改写三不改）

1. **改套路感，不改正式感。** 职场文档可以正式，但不能 AI 味。
2. **改写不改立场，不改语气。** 只消除模板化表达，不改变原作者态度。
3. **口语化仅用于打破套路感，不是改写目标。** 只做节奏优化，不翻译成大白话。

---

## 场景与规则

- **检测规则**：45 条中文 AI 痕迹规则（致命 / 明显 / 轻微）
- **改写场景**：10 个（通用、公众号、知乎、小红书、朋友圈、工作汇报、商务邮件、短视频脚本、产品/活动文案、简历/自我介绍）
- **产品精髓**：结果页正文必须干净，不在改写内容里加框线、标签、标注

---

## WorkBuddy UI 预览

- **预览文件**: `D:\AI去痕迹改写\previews\workbuddy-ui-preview.html`
- **用途**:
  1. 在 WorkBuddy 中预览完整聊天式 UI（开场卡、场景选择、等待粘贴、改写结果、诊断结果、全流程串看）
  2. 作为截图素材源，用于小红书、朋友圈、知乎等推广内容
  3. 后续做 UI 迭代时，先对照这个静态预览核对层级、按钮和结果卡观感
- **维护规则**:
  - 交互结构有明显改动后，必须同步更新该 HTML 预览
  - 更新后同时同步 skill-factory 的 `projects/ownpen.md`
  - `previews/` 目录不进入发布包

---

## 文件结构

```text
D:\AI去痕迹改写\
├── SKILL.md
├── README.md
├── rules/
├── examples/
├── previews/
│   └── workbuddy-ui-preview.html   ← WorkBuddy UI 静态预览
├── _publish_/
├── _publish_clawhub/
└── .claude/
    └── CLAUDE.md
```

---

## 发布与素材备注

- GitHub: https://github.com/huangjihua007-rgb/ownpen
- ClawHub: https://clawhub.ai/skills/ownpen
- 营销主素材优先级：
  1. 改前 vs 改后对比截图
  2. WorkBuddy UI 结果页截图
  3. 诊断页问题分级截图

---

## 注意事项

- description 保持口语化，避免 moderation 标记 suspicious
- 预览文件用于演示和截图，不用于发布
- 如果改写模式、场景菜单或结果卡结构变动，优先更新预览文件再更新营销素材
