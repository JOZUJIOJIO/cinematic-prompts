# 🎬 Seedance Cinematic Video — AI视频提示词引擎

<div align="center">

**即梦2.0 (Seedance 2.0) 电影级视频提示词生成器**

[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)](https://github.com/JOZUJIOJIO/cinematic-prompts)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-purple.svg)](https://claude.ai/claude-code)
[![Platform](https://img.shields.io/badge/Platform-即梦2.0%20%7C%20Seedance%202.0-orange.svg)](https://jimeng.jianying.com)

[English](#english) | [中文](#中文)

</div>

---

## 中文

### 📖 简介

专为**即梦 2.0 (Seedance 2.0)** 设计的 Claude Code SKILL，从故事/剧本到可直接粘贴的电影级提示词，一键完成。

**核心原则：**
- 🎭 **角色即变量** — 每个角色注册为 `@图片N` 槽位，保持多镜头一致性
- ⏱️ **4-15秒硬约束** — 严格遵守即梦2.0平台限制，智能分配每镜头时长
- 🎵 **音画原生同步** — 口型同步、环境音效、BGM 全部写入提示词
- 📋 **素材准备清单** — 自动生成需要上传的参考图/音频列表

### ✨ 功能特点

- 🎭 **@槽位系统** — 角色/场景/道具/音频全部注册为变量（最多9图+3视频+3音频）
- ⏱️ **智能时长判定** — 基于角色数/动作复杂度/运镜幅度/对白时长综合计算
- 🎬 **六层提示词结构** — 角色层+场景层+镜头层+光影层+音频层+约束层
- 🎵 **音频层** — 口型同步、环境音效、BGM写入提示词
- 📋 **素材准备清单** — 每个分镜附带完整的素材槽位说明和用户操作指引
- ✅ **质量检查清单** — 结构/提示词/输出三层自动验证

### 🚀 快速开始

#### 1. 克隆仓库

```bash
git clone https://github.com/JOZUJIOJIO/cinematic-prompts.git
cd cinematic-prompts
```

#### 2. 在 Claude Code 中使用

```bash
/skill seedance-cinematic-video
```

#### 3. 开始创作

告诉 SKILL 你的场景，例如：

```
帮我生成《让子弹飞》火车上提字诗场景的即梦2.0分镜提示词
主角：马邦德（圆脸，西装）、县长夫人（旗袍）
场景：火车餐车厢，民国风格
```

SKILL 会自动：
1. 注册角色表（每个角色 = `@图片N` 槽位）
2. 生成素材准备清单
3. 智能拆分镜头并判定时长（4-15秒）
4. 逐镜头生成六层提示词（含口型同步音频层）
5. 输出每个镜头的用户操作指引

### 📏 平台约束（即梦2.0）

| 约束 | 值 |
|------|-----|
| 单镜头时长 | **4-15秒**（硬上限） |
| 图片参考上限 | 9张 |
| 视频参考上限 | 3段，总时长≤15秒 |
| 音频参考上限 | 3段，总时长≤15秒 |
| 混合上传总上限 | 12个文件 |

### 📂 项目结构

```
cinematic-prompts/
├── LICENSE
├── README.md
├── skills/
│   └── seedance-cinematic-video/
│       ├── skill.json          # SKILL 元信息
│       └── prompts/
│           └── main.md         # 核心提示词引擎（六层结构）
└── examples/
    ├── README.md
    └── narrative/
        └── 让子弹飞_提字诗场景_Seedance2.0.md   # 完整示例
```

### 🎯 工作流程

```
用户输入：故事/剧本/场景描述
    ↓
Step 1: 剧本分析 → 角色表 + 场景表 + 道具表
    ↓
Step 2: 素材槽位注册 → @图片N / @视频N / @音频N
    ↓
Step 3: 智能分镜 → 拆镜头 + 时长判定（4-15s）
    ↓
Step 4: 逐镜头六层提示词
    ↓
Step 5: 输出提示词 + 素材清单 + 用户操作指引
```

### 📋 六层提示词结构

```
[角色层] @图片N 的角色[具体动作]，[表情]，[姿态]
[场景层] 在 @图片K 的场景中，[环境细节]，[时间天气]
[镜头层] [景别]，镜头[运镜方式+速度+方向]
[光影层] [光线类型]，[色调]，[氛围风格]
[音频层] [环境音效]。角色说出 @音频N 的对白，口型同步。[配乐]
[约束层] 画面流畅稳定，面部清晰不变形，保持@图片N角色一致性，8K超高清，电影级质感
```

### 💡 示例

查看 `examples/` 目录：
- [《让子弹飞》提字诗场景完整分镜（6镜头）](./examples/narrative/让子弹飞_提字诗场景_Seedance2.0.md)

---

## English

### 📖 Introduction

A Claude Code SKILL designed specifically for **Seedance 2.0 (即梦 2.0)** by ByteDance. Turns stories/scripts into cinematic-quality prompts ready to paste into the platform.

**Core principles:**
- 🎭 **Characters as variables** — Each character registered as `@imageN` slot for multi-shot consistency
- ⏱️ **4-15 second hard constraint** — Strictly follows Seedance 2.0 platform limits with intelligent duration allocation
- 🎵 **Native audio-video sync** — Lip sync, ambient sounds, BGM all written into prompts
- 📋 **Asset checklist** — Auto-generates list of reference images/audio to upload

### 🚀 Quick Start

```bash
git clone https://github.com/JOZUJIOJIO/cinematic-prompts.git
cd cinematic-prompts
```

```bash
/skill seedance-cinematic-video
```

Tell the SKILL your scene, for example:
- "Generate Seedance 2.0 prompts for a train dining car scene with two characters"
- "Create a 6-shot action sequence with a hero character"

### 📏 Platform Constraints (Seedance 2.0)

| Constraint | Value |
|-----------|-------|
| Shot duration | **4-15 seconds** (hard limit) |
| Image references | Up to 9 |
| Video references | Up to 3, total ≤15s |
| Audio references | Up to 3, total ≤15s |
| Total files | Up to 12 |

### 🛠️ Supported Platform

**AI Video Generation**: Seedance 2.0 / 即梦 2.0 (ByteDance)

### 📄 License

[MIT License](./LICENSE)

---

<div align="center">

**Built with ❤️ by Cyber Bayes**

[Report Bug](https://github.com/JOZUJIOJIO/cinematic-prompts/issues) · [Request Feature](https://github.com/JOZUJIOJIO/cinematic-prompts/issues)

</div>
