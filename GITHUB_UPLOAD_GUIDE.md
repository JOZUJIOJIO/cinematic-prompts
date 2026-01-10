# 📤 GitHub 上传指南

本指南将帮助你将 Cinematic Prompts Generator 上传到 GitHub。

---

## 🚀 快速上传步骤

### 1. 在 GitHub 上创建新仓库

1. 访问 [GitHub](https://github.com)
2. 点击右上角的 `+` 按钮
3. 选择 `New repository`
4. 填写仓库信息:
   - **Repository name**: `cinematic-prompts` (或你喜欢的名称)
   - **Description**: `🎬 Professional cinematic AI prompt generator for image-to-video workflows`
   - **Public/Private**: 选择 `Public` (推荐)
   - **不要勾选** "Initialize this repository with a README" (我们已经有了)
   - 不要添加 .gitignore 或 License (我们已经创建了)
5. 点击 `Create repository`

### 2. 连接本地仓库到 GitHub

在你的终端中执行以下命令:

```bash
# 确保在项目目录中
cd /Users/yewudao/Desktop/cinematic-prompts

# 添加远程仓库(替换 YOUR_USERNAME 为你的 GitHub 用户名)
git remote add origin https://github.com/YOUR_USERNAME/cinematic-prompts.git

# 推送到 GitHub
git push -u origin main
```

### 3. 推送完成后

访问你的 GitHub 仓库页面，你应该能看到:
- ✅ 完整的 README.md 首页展示
- ✅ 所有文件和目录
- ✅ MIT License 标识
- ✅ 完整的项目结构

---

## 🎨 GitHub 仓库优化建议

### 添加 Topics (标签)

在 GitHub 仓库页面点击 `Add topics`，添加以下标签:

```
claude-code
ai-prompts
cinematic
video-generation
midjourney
runway
pika
stable-diffusion
prompt-engineering
storyboard
filmmaking
ai-art
```

### 设置 About 描述

在仓库页面右侧的 "About" 区域点击设置图标:
- **Description**: `🎬 Professional cinematic AI prompt generator with separated image and video prompts for modern AI workflows`
- **Website**: (可选) 添加你的个人网站或文档链接
- **Topics**: 参考上面的标签列表

### 启用 GitHub Pages (可选)

如果你想创建一个在线文档网站:

1. 进入仓库的 `Settings` > `Pages`
2. 在 `Source` 下选择 `main` 分支
3. 选择 `/ (root)` 或 `/docs` 文件夹
4. 点击 `Save`

---

## 📝 更新 README 中的链接

上传后，记得更新 README.md 中的占位符链接:

```bash
# 打开 README.md 文件
nano README.md  # 或使用你喜欢的编辑器

# 将所有 "yourusername" 替换为你的实际 GitHub 用户名
# 例如: https://github.com/yourusername/cinematic-prompts
# 改为: https://github.com/your-actual-username/cinematic-prompts
```

然后提交更新:

```bash
git add README.md
git commit -m "docs: update repository links"
git push
```

---

## 🌟 推广你的项目

### 1. 创建 Release

创建第一个正式版本:

1. 在 GitHub 仓库页面点击 `Releases`
2. 点击 `Create a new release`
3. 填写信息:
   - **Tag version**: `v2.0.0`
   - **Release title**: `🎉 Cinematic Prompts Generator v2.0.0`
   - **Description**: 复制 CHANGELOG.md 中的 v2.0.0 部分
4. 点击 `Publish release`

### 2. 分享到社区

可以在以下平台分享:
- Reddit: r/StableDiffusion, r/midjourney, r/RunwayML
- Discord: Midjourney, Pika Labs, Runway 官方服务器
- Twitter/X: 使用标签 #AIArt #Midjourney #Runway
- Product Hunt: 提交你的项目

### 3. 鼓励贡献

在 GitHub 仓库中:
1. 创建 `CONTRIBUTING.md` 文件说明如何贡献
2. 添加 Issue 模板
3. 添加 Pull Request 模板

---

## 🔒 安全提示

- ✅ 不要在仓库中包含任何 API 密钥或敏感信息
- ✅ .gitignore 已经配置好忽略临时文件和敏感文件
- ✅ MIT License 允许他人自由使用和修改

---

## 📊 Git 常用命令参考

```bash
# 查看状态
git status

# 查看提交历史
git log --oneline

# 添加文件
git add <file>
git add .  # 添加所有文件

# 提交更改
git commit -m "描述你的更改"

# 推送到 GitHub
git push

# 拉取最新更改
git pull

# 查看远程仓库
git remote -v

# 创建新分支
git checkout -b feature-branch-name

# 切换分支
git checkout main
```

---

## ❓ 常见问题

### Q: 推送时要求输入用户名和密码?

从 2021 年起，GitHub 不再支持密码验证。你需要:
1. 生成 Personal Access Token (PAT)
2. 或配置 SSH 密钥

**推荐方式 - 使用 SSH**:

```bash
# 1. 生成 SSH 密钥
ssh-keygen -t ed25519 -C "your_email@example.com"

# 2. 添加到 ssh-agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# 3. 复制公钥
cat ~/.ssh/id_ed25519.pub

# 4. 在 GitHub Settings > SSH and GPG keys 中添加
# 5. 更改远程仓库 URL
git remote set-url origin git@github.com:YOUR_USERNAME/cinematic-prompts.git
```

### Q: 如何更新已上传的文件?

```bash
# 1. 修改文件后
git add <modified-files>
git commit -m "描述你的更改"
git push
```

### Q: 如何删除 GitHub 上的文件?

```bash
# 删除本地文件
git rm <file>
# 或删除整个目录
git rm -r <directory>

# 提交删除
git commit -m "remove: 删除文件说明"
git push
```

---

## 🎯 下一步

上传成功后，你可以:

1. ⭐ 邀请朋友给项目点星
2. 📝 写一篇博客介绍你的项目
3. 🎥 录制使用教程视频
4. 🤝 接受社区贡献
5. 📈 定期更新和维护

---

## 📞 需要帮助?

如果遇到问题:
- 📖 查看 [GitHub 官方文档](https://docs.github.com)
- 💬 在 [GitHub Community](https://github.com/community) 提问
- 🔍 搜索 [Stack Overflow](https://stackoverflow.com/questions/tagged/github)

---

**祝你的项目获得成功！🎉**

记得在上传完成后删除此指南文件:
```bash
git rm GITHUB_UPLOAD_GUIDE.md
git commit -m "docs: remove upload guide"
git push
```
