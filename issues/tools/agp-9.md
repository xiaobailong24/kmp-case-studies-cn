# Android Gradle Plugin 9.0

> Issue [#72](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/72) · ⚒️ Android Gradle Plugin 9.0

## 概述

AGP 9.0 是 Android 构建工具链的重要升级，配合 Gradle 9.0 使用。JetBrains 发布了详细的迁移指南，涵盖两个关键任务。

### 迁移任务

1. **Android 应用采用 AGP 9.0 集成的 Kotlin 支持**：AGP 9.0 内置了对 Kotlin 编译的集成支持
2. **KMP 项目迁移到新插件**：使用 `com.android.kotlin.multiplatform.library` 替代旧的 KMP + Android 组合配置

### 关键变化

- 要求 Gradle 9.0+
- 构建性能改进
- KMP 专用 Android 库插件（`com.android.kotlin.multiplatform.library`）
- 新的 DSL API

## 参考资料

- [Migrating to AGP 9.0 — JetBrains Kotlin Blog](https://blog.jetbrains.com/kotlin/)
- [Android Gradle Plugin Release Notes](https://developer.android.com/build/releases/gradle-plugin)
