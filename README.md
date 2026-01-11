# 🎬 Cinematic Prompts Generator

<div align="center">

**专业的电影级 AI 提示词生成器 v3.0 | Professional Cinematic AI Prompt Generator**

[![Version](https://img.shields.io/badge/version-3.0.0-blue.svg)](https://github.com/JOZUJIOJIO/cinematic-prompts)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-purple.svg)](https://claude.ai/claude-code)

[English](#english) | [中文](#中文)

</div>

---

## 中文

### 📖 简介

这是一个专业的 Claude Code SKILL，用于生成电影级别的 AI 提示词系列。v3.0 采用全新的三层提示词架构，基于时长自动计算画面数量，智能选择最佳镜头类型，为每个画面生成完整的视频制作参数。

**v3.0 核心创新**：
- **时长驱动工作流**：输入期望时长，自动计算画面数量（每画面5秒）
- **三层提示词架构**：画面提示词 → 镜头提示词 → 视频转换提示词
- **智能自动选镜**：基于叙事节奏、内容匹配、视觉多样性、情绪强度四大规则
- **12种运镜库 + 10种过渡效果**：专业电影语言库，智能匹配

### ✨ 功能特点

- ⏱️ **时长驱动** - 输入视频时长，自动计算最优画面数量
- 🎯 **三层提示词** - 画面提示词(JSON) + 镜头提示词(7种景别) + 视频转换提示词
- 🤖 **智能选镜** - AI自动选择最合适的景别，并输出详细理由
- 🎥 **7种标准景别** - EWS/LS/MLS/MS/MCU/CU/ECU，每种包含完整技术参数
- 📹 **12种专业运镜** - Static/Pan/Tilt/Dolly/Tracking/Orbit/Drone等，含速度和情绪定义
- 🎞️ **10种过渡效果** - Cut/Fade/Dissolve/Match Cut/Jump Cut等，含时长和情绪匹配
- 🎵 **BGM智能匹配** - 10种氛围分类，自动推荐音乐类型和作曲家参考
- 🎨 **好莱坞标准** - 专业导演级场景描述和电影叙事规则

### 🚀 快速开始

#### 1. 克隆仓库

```bash
git clone https://github.com/JOZUJIOJIO/cinematic-prompts.git
cd cinematic-prompts
```

#### 2. 在 Claude Code 中使用

```bash
# 确保在项目目录中
pwd  # 应显示 .../cinematic-prompts

# 调用 SKILL
/skill cinematic-prompts
```

#### 3. 开始创作

告诉 SKILL 你的需求，例如：
- "我想制作一个60秒的科幻短片，讲述宇航员在月球基地的一天"
- "帮我生成一个30秒的浪漫求婚场景视频脚本"
- "制作一个90秒的动作追逐场景分镜"

SKILL 会自动：
1. 计算画面数量（60秒 ÷ 5秒 = 12个画面）
2. 逐画面生成完整的三层提示词
3. 自动选择最合适的镜头景别
4. 为每个画面配置运镜、过渡、BGM建议

### 📂 项目结构

```
cinematic-prompts/
├── .clauderc                    # Claude Code 配置
├── .gitignore                   # Git 忽略文件
├── LICENSE                      # MIT 许可证
├── README.md                    # 本文件
├── CHANGELOG.md                 # 版本更新日志
├── skills/
│   └── cinematic-prompts/
│       ├── skill.json          # SKILL 定义
│       └── prompts/
│           └── main.md         # 核心提示词模板
└── examples/
    ├── 浪漫日落场景_分镜脚本_v2.md    # 示例输出
    └── README.md               # 示例说明
```

### 🎯 v3.0 工作流程

```
用户输入：剧本 + 期望时长(秒)
    ↓
自动计算：画面数 = 时长 ÷ 5秒
    ↓
用户确认：画面数量
    ↓
FOR 每个画面 (1 到 N):
    ├─ 步骤1: 生成画面提示词 (JSON格式，好莱坞标准)
    ├─ 步骤2: 生成7种镜头提示词 (基于画面提示词+景别模板)
    ├─ 步骤3: AI自动选择最合适镜头 (输出选择理由)
    └─ 步骤4: 生成视频转换提示词 (运镜+过渡+BGM)
    ↓
输出完整Markdown分镜脚本
```

### 📦 三层提示词架构

#### 1️⃣ 画面提示词 (Scene Prompt)
**JSON格式，包含**：
- 场景描述（环境、角色、动作）
- 光线设置（类型、方向、强度、色温）
- 色彩基调（主色调、对比度、饱和度）
- 氛围情绪（整体感觉、情感基调）
- Scene DNA（人物/环境/风格固定特征，权重1.3-1.5）

#### 2️⃣ 镜头提示词 (Shot Prompt)
**动态生成7种景别**：
1. EWS (远景) - 14-24mm, f/8-f/11
2. LS (全景) - 24-35mm, f/5.6-f/8
3. MLS (中远景) - 35-50mm, f/4-f/5.6
4. MS (中景) - 50mm, f/4
5. MCU (中近景) - 50-85mm, f/2.8-f/4
6. CU (近景) - 85-100mm, f/1.4-f/2.8
7. ECU (特写) - 100mm+ Macro, f/2.0-f/2.8

#### 3️⃣ 视频转换提示词 (Video Prompt)
**包含**：
- 选中的镜头提示词（完整内容）
- 运镜方式（12种标准运镜库智能选择）
- 过渡效果（10种过渡效果库智能匹配）
- BGM建议（10种氛围分类自动匹配）
- 完整技术参数（焦距/光圈/帧率/画幅）

### 🛠️ 适用工具

**图片生成**：
- Midjourney v6
- DALL-E 3
- Stable Diffusion XL

**图转视频**：
- Runway Gen-2/Gen-3
- Pika Labs 1.5
- Stability AI SVD

### 💡 v3.0 新特性详解

#### 🤖 智能自动选镜系统
基于四大规则自动选择最佳景别：
1. **叙事节奏**：开场用远景，高潮用近景/特写，结尾回到远景
2. **内容匹配**：环境为主用EWS/LS，对话用MS/MCU，情绪用CU/ECU
3. **视觉多样性**：避免连续重复，创造推拉节奏（LS→MS→CU→MS→LS）
4. **情绪强度**：平静用MS/LS，紧张用MCU/CU，爆发用CU/ECU

#### 📹 12种专业运镜库
- **基础运镜**：Static, Pan, Tilt, Dolly, Truck, Crane
- **高级运镜**：Tracking, Orbit, Dolly Zoom, Handheld, Drone, POV Walking
- 每种运镜包含：速度参数(0.3x/0.5x/1.0x)、情绪定义、适用场景

#### 🎞️ 10种过渡效果库
- **基础过渡**：Cut, Fade In/Out, Dissolve, Fade to White, Wipe
- **高级过渡**：Match Cut, Jump Cut, L Cut/J Cut, Defocus, Morph
- 每种过渡包含：时长规范、适用场景、情绪匹配

#### 🎵 BGM智能匹配系统
10种氛围自动匹配音乐类型：
- 史诗/壮观 → Hans Zimmer风格管弦乐
- 浪漫/温馨 → Yiruma风格钢琴
- 悬疑/紧张 → Trent Reznor风格电子音效
- 科幻/未来 → Vangelis风格合成器
- (更多详见文档)

### 💡 使用示例

查看 `examples/` 目录获取完整示例：
- [v2.0 浪漫日落场景分镜脚本](./examples/浪漫日落场景_分镜脚本_v2.md)
- v3.0 示例即将更新

### 🤝 贡献

欢迎提交 Issue 和 Pull Request！

### 📄 许可证

本项目采用 [MIT 许可证](./LICENSE)

### 🙏 致谢

- 基于 [Claude Code](https://claude.ai/claude-code) 构建
- 感谢所有贡献者

---

## English

### 📖 Introduction

A professional Claude Code SKILL for generating cinematic-quality AI prompts. v3.0 introduces a revolutionary three-layer prompt architecture with duration-based scene calculation and intelligent shot selection.

**v3.0 Key Innovations**:
- **Duration-Driven Workflow**: Input desired duration, auto-calculate scene count (5 sec/scene)
- **Three-Layer Prompt Architecture**: Scene Prompt → Shot Prompt → Video Prompt
- **Intelligent Auto-Selection**: AI chooses optimal shot types based on 4 narrative rules
- **12 Camera Movements + 10 Transitions**: Professional film language library

### ✨ Features

- ⏱️ **Duration-Driven** - Input video duration, auto-calculate optimal scene count
- 🎯 **Three-Layer Prompts** - Scene(JSON) + Shot(7 types) + Video(final)
- 🤖 **Smart Selection** - AI auto-selects best shot type with reasoning
- 🎥 **7 Standard Shots** - EWS/LS/MLS/MS/MCU/CU/ECU with complete specs
- 📹 **12 Pro Movements** - Static/Pan/Tilt/Dolly/Tracking/Orbit/Drone with speed & emotion
- 🎞️ **10 Transitions** - Cut/Fade/Dissolve/Match Cut/Jump Cut with timing & mood
- 🎵 **BGM Matching** - 10 mood categories with composer references
- 🎨 **Hollywood Standard** - Professional director-level scene descriptions

### 🚀 Quick Start

#### 1. Clone Repository

```bash
git clone https://github.com/JOZUJIOJIO/cinematic-prompts.git
cd cinematic-prompts
```

#### 2. Use in Claude Code

```bash
# Make sure you're in the project directory
pwd  # Should show .../cinematic-prompts

# Invoke the SKILL
/skill cinematic-prompts
```

#### 3. Start Creating

Tell the SKILL what you need:
- "Create a 60-second sci-fi short film about an astronaut's day on a lunar base"
- "Generate a 30-second romantic proposal scene"
- "Make a 90-second action chase sequence"

The SKILL will automatically:
1. Calculate scene count (60sec ÷ 5sec = 12 scenes)
2. Generate three-layer prompts for each scene
3. Auto-select optimal shot types
4. Configure camera movement, transitions, and BGM

### 🛠️ Supported Tools

**Image Generation**:
- Midjourney v6
- DALL-E 3
- Stable Diffusion XL

**Image-to-Video**:
- Runway Gen-2/Gen-3
- Pika Labs 1.5
- Stability AI SVD

### 💡 Examples

Check the `examples/` directory for complete examples:
- [Romantic Sunset Scene Storyboard](./examples/浪漫日落场景_分镜脚本_v2.md)

### 🤝 Contributing

Issues and Pull Requests are welcome!

### 📄 License

This project is licensed under the [MIT License](./LICENSE)

### 🙏 Acknowledgments

- Built with [Claude Code](https://claude.ai/claude-code)
- Thanks to all contributors

---

<div align="center">

**Made with ❤️ by the community**

[Report Bug](https://github.com/JOZUJIOJIO/cinematic-prompts/issues) · [Request Feature](https://github.com/JOZUJIOJIO/cinematic-prompts/issues)

</div>
