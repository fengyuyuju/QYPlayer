# QYPlayer - 项目概述

## 项目简介

QYPlayer 是一个基于 Flutter 开发的跨平台有声书播放器应用，作为 AudioBookShelf 服务器的客户端。应用提供完整的有声书和播客收听体验，包括书库浏览、播放进度同步、后台播放、主题定制等功能。

项目采用 GetX 框架实现响应式状态管理和依赖注入，使用 just_audio 和 audio_service 处理音频播放，通过 Dio 与 AudioBookShelf API 通信。应用支持多种音频格式，并在 Windows/Linux 平台通过 media_kit 提供原生音频解码支持。

## 技术栈

| 类别 | 技术 | 用途 |
|------|------|------|
| **框架** | Flutter 3.6+ / Dart | 跨平台 UI 框架 |
| **状态管理** | GetX 4.7.2 | 响应式状态、路由、依赖注入 |
| **音频播放** | just_audio 0.10.0 | 核心音频播放引擎 |
| **后台播放** | audio_service 0.18.17 | 系统媒体控制和通知 |
| **跨平台音频** | just_audio_media_kit 2.1.0 | Windows/Linux 音频支持 |
| **HTTP 客户端** | Dio 5.8.0 | API 请求和拦截器 |
| **主题系统** | FlexColorScheme 8.4.0 | Material Design 3 主题 |
| **本地存储** | SharedPreferences | 用户设置和认证持久化 |
| **JSON 序列化** | json_serializable 6.9.4 | 数据模型代码生成 |
| **国际化** | flutter_localizations + Intl | 多语言支持 |

## 主要功能

- **有声书播放**：章节导航、进度追踪、播放速度调节（0.1x-2.0x）
- **后台播放**：系统通知控制、锁屏控制、耳机线控
- **书库管理**：多书库切换、排序筛选、网格/列表视图
- **进度同步**：10秒间隔自动同步、跨设备进度恢复
- **主题定制**：30+ 预设主题、亮/暗模式、系统主题跟随
- **多语言**：中文/英文，自动识别系统语言
- **播客支持**：剧集独立进度、播客特定 UI

## 支持平台

| 平台 | 状态 | 特殊配置 |
|------|------|---------|
| **Android** | 完整支持 | 前台服务后台播放、AudioServiceActivity |
| **iOS** | 完整支持 | 后台音频模式、系统媒体集成 |
| **macOS** | 完整支持 | 窗口管理（400x800）、中文本地化 |
| **Windows** | 完整支持 | media_kit 音频后端、MSIX 打包 |
| **Linux** | 完整支持 | media_kit 音频后端 |
| **Web** | 基础支持 | PWA 模式检测、特殊 padding 处理 |
