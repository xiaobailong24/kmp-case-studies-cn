# KMP/CMP 架构分层

> Issue [#80](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/80) · 🛠️ KMP/CMP 架构分层 · 2026-02-25

## 概述

KMP/CMP 项目的架构分层可参考 Android 官方架构指南，结合多平台特性进行调整。

### 推荐分层

```
┌─────────────────────────────────┐
│           UI Layer              │  Compose Multiplatform (commonMain)
│     Screen / ViewModel          │
├─────────────────────────────────┤
│         Domain Layer            │  Use Cases / Repository Interfaces
│      (optional, pure Kotlin)    │
├─────────────────────────────────┤
│          Data Layer             │  Repository Impl / DataSource
│   Network(Ktor) + Local(Room)   │
├─────────────────────────────────┤
│        Platform Layer           │  expect/actual + 平台特定 API
│   Android / iOS / Desktop / Web │
└─────────────────────────────────┘
```

### KMP 项目中的代码共享策略

| 层级 | 共享程度 | 典型技术栈 |
|------|----------|-----------|
| UI | 可共享（CMP）或平台独立 | Compose Multiplatform / SwiftUI |
| Domain | 完全共享 | 纯 Kotlin |
| Data | 大部分共享 | Ktor, Room/SQLDelight, DataStore |
| Platform | 按平台实现 | expect/actual, Koin |

## 参考资料

- [应用架构指南 — Android 官方](https://developer.android.com/topic/architecture?hl=zh-cn)
