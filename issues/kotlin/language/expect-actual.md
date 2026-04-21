# Kotlin expect/actual 机制

> Issue [#62](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/62) · ⚒️ Kotlin expect/actual

## 概述

`expect`/`actual` 是 Kotlin Multiplatform 的核心机制，允许在公共代码中声明平台相关的 API 接口，然后在各平台模块中提供具体实现。

### 基本用法

```kotlin
// commonMain
expect fun platformName(): String

// androidMain
actual fun platformName(): String = "Android"

// iosMain
actual fun platformName(): String = "iOS"
```

### 支持的声明类型

- `expect fun` / `actual fun` — 函数
- `expect class` / `actual class` — 类（含构造器）
- `expect object` / `actual object` — 单例
- `expect val`/`var` / `actual val`/`var` — 属性
- `expect annotation` — 注解（如 `@Parcelize`）

### 最佳实践

1. 尽量减少 `expect`/`actual` 的使用范围，优先使用接口 + 依赖注入
2. 复杂的平台实现考虑使用 `interface` + `expect` 工厂函数
3. Kotlin 2.0+ 支持 `expect`/`actual` 用于 `typealias`

## 参考资料

- [Expected and actual declarations — Kotlin Docs](https://kotlinlang.org/docs/multiplatform-expect-actual.html)
