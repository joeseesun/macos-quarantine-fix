# Mac 应用打不开？一键修复

macOS 提示「应用已损坏」或「无法验证开发者」？把应用拖进来，一键生成修复命令。

## 在线使用

访问 → [macos-quarantine-fix.vercel.app](https://macos-quarantine-fix.vercel.app)

## 一键部署

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fjoeseesun%2Fmacos-quarantine-fix)

## 原理

macOS 会给所有从网上下载的文件打上「隔离标记」(`com.apple.quarantine`)。如果应用没有经过 Apple 官方公证，系统就会阻止运行。

本工具生成的命令只是去掉这个标记，不会修改应用本身：

```bash
sudo xattr -rd com.apple.quarantine /Applications/YourApp.app
```

## 功能

- 🖱️ 拖拽 `.app` / `.dmg` 文件自动识别
- 📁 点击浏览选择文件
- ⌨️ 手动输入应用路径
- 📋 一键复制命令
- 🌗 自动适配深色/浅色模式
- 📱 响应式设计，支持手机访问

## 本地运行

纯静态 HTML，无需构建：

```bash
open index.html
```

## 📱 关注作者

如果这个项目对你有帮助，欢迎关注我获取更多技术分享：

- **X (Twitter)**: [@vista8](https://x.com/vista8)
- **微信公众号「向阳乔木推荐看」**:

<p align="center">
  <img src="https://github.com/joeseesun/terminal-boost/raw/main/assets/wechat-qr.jpg?raw=true" alt="向阳乔木推荐看公众号二维码" width="300">
</p>

## License

MIT
