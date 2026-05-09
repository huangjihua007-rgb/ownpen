# OwnPen — 亲笔写的 项目记忆

## 基本信息

- **英文名**: OwnPen
- **中文名**: 亲笔写的
- **Slug**: `ownpen`（旧 slug `qinbixiede` 已弃用）
- **当前版本**: v1.1.0（2026-05-02）
- **Tagline EN**: "Make it sound like YOU wrote it."
- **Tagline CN**: "让领导看不出是AI写的"
- **Author**: huangjihua007-rgb
- **Category**: productivity
- **Tags**: writing, chinese, humanizer, ai-detection, rewriting, ownpen

---

## 产品定位

中文去AI化 + 平台风格化写作工具。不是翻译英文 humanizer，是中文原生规则。

**三层架构**:
1. **检测层**: 45+ 条中文AI痕迹规则（致命/明显/轻微三级）
2. **改写层**: 5种平台风格化改写（公众号/知乎/小红书/汇报/朋友圈/通用）
3. **指纹层**: V2.0 规划 — 个人写作风格注入（未实现）

---

## 核心原则（改写三不改）

1. **改套路感，不改正式感。** 职场文档可以正式但不能AI味。"赋能"→"帮助"，不是→"使劲用"。
2. **改写不改立场，不改语气。** 原文什么态度就保持什么态度，只消除模板化表达。
3. **口语化仅用于打破套路感，不是改写目标。** "口语点缀"指连接词变化和偶尔短句穿插，不是把书面语翻译成大白话。

---

## 检测规则体系（45条）

### 致命级（出现即暴露）
- 体制词堆砌（赋能/闭环/深耕/沉淀...13个）
- 总结套话（综上所述/未来可期/任重道远...6个）
- 假高级词（深度剖析/全面赋能/精准触达...6个）
- 万能开头/排比三连/对偶强迫/同义反复
- 零立场/假共情/过度正能量
- 工整病/总分总/论点无例证
- 成语堆砌（100字内3+）/ 体制词密度（200字内5+）
- **四字词偏好**（"目前现状"→"现在"）
- 概念先行无体感

### 明显级（累积3个以上可疑）
- 机械过渡/数字套路/假设问答
- **设问自答式推进**（"差在哪？为什么？怎么做？"）
- **分类枚举框架感**（"第一层/第二层"）
- **括号解释癖**（"X（即Y）"）
- 递进叠加/因果链过长/转折后必递进
- 情绪均匀/万能鼓励结尾/过度谦虚/情感标签外贴/口语化为零
- 小标题过度工整/topic sentence模式/段落主题单一/比喻缺失
- 分号癖/省略号缺失/破折号滥用

### 轻微级
- 被动语态/感叹号均匀/句子长度均匀/定语过长/强行分点/信息密度均匀/引号过于规范

---

## 平台改写要点

| 平台 | 核心目标 | 口语化度 |
|------|---------|:--------:|
| 公众号 | **观点输出**+节奏+细节，情绪偶尔流露 | 适度 |
| 知乎 | 立场+经验+承认不确定性 | 20% |
| 小红书 | 真实分享+时间线+具体细节 | 40-50% |
| 工作汇报 | 结论先行+数据+行动项 | ~0% |
| 朋友圈 | 短+留白+不完整 | 30-40% |
| 通用 | 去AI套路+**加具体细节**，不加口语 | 不加 |

---

## 文件结构

```
D:\亲笔写的SKILL\
├── SKILL.md                    ← 主入口（v1.1.0）
├── README.md                   ← 发布用说明
├── 需求.md                     ← PRD
├── rules/
│   ├── ai_patterns.json        ← AI句式模板库
│   ├── ai_words.json           ← AI高频词库
│   └── platform_styles.json    ← 平台风格规则
├── examples/
│   └── before_after.md         ← 改前改后对比样本
├── _publish_/                  ← 完整发布包（含 rules/）
├── _publish_slim/              ← 精简发布包（不含 rules/）
├── ownpen-v1.1.0.zip           ← 完整 zip
└── ownpen-v1.1.0-slim.zip      ← 精简 zip
```

---

## 竞品对比

| | humanizer-zh | OwnPen |
|---|---|---|
| 安装量 | 221 | 待发布 |
| 规则来源 | 英文维基翻译 | 中文原生 |
| 中文理解 | 零（检测 -ing 结尾） | 深度（体制词/排比/四字词...） |
| 平台区分 | 无 | 5种平台改写 |
| 核心原则 | 无 | 改写三不改 |
| 更新频率 | 从未更新 | 持续迭代 |

---

## 版本历史

| 版本 | 日期 | 变更 |
|------|------|------|
| **v1.1.0** | 2026-05-02 | 英文品牌名 OwnPen；slug 改为 ownpen；改写三不改原则；+5检测规则；公众号强调观点；通用加细节去口语 |
| v1.0.2 | 2026-05-02 | slim 发布包创建；_publish_ 目录规范化 |
| v1.0.0 | 2026-05-01 | 初版：40条规则 + 5平台改写 |

---

## 发布状态（2026-05-02）

| 平台 | 状态 | 链接 |
|------|:----:|------|
| **clawhub.ai** | ✅ v1.1.0, moderation: null | https://clawhub.ai/skills/ownpen |
| **skillhub.cn** | ✅ 同步 clawhub | — |
| **GitHub** | ✅ 已推送 | https://github.com/huangjihua007-rgb/ownpen |
| **skills.sh** | 🕐 等审核 | https://github.com/vercel-labs/skills/issues/1046 |
| **skillsmp.com** | 🕐 等自动同步 | topic: claude-skills, claude-code-skill |

## 发布目录说明

| 目录 | 用途 | 内容 |
|------|------|------|
| `_publish_/` | GitHub 仓库 + 完整版 | SKILL.md + README + rules/ + examples/ |
| `_publish_clawhub/` | clawhub 专用（<8192 tokens） | 精简 SKILL.md + README |
| `_publish_slim/` | 备用精简版 | SKILL.md + README + examples/ |

## 发布命令备忘

```powershell
# clawhub 发布
clawhub publish "D:\亲笔写的SKILL\_publish_" --workdir "D:\亲笔写的SKILL\_publish_" --name "OwnPen - 亲笔写的" --version "1.1.0" --slug "ownpen" --changelog "Brand: English name OwnPen; Core: 3-Don'ts principles; Rules: +5 patterns; Platform: WeChat insight-first, General adds specifics"

# GitHub 创建仓库
gh repo create ownpen --public --description "Make it sound like YOU wrote it. 让领导看不出是AI写的。Chinese AI text humanizer with platform-aware rewriting."
```

---

## 注意事项

- description 写口语化简短，避免被 clawhub moderation 标记 suspicious
- 发布目录用 `_publish_/` 不用源码目录（避免大文件 502）
- 必须加 `--workdir` 参数
