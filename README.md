# 日序 · 个人事务工作台

海蓝与薄荷绿主题的个人项目与每日待办 PWA。仓库不包含个人项目、目标、待办或历史；所有新增数据仅保存在用户设备的网页存储中，不会提交到 GitHub。

## GitHub Pages 发布

1. 在 GitHub 仓库 Settings → Pages 中，将 Build and deployment 设为 Deploy from a branch。
2. 选择 `main` 分支和 `/(root)` 目录并保存。
3. 等待 GitHub Pages 完成发布。默认站点地址为 `https://<用户名>.github.io/rixu-personal-planner/`。
4. 用 iPhone Safari 打开该 HTTPS 地址，点分享 → 添加到主屏幕。

Pages 网站会公开访问，因此本仓库只放置空白应用代码。GitHub Pages 只托管网页文件，不保存应用中的项目和任务数据。

## 本机数据与提醒

- 第一次打开是空白工作台。项目、任务、进度历史保存在当前 iPhone 的网站存储中，不跨设备同步。
- 首次打开需联网加载；Service Worker 缓存页面后可离线重新进入。
- 提醒时间会被保存，但纯静态网页不能保证应用关闭或系统挂起时触发 iOS 提醒。
- 这是从主屏幕全屏运行的网页 App，不会生成 `.ipa`，不需要 Mac 或 Apple 开发者签名。

## 文件

- `index.html`：界面、业务逻辑和本机数据存储
- `manifest.webmanifest`：主屏幕名称、颜色、图标配置
- `service-worker.js`：离线缓存与更新
- 根目录 PNG/SVG 文件：网页与 iPhone 主屏幕图标
- `.nojekyll`：让 GitHub Pages 原样提供静态 PWA 文件
