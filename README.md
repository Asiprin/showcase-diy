# ShowcaseApp DIY 作品展

把闲置的屏幕，做成艺术电子相框。

社区 DIY 硬件作品展示站——展示大家用开源项目 [ShowcaseApp](https://github.com/mrjoechen/ShowcaseApp) 制作的实体数字相框作品。每件作品附成品介绍与硬件清单，看得见做法，也做得出来。

> **本站为社区作品展示，非官方。** 作品基于开源项目 ShowcaseApp 制作，本站与 ShowcaseApp 官方无关，作品内容由站长上传。

**在线访问：** https://asiprin.github.io/showcase-diy/

## 功能

**展示端（index.html）**
- 明信片帖子流：多图 / 视频作品可拖拽滑动切换，弹簧回弹手感，分段进度条与点状分页器
- 双击图片落下爱心，爱心/收藏即时反馈
- 点击图片浮动放大：背景模糊、多图循环翻页、键盘 ← → 支持
- 画框比例逐张自适应：横版 / 竖版 / 超宽素材各按原比例展示
- 视频默认静音播放，右下角一键开声
- 深浅色主题：跟随系统，可手动切换并记忆
- 响应式：桌面三栏，平板两栏，手机单栏

**管理后台（admin.html）**
- 四步上传向导：上传素材 → 填写信息（作者必填）→ 首页预览 → 发布
- 作品管理：编辑自动回填表单、删除、保存发布
- 首页文案全量可改：站名、首屏标题、简介、关于区、页脚
- 内容通过 GitHub API 提交到本仓库，GitHub Pages 自动发布，无需服务器

## 使用后台

1. 打开 `https://asiprin.github.io/showcase-diy/admin.html`
2. 填入仓库（`owner/repo`）、分支（`main`）和一个 Personal Access Token
   - **经典 Token（classic）**：勾选 `repo` 权限
   - **精细 Token（fine-grained）**：包含本仓库，Contents 权限设为 **Read and write**
3. 连接后即可上传作品、修改文案，点「发布」自动 commit 并生效（约 1 分钟）

> Token 只保存在你自己浏览器本地。请勿将 Token 发给他人或提交到仓库。

## 目录结构

```
├── index.html        # 前台展示页
├── admin.html        # 管理后台
├── data/
│   └── works.js      # 站点数据（作品、文案，由后台维护）
└── assets/
    └── media/        # 作品图片与视频
```

## 部署

本站是纯静态站，托管在 GitHub Pages：

1. 将本目录全部内容上传到仓库根目录
2. 仓库 **Settings → Pages**：Source 选 `Deploy from a branch`，Branch 选 `main` / `(root)`
3. 一两分钟后即可通过 `https://<用户名>.github.io/<仓库名>/` 访问

## 致谢

- [ShowcaseApp](https://github.com/mrjoechen/ShowcaseApp) —— 把设备变成数码相框的开源项目，本站全部作品的灵感来源
