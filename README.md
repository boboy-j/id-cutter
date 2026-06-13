# 📸 AI 证件照制作工具

> 纯前端 AI 证件照制作工具 — 照片不上传服务器，隐私安全。

在线体验：**[https://你的用户名.github.io/id-photo](https://你的用户名.github.io/id-photo)**

## ✨ 功能特色

| 功能 | 说明 |
|------|------|
| 🎨 **AI 智能抠图** | 基于 @imgly/background-removal + ONNX Runtime，浏览器端本地处理 |
| 🖌️ **换背景色** | 白底 / 蓝底 / 红底 / 浅灰底 + 自定义颜色 |
| 📐 **标准证件照尺寸** | 1寸、小1寸、大1寸、2寸、小2寸、大2寸、社保卡、3寸、5寸、7寸 |
| 📖 **各国证件照规格百科** | 内置中国、美国、英国、欧盟、日本等多国规格库 |
| 🖨️ **多联排版打印** | 支持 4×6 等排版打印 |
| 🌙 **深色模式** | 一键切换主题 |
| 📱 **PWA 支持** | 可添加到主屏幕，像原生 App 一样使用 |
| 🔒 **隐私安全** | 纯前端处理，照片不上传任何服务器 |

## 🚀 部署到 GitHub Pages

### 方式一：直接推送

```bash
# 克隆仓库
git clone https://github.com/你的用户名/id-photo.git
cd id-photo

# 将 release 目录的内容复制到仓库根目录
cp -r path/to/release/* .

# 推送
git add .
git commit -m "init: AI 证件照制作工具"
git push
```

然后在仓库 Settings → Pages → 选择 `main` 分支，根目录即可。

### 方式二：使用 GitHub Actions（自动部署）

在仓库创建 `.github/workflows/deploy.yml`：

```yaml
name: Deploy to GitHub Pages
on:
  push:
    branches: [main]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: .
```

## 📱 iOS 添加到主屏幕

1. 在 iPhone Safari 浏览器中打开应用地址
2. 点击底部分享按钮（⬆️ 方框箭头图标）
3. 向下滑动，选择**「添加到主屏幕」**
4. 点击右上角**「添加」**
5. 主屏幕会出现应用图标，点击即可像原生 App 一样全屏使用

## 🧩 技术栈

- **AI 引擎**: ONNX Runtime Web + @imgly/background-removal
- **图像处理**: HTML5 Canvas
- **部署**: GitHub Pages（零服务器成本）
- **PWA**: Service Worker + Web App Manifest

## 📄 License

MIT License — 自由使用、修改、分发。
