# Kotlin/Native interop: ObjC/Swift import

> Issue [#19](https://github.com/xiaobailong24/kmp-case-studies-cn/issues/19) · 标签：`articles` · 2025-07

## 概述

Kotlin/Native 通过 Objective-C 互操作层与 iOS 平台交互。理解其映射规则是 KMP iOS 开发的基础。

### 互操作映射

| Kotlin | Objective-C / Swift |
|--------|-------------------|
| `class` | `NSObject` 子类 |
| `interface` | `@protocol` |
| `suspend fun` | completionHandler callback |
| `sealed class` | 不直接映射（需手动处理） |
| `enum class` | 不直接映射（需 `@ObjCName`） |
| `Flow` | 需包装为 callback/Combine |

### 常见问题

1. **泛型擦除**：Kotlin 泛型在 ObjC 层会被擦除
2. **协程集成**：`suspend` 函数映射为 completionHandler，可通过 SKIE 或 KMP-NativeCoroutines 改善
3. **Swift 友好性**：使用 `@ObjCName` 优化导出名称

## 参考资料

- [Kotlin/Native ObjC interop — Kotlin Docs](https://kotlinlang.org/docs/native-objc-interop.html)
