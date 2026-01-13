# 📝 GitHub Profile 配置指南

这份指南将帮助你进一步个性化你的 GitHub Profile。

## ✅ 已完成的功能

- ✨ 动态标题横幅
- 🎯 打字机动画效果
- 📊 GitHub 统计卡片
- 🏆 GitHub 奖杯
- 📈 活动图表
- 🔥 连续贡献统计
- 🐍 贡献蛇形动画（自动生成）
- 💬 每日开发者名言

## 🔧 需要你自定义的部分

### 1. 更新社交媒体链接（README.md 第 194-197 行）

找到这部分代码并更新为你的真实链接：

```markdown
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@example.com)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/yourusername)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/yourusername)
```

替换为：
- `your.email@example.com` → 你的真实邮箱
- `https://twitter.com/yourusername` → 你的 Twitter 链接（如果没有可以删除）
- `https://linkedin.com/in/yourusername` → 你的 LinkedIn 链接（如果没有可以删除）

### 2. 启用 Snake 动画

Snake 动画已经配置好了，但需要手动运行一次：

1. 前往 https://github.com/Z3FisherX/Z3FisherX/actions
2. 点击 "Generate Snake Animation" workflow
3. 点击 "Run workflow" 按钮
4. 等待几分钟让动画生成完成

### 3. 可选：添加 WakaTime 统计

如果你想展示每周编码时间统计：

1. 注册 [WakaTime](https://wakatime.com/)
2. 安装 WakaTime 插件到 VS Code
3. 在 GitHub 仓库设置中添加 `WAKATIME_API_KEY` secret
4. 在你的仓库中创建 `.github/workflows/waka-readme.yml`：

```yaml
name: Waka Readme

on:
  schedule:
    - cron: '0 0 * * *'
  workflow_dispatch:

jobs:
  update-readme:
    name: Update Readme with Metrics
    runs-on: ubuntu-latest
    steps:
      - uses: anmol098/waka-readme-stats@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### 4. 可选：添加 Spotify 正在播放

如果你想显示你正在听的音乐：

1. 参考 [novatorem](https://github.com/novatorem/novatorem) 设置
2. 部署到 Vercel
3. 更新 README 中的 Spotify 链接

### 5. 自定义项目展示

根据你想重点展示的项目，修改 README.md 中的 Featured Projects 部分（第 99-111 行）。

当前展示的项目：
- yapi-to-ts
- report-error  
- codeSetting

你可以替换为其他公开仓库。

### 6. 调整个人信息

在 README.md 的第 25-45 行，更新 `Z3FisherX` 对象中的信息：

```typescript
const Z3FisherX = {
    location: "China 🇨🇳",  // 你的位置
    role: "Full-Stack Developer",  // 你的职位
    // ... 其他信息
    funFact: "你的有趣事实"
};
```

## 🎨 主题配置

当前使用的主题是 `tokyonight`，你可以换成其他主题：

可用主题：
- `dark`, `radical`, `merko`, `gruvbox`, `tokyonight`
- `onedark`, `cobalt`, `synthwave`, `highcontrast`, `dracula`

修改方法：在 README.md 中搜索 `theme=tokyonight`，替换为你喜欢的主题名称。

## 📱 添加更多徽章

访问 [shields.io](https://shields.io/) 或 [badgen.net](https://badgen.net/) 生成更多自定义徽章。

## 🔄 定期更新

- Snake 动画：每天自动更新
- GitHub 统计：实时更新
- WakaTime 统计（如果启用）：每天更新

## 📚 参考资源

- [Awesome GitHub Profile README](https://github.com/abhisheknaiidu/awesome-github-profile-readme)
- [GitHub Profile README Generator](https://rahuldkjain.github.io/gh-profile-readme-generator/)
- [Shields.io](https://shields.io/)
- [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats)

## 💡 提示

1. 保持 README 简洁，不要添加过多内容
2. 定期更新你的项目展示
3. 确保所有链接都是有效的
4. 根据实际情况调整技术栈徽章
5. 删除不需要的部分（如 Spotify、WakaTime 等）

---

祝你的 GitHub Profile 越来越完善！🎉
