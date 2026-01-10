# ⚡ 快速开始指南 | Quick Start Guide

**只需 3 步，开始创作电影级 AI 视频！**

---

## 🎯 30 秒快速开始

### 中文用户

```bash
# 1. 进入项目目录
cd /path/to/cinematic-prompts

# 2. 启动 Claude Code 并调用 SKILL
/skill cinematic-prompts

# 3. 告诉它你想要什么
"创建一个浪漫日落场景的分镜脚本"
```

### English Users

```bash
# 1. Navigate to project
cd /path/to/cinematic-prompts

# 2. Launch Claude Code and invoke SKILL
/skill cinematic-prompts

# 3. Describe what you need
"Create a romantic sunset scene storyboard"
```

**就是这么简单！✨**

---

## 🎬 完整工作流程

### 第一步: 生成分镜脚本

使用 SKILL 生成完整的分镜脚本，获得:
- 📄 详细的 Markdown 文档
- 📊 结构化的 JSON 数据
- 🖼️ 图片生成提示词
- 🎥 图转视频提示词

### 第二步: 生成图片

将**图片生成提示词**复制到:

**Midjourney**:
```
/imagine [粘贴图片提示词] --ar 2.39:1 --v 6
```

**DALL-E 3**:
```
直接粘贴图片提示词
```

**Stable Diffusion**:
```
粘贴图片提示词 + 选择合适的模型
```

### 第三步: 转换为视频

将生成的图片导入图转视频工具:

**Runway Gen-3**:
1. 上传图片
2. 选择 "Image to Video"
3. 粘贴**图转视频提示词**
4. 设置时长(建议 4-7 秒)
5. 生成视频

**Pika Labs**:
1. 上传图片
2. 在 Motion 描述框粘贴**图转视频提示词**
3. 调整 Motion 强度(建议 0.3-0.5)
4. 生成视频

### 第四步: 剪辑合成

在视频编辑软件中:
1. 按顺序导入所有视频片段
2. 添加转场效果(参考脚本中的转场建议)
3. 添加音效和背景音乐
4. 调色和最终输出

---

## 💡 示例场景

### 场景 1: 浪漫日落
```
需求: "创建一个浪漫日落场景的分镜脚本"
镜头数: 6 个
风格: 温暖、浪漫、自然主义
时长: 30-35 秒
```

### 场景 2: 科幻城市
```
需求: "生成一个赛博朋克城市夜景的 8 个镜头"
镜头数: 8 个
风格: 赛博朋克、霓虹灯、未来感
时长: 40-50 秒
```

### 场景 3: 自然风光
```
需求: "制作山林清晨的 5 个镜头系列"
镜头数: 5 个
风格: 自然、宁静、晨光
时长: 25-30 秒
```

---

## 🛠️ 推荐工具组合

### 免费方案
- **图片**: Stable Diffusion (本地部署)
- **视频**: Stability AI SVD (本地)
- **剪辑**: DaVinci Resolve (免费版)

### 付费方案
- **图片**: Midjourney ($10/月起)
- **视频**: Runway Gen-3 ($12/月起)
- **剪辑**: Adobe Premiere Pro

### 最佳方案
- **图片**: Midjourney v6 (质量最高)
- **视频**: Runway Gen-3 (运动控制最精准)
- **剪辑**: DaVinci Resolve Studio (专业调色)

---

## 🎨 提示词使用技巧

### 图片提示词技巧

1. **保持完整性**: 不要删减技术参数
2. **调整画幅**: 根据需要修改 aspect ratio
3. **风格微调**: 可添加艺术家风格(如 "in the style of...")
4. **质量控制**: 保留 "cinematic", "professional" 等关键词

### 视频提示词技巧

1. **控制速度**: 调整运动速度(0.2x-1.5x)
2. **方向明确**: 确保运动方向清晰
3. **强度适中**: 避免过度运动导致画面失真
4. **时长匹配**: 根据提示词建议设置视频时长

---

## ⚠️ 常见问题

### Q: 生成的图片不符合预期？

**A**: 尝试:
1. 调整提示词中的关键词权重
2. 在 Midjourney 中使用 `--chaos` 参数增加变化
3. 多次生成选择最佳结果
4. 参考技术参数调整构图

### Q: 视频运动太剧烈或太弱？

**A**: 调整:
1. 修改速度参数(如 0.3x → 0.5x)
2. 在工具中调整 Motion Strength
3. 简化运动描述,只保留核心动作
4. 分多次尝试找到最佳参数

### Q: 如何保持镜头间的一致性？

**A**: 建议:
1. 使用相同的风格描述词
2. 保持色调和光线一致
3. 在 Midjourney 中使用 `--seed` 参数
4. 后期统一调色

---

## 🚀 进阶技巧

### 1. 批量生成

创建一个脚本文件:
```bash
#!/bin/bash
# batch_generate.sh

scenes=("浪漫日落" "科幻城市" "自然风光")

for scene in "${scenes[@]}"; do
    echo "生成 $scene 场景..."
    # 调用 SKILL 并保存输出
done
```

### 2. 自定义模板

修改 `skills/cinematic-prompts/prompts/main.md`:
- 添加你常用的风格预设
- 自定义镜头类型
- 调整输出格式

### 3. 工具集成

将生成的 JSON 数据导入:
- Notion (项目管理)
- Airtable (数据库)
- 自定义脚本(批处理)

---

## 📚 学习资源

### 电影术语
- [电影摄影基础](https://www.masterclass.com/classes/martin-scorsese-teaches-filmmaking)
- [镜头语言指南](https://www.studiobinder.com/blog/types-of-camera-movements/)

### AI 工具教程
- [Midjourney 官方文档](https://docs.midjourney.com/)
- [Runway 教程](https://runwayml.com/tutorials/)
- [Pika Labs Discord](https://discord.gg/pika)

### 社区
- Reddit: r/StableDiffusion, r/midjourney
- Discord: 各工具官方服务器
- YouTube: AI 视频创作教程

---

## ✅ 检查清单

开始创作前确保:

- [ ] Claude Code 已安装并配置
- [ ] 已选择合适的图片生成工具
- [ ] 已准备好图转视频工具账号
- [ ] 有基本的视频编辑软件
- [ ] 了解基本的镜头语言

---

## 🎯 你的第一个作品

**建议从简单开始**:

1. **第一次**: 使用提供的"浪漫日落场景"示例
   - 复制提示词直接使用
   - 熟悉整个流程
   - 完成第一个作品

2. **第二次**: 修改示例
   - 改变场景(海边→山顶)
   - 调整色调(暖色→冷色)
   - 尝试不同工具

3. **第三次**: 完全原创
   - 使用 SKILL 生成新场景
   - 应用学到的技巧
   - 创作独特作品

---

## 🎉 开始创作吧！

你已经准备好了:
- ✅ SKILL 已配置
- ✅ 工具已了解
- ✅ 流程已清楚

**现在就开始你的第一个电影级 AI 视频创作！**

有问题随时查看:
- 📖 [完整文档](./README.md)
- 💡 [示例](./examples/)
- 🐛 [提交 Issue](https://github.com/yourusername/cinematic-prompts/issues)

---

**祝创作愉快！🎬✨**
