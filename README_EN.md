# QYPlayer - Project Overview

## Introduction

QYPlayer is a cross-platform audiobook player application built with Flutter, serving as a client for AudioBookShelf server. The app provides a complete audiobook and podcast listening experience, including library browsing, playback progress synchronization, background playback, theme customization, and more.

The project uses the GetX framework for reactive state management and dependency injection, just_audio and audio_service for audio playback, and Dio for communicating with the AudioBookShelf API. The app supports multiple audio formats and provides native audio decoding support on Windows/Linux platforms through media_kit.

## Tech Stack

| Category | Technology | Purpose |
|----------|------------|---------|
| **Framework** | Flutter 3.6+ / Dart | Cross-platform UI framework |
| **State Management** | GetX 4.7.2 | Reactive state, routing, dependency injection |
| **Audio Playback** | just_audio 0.10.0 | Core audio playback engine |
| **Background Playback** | audio_service 0.18.17 | System media controls and notifications |
| **Cross-platform Audio** | just_audio_media_kit 2.1.0 | Windows/Linux audio support |
| **HTTP Client** | Dio 5.8.0 | API requests and interceptors |
| **Theme System** | FlexColorScheme 8.4.0 | Material Design 3 themes |
| **Local Storage** | SharedPreferences | User settings and auth persistence |
| **JSON Serialization** | json_serializable 6.9.4 | Data model code generation |
| **Internationalization** | flutter_localizations + Intl | Multi-language support |

## Key Features

- **Audiobook Playback**: Chapter navigation, progress tracking, playback speed adjustment (0.1x-2.0x)
- **Background Playback**: System notification controls, lock screen controls, headphone controls
- **Library Management**: Multi-library switching, sorting and filtering, grid/list views
- **Progress Sync**: Auto-sync every 10 seconds, cross-device progress recovery
- **Theme Customization**: 30+ preset themes, light/dark mode, system theme following
- **Multi-language**: Chinese/English, automatic system language detection
- **Podcast Support**: Independent episode progress, podcast-specific UI

## Supported Platforms

| Platform | Status | Special Configuration |
|----------|--------|----------------------|
| **Android** | Full Support | Foreground service for background playback, AudioServiceActivity |
| **iOS** | Full Support | Background audio mode, system media integration |
| **macOS** | Full Support | Window management (400x800), Chinese localization |
| **Windows** | Full Support | media_kit audio backend, MSIX packaging |
| **Linux** | Full Support | media_kit audio backend |
| **Web** | Basic Support | PWA mode detection, special padding handling |
