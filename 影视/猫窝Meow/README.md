## 猫窝 Meow

猫窝 Meow 是一款开源跨端影视客户端：手机、电脑、电视、NAS 同源同进度，支持点播、直播、弹幕、片库与本地播放。TV 端基于 Android WebView + 端上 JVM 宿主，可直接加载 FongMi / TVBox / 猫窝生态的 spider jar 以及 JS / PY 扩展源，站点配置由用户自行导入。

- 项目主页：https://github.com/upchr/meow
- 文档站：https://upchr.github.io/meow/
- 开源协议：Apache-2.0
- 作者：upchr

## 下载地址

| 平台 | 版本 | 下载 |
| --- | --- | --- |
| Android TV | v1.2.28 | [meow-TV-1.2.28.apk](https://github.com/upchr/meow/releases/download/release-v1.2.28/meow-TV-1.2.28.apk) |

APK SHA256：`1aa9fa97d2aa2e1955d1bab611936aa9ebd6ca8df63e6c2adca1d6a8b3b82f70`

## 来源与安全性说明

- 项目完全开源，源码见 https://github.com/upchr/meow ，任何人均可审计。
- 运行时申请权限仅 `MANAGE_EXTERNAL_STORAGE`（本地片库文件读取）与 AndroidX 自动生成的 `DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION`；**不含**通讯录、短信、电话、定位、悬浮窗等敏感权限。
- 应用不内置任何影视内容或站点数据；站点配置、弹幕数据均由用户自行导入，本项目只提供播放与加载能力。
- Release 包由 GitHub Actions 从上述公开源码构建，可下载后比对上方 SHA256。

## 测试截图

以下均为大屏横屏（1920×1080）实机截图，覆盖主要页面：

| 首页 | 分类 | 详情 |
| --- | --- | --- |
| ![首页](screenshots/01-home.jpg) | ![分类](screenshots/02-category.jpg) | ![详情](screenshots/03-detail.jpg) |

| 搜索 | 播放 | 片库 |
| --- | --- | --- |
| ![搜索](screenshots/04-search.jpg) | ![播放](screenshots/10-play.jpg) | ![片库](screenshots/05-library.jpg) |

| 历史 | 收藏 | 我的 |
| --- | --- | --- |
| ![历史](screenshots/06-history.jpg) | ![收藏](screenshots/07-favorites.jpg) | ![我的](screenshots/11-me.jpg) |

| 设置 | AI 助手 | 运行日志 |
| --- | --- | --- |
| ![设置](screenshots/08-settings.jpg) | ![AI](screenshots/09-ai.jpg) | ![日志](screenshots/12-logs.jpg) |

## 测试信息

- 测试时间：2026-11-27
- 测试环境：`http://192.168.1.20:30010/app/meow/`（后端 136 站点，health ok）+ Android 模拟器横屏（1920×1080）
- 测试版本：v1.2.28（versionCode 1228，minSdk 26 / targetSdk 34）
- 测试内容：覆盖 15 个页面路由（首页、分类、详情、播放、投屏、搜索、我的、历史、直播、片库、离线、收藏、设置、AI、日志），应用正常渲染与交互，无崩溃。
